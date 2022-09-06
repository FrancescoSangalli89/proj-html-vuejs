<template>
    <main>
        <MyAboutUs />
        <MyUpdates />
        <MySpeaker />
        <MyProgram />
        <MyMaps />
        <MyLocation />
        <MyNews />
        <MyTickets />
        <MyPresentation />
    </main>
</template>

<script>

    import MyAboutUs from '../main/MyAboutUs.vue';
    import MyUpdates from '../main/MyUpdates.vue';
    import MySpeaker from '../main/MySpeaker.vue';
    import MyProgram from '../main/MyProgram.vue';
    import MyMaps from '../main/MyMaps.vue';
    import MyLocation from '../main/MyLocation.vue';
    import MyNews from '../main/MyNews.vue';
    import MyTickets from '../main/MyTickets.vue';
    import MyPresentation from '../main/MyPresentation.vue';

export default {
    name: 'MyMain',
    components: {
        MyAboutUs,
        MyUpdates,
        MySpeaker,
        MyProgram,
        MyMaps,
        MyLocation,
        MyNews,
        MyTickets,
        MyPresentation
        
    }
}
</script>

<style scoped lang="scss">

</style>