<template>
    <footer>
        <MyFooterTop />
        <MyFooterBtm />
    </footer>
</template>

<script>
    import MyFooterTop from './MyFooterTop.vue';
    import MyFooterBtm from './MyFooterBtm.vue';
export default {
    name: 'MyFooter',
    components: {
        MyFooterTop,
        MyFooterBtm
    }
}
</script>

<style scoped lang="scss">

</style>