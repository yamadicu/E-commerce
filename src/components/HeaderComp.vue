<script>
export default{
    name: 'HeaderComp',
    data() {
      return{
        linkBar:[
          {
            url: '/',
            name: 'home',
            stato: false
          },{
            url: '/',
            name: 'shop',
            stato: true
          },{
            url: '/',
            name: 'chi siamo',
            stato: false 
          },
        ]
      }
    }
}
</script>

<template>
    <div class="header">
      <h1 class="titolo">Marianna</h1>
      <div class="barra"></div>
      <!-- LISTA CON HOME SHOP ECC -->
      <ul>
        <li v-for="(elem, index) in linkBar" :key="index" :class="elem.stato ? 'active' : '' ">
          <a href="elem.url">{{ elem.name }}</a>
        </li>
      </ul>
    </div>
  </template>
  
  <style lang="scss">
  .header {
    display: flex;
    flex-direction: column;
    align-items: center;

    .titolo {
      font-size: 6rem;
    }

    .barra {
      width: 90vw;
      height: 0.3rem;
      background-color: rgb(144, 102, 5);
      margin-bottom: 0.5rem;
    }

    ul{
      display: flex;

      li{
        list-style: none;
        margin: 0 10px;

        a{
          text-decoration: none;
          color: black;
          text-transform: uppercase;
          font-weight: bold;
          font-size: 1.1rem;
        }

        &.active {
          border-bottom: 3px solid rgb(144, 102, 5);
        }

        &.active a {
            color: rgb(144, 102, 5);
        }
      }
    }
  }
  
  
  </style>
  