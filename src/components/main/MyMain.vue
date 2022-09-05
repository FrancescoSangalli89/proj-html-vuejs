<template>
    <main>
        <MyAboutUs/>
        <MyUpdates />
    </main>
</template>

<script>

    import MyAboutUs from '../main/MyAboutUs.vue';
    import MyUpdates from '../main/MyUpdates.vue';

export default {
    name: 'MyMain',
    components: {
        MyAboutUs,
        MyUpdates
    }
}
</script>

<style scoped lang="scss">

</style>