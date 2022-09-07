<template>
    <section class="footerAboutUs component">
        <h5>ABOUT US</h5>
        <p>Lorem ipsum dolor sit amet conse adipisicing elit. Molestiae iusto repellendus quod a animi velit.</p>
        <div class="socialIcons d-flex">
            <a href="#" v-for="(icon, index) in icons" :key="index">
                <i  class="fa-brands" :class="icon"></i>
            </a>
        </div>
    </section>
</template>

<script>
export default {
    name: 'MyFooterAboutUs',
    data() {
        return {
            icons: ['fa-square-twitter', 'fa-square-facebook', 'fa-linkedin', 'fa-square-pinterest', 'fa-square-youtube', 'fa-square-instagram'],
        }
    }
}
</script>

<style scoped lang="scss">
    @import '../../assets/styles/footerComponentsUtilities.scss';
    i {
        color: #fff;
        margin-right: 15px;
        font-size: 25px;
    }
</style>