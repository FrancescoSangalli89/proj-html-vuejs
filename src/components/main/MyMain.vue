<template>
    <main>
        <MyAboutUs />
        <MyUpdates />
        <MySpeaker />
    </main>
</template>

<script>

    import MyAboutUs from '../main/MyAboutUs.vue';
    import MyUpdates from '../main/MyUpdates.vue';
    import MySpeaker from '../main/MySpeaker.vue';

export default {
    name: 'MyMain',
    components: {
        MyAboutUs,
        MyUpdates,
        MySpeaker
    }
}
</script>

<style scoped lang="scss">

</style>