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
        <MySponsors />
    </main>
</template>

<script>

    import MyAboutUs from './MyAboutUs.vue';
    import MyUpdates from './MyUpdates.vue';
    import MySpeaker from './MySpeaker.vue';
    import MyProgram from './MyProgram.vue';
    import MyMaps from './MyMaps.vue';
    import MyLocation from './MyLocation.vue';
    import MyNews from './MyNews.vue';
    import MyTickets from './MyTickets.vue';
    import MyPresentation from './MyPresentation.vue';
    import MySponsors from './MySponsors.vue';

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
        MyPresentation,
        MySponsors
        
    }
}
</script>

<style scoped lang="scss">

</style>