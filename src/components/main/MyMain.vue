<template>
    <main>
        <MyAboutUs />
        <MyUpdates />
        <MySpeaker />
        <MyProgram />
        <MyMaps />
    </main>
</template>

<script>

    import MyAboutUs from '../main/MyAboutUs.vue';
    import MyUpdates from '../main/MyUpdates.vue';
    import MySpeaker from '../main/MySpeaker.vue';
    import MyProgram from '../main/MyProgram.vue';
    import MyMaps from '../main/MyMaps.vue';

export default {
    name: 'MyMain',
    components: {
        MyAboutUs,
        MyUpdates,
        MySpeaker,
        MyProgram,
        MyMaps
        
    }
}
</script>

<style scoped lang="scss">

</style>