<template>
    <header>
        <MyHeaderTop />
        <MyJumbotron />
    </header>
</template>

<script>

    import MyHeaderTop from './MyHeaderTop.vue';
    import MyJumbotron from './MyJumbotron.vue';

export default {
    name: 'MyHeader',
    components: {
        MyHeaderTop,
        MyJumbotron
    }
}
</script>

<style scoped lang="scss">

</style>