<template>
    <section class="footerTop">
        <div class="container d-flex componentContainer">
            <MyFooterAboutUs />
            <MyFooterNews />
            <MyFooterTicket />
            <MyFooterGallery />
        </div>
    </section>
</template>

<script>
    import MyFooterAboutUs from './MyFooterAboutUs.vue';
    import MyFooterNews from './MyFooterNews.vue';
    import MyFooterTicket from './MyFooterTicket.vue';
    import MyFooterGallery from './MyFooterGallery.vue';
export default {
    name: 'MyFooterTop',
    components: {
        MyFooterAboutUs,
        MyFooterNews,
        MyFooterTicket,
        MyFooterGallery
    }
}
</script>

<style scoped lang="scss">
    @import '../../assets/styles/vars.scss';
    .footerTop {
        background-color: $footer-top-background;
        padding: 70px 0;
        .componentContainer {
            justify-content: space-between;
        }
    }
</style>