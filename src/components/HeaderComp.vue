<script>
export default{
    name: 'HeaderComp',
}
</script>

<template>
    <div class="header">
      <h1 class="titolo">Marianna</h1>
      <div class="barra"></div>
      <!-- LISTA CON HOME SHOP ECC -->
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
          width: 80vw;
          height: 0.5rem;
          background-color: rgb(144, 102, 5);
        }
  }
  
  
  </style>
  