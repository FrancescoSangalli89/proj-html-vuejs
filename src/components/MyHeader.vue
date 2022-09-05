<template>
    <header>
        <MyHeaderTop :links="links"/>
        <MyJumbotron />
    </header>
</template>

<script>

    import MyHeaderTop from './MyHeaderTop.vue';
    import MyJumbotron from './MyJumbotron.vue';

export default {
    name: 'MyHeader',
    components: {
        MyHeaderTop,
        MyJumbotron
    },
    data() {
        return {
            links: [
                {
                    text: 'HOME',
                    url: '#',
                    active: false
                },
                {
                    text: 'PAGES',
                    url: '#',
                    active: false
                },
                {
                    text: 'PROGRAM',
                    url: '#',
                    active: false
                },
                {
                    text: 'TICKETS',
                    url: '#',
                    active: false
                },
                {
                    text: 'SPEAKERS',
                    url: '#',
                    active: false
                },
                {
                    text: 'PAPERS',
                    url: '#',
                    active: false
                },
                {
                    text: 'BLOG',
                    url: '#',
                    active: false
                },
                {
                    text: 'SHORTCODES',
                    url: '#',
                    active: false
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">

</style>