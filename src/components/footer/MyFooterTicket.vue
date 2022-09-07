<template>
    <section class="component">
        <h5>GET YOUR SEAT!</h5>
        <p>Book for your seat before it's too late. We provide variety of ticket options.</p>
        <button>CHECK OUT TICKETS!</button>
    </section>
</template>

<script>
export default {
    name: 'MyFooterTicket'
}
</script>

<style scoped lang="scss">
    @import '../../assets/styles/footerComponentsUtilities.scss';
    button {
        color: #fff;
        background-color: $primary-color;
        border: none;
        border-bottom: 3px solid $primary-color-hover;
        padding: 10px;
        font-weight: 600;
    }
</style>