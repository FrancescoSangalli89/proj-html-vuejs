<template>
    <section class="footerBtm">
        <div class="container d-flex footerBtmElemets">
            <span>&copy; Copyright GoodLayers, All Right Reserved</span>
            <span>
                <a href="#">About Us</a>
                <a href="#">Accomodation</a>
                <a href="#">Call For Paper</a>
                <a href="#">Contact Us</a>
            </span>
        </div>
    </section>
</template>

<script>
export default {
    name: 'MyFooterBtm'
}
</script>

<style scoped lang="scss">
    @import '../../assets/styles/vars.scss';
    .footerBtm {
        background-color: $footer-btm-background;
        height: 70px;
        .footerBtmElemets {
            height: 100%;
            justify-content: space-between;
            align-items: center;
        }
        span, a {
            color: $text-color;
            font-weight: 300;
        }
        a {
            border-right: 1px solid $text-color;
            margin-right: 5px;
            padding-right: 5px;
            &:last-child {
                border: none;
            }
        }
    }
</style>