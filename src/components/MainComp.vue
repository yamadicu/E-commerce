<script>
import HeaderComp from './HeaderComp.vue';
import FooterComp from './FooterComp.vue';
export default{
    name: 'MainComp',

    components: {
        HeaderComp,
        FooterComp
    }
}
</script>

<template>
    <HeaderComp></HeaderComp>
    <h1>componente main</h1>
    <FooterComp></FooterComp>
</template>

<style lang="scss" scoped></style>