<template>
    <section class="component">
        <h5>RECENT NEWS</h5>
        <ul>
            <li v-for="n in 5" :key="n">
                <a href="#">
                    <i class="fa-solid fa-angle-right"></i>
                    <span>Lorem ipsum dolor sit amet.</span>
                </a>
            </li>
        </ul>
    </section>
</template>

<script>
export default {
    name: 'MyFooterNews'
}
</script>

<style scoped lang="scss">
    @import '../../assets/styles/footerComponentsUtilities.scss';
    li {
        margin-bottom: 25px;
        a {
            color: $text-color;
            i {
                margin-right: 10px;
            }
        }
    }
</style>