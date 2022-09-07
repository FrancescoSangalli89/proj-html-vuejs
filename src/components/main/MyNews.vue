<template>
    <section class="container news">
        <div class="newsTop d-flex">
            <h3>RECENT NEWS</h3>
            <a href="#">Read All News</a>
        </div>
        <ul class="newsList d-flex">
            <MySingleNew v-for="(news, index) in newsList" :key="index" :news="news" />
        </ul>
    </section>
</template>

<script>

    import MySingleNew from './MySingleNew.vue';

export default {
    name: 'MyNews',
    components: {
        MySingleNew
    },
    data() {
        return {
            newsList: [
                {
                    sticky: true,
                    img: require('../../assets/images/photodune-7770665-two-white-coffee-mug-with-diy-decoration-o.jpg'),
                    date: '06 Sept 2022',
                    comments: 0,
                    title: 'NEW NEWS',
                    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptas nulla ipsam beatae? Facilis doloremque earum veniam ad illo praesentium eveniet?',
                    url: '#'
                },
                {
                    sticky: false,
                    img: require('../../assets/images/photodune-8797753-multiethnic-people-with-startup-business-t.jpg'),
                    date: '03 Sept 2022',
                    comments: 2,
                    title: 'OLD NEWS',
                    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptas nulla ipsam beatae? Facilis doloremque earum veniam ad illo praesentium eveniet?',
                    url: '#'
                },
                {
                    sticky: false,
                    img: require('../../assets/images/photodune-8522811-speaker-at-business-conference-and-present.jpg'),
                    date: '17 aug 2022',
                    comments: 10,
                    title: 'OLDEST NEWS',
                    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptas nulla ipsam beatae? Facilis doloremque earum veniam ad illo praesentium eveniet?',
                    url: '#'
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
    @import '../../assets/styles/vars.scss';
    .news {
        padding: 80px 0;
        .newsTop {
            align-items: center;
            justify-content: space-between;
            margin-bottom: 75px;
            h2 {
                margin-right: 50px;
            }
            a {
                font-style: italic;
                color: $primary-color;
            }
        }
        .newsList {
            margin: 70px 0;
            justify-content: space-between;
            align-items: center;
        }
    }
    
</style>