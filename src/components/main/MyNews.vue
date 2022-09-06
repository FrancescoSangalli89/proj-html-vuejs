<template>
    <section class="container news">
        <div class="newsTop d-flex">
            <h3>RECENT NEWS</h3>
            <a href="#">Read All News</a>
        </div>

        <ul class="newsList d-flex">
            <li class="newsCard"  v-for="(news, index) in newsList" :key="index">
                <img :src="news.img" alt="">
                <div class="sticker" :class="news.sticky?'stickyOn':'stickyOff'">
                    <i class="fa-solid fa-bullhorn"></i>
                    <span>STICKY POST</span>
                </div>
                <div class="dateComments">{{news.date}} / {{news.comments}} Comments</div>
                <h4>{{news.title}}</h4>
                <p>{{news.text}}</p>
                <a :href="news.url">Read More</a>
            </li>
        </ul>
    </section>
</template>

<script>
export default {
    name: 'MyNews',
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
            .newsCard {
                width: calc(100% / 3 - 20px);
                position: relative;
                img {
                    width: 100%;
                    margin-bottom: 30px;
                }
                .sticker {
                    color: #fff;
                    background-color: rgba($color: #000000, $alpha: 0.8);
                    padding: 10px;
                    position: absolute;
                    right: 0;
                    top: 173px;
                    i {
                        margin-right: 10px;
                    }
                }
                .dateComments {
                    color: $text-color;
                    font-style: italic;
                    font-size: 12px;
                    margin-bottom: 10px;
                }
                h4 {
                    font-weight: 600;
                    margin-top: 5px;
                }
                p {
                    margin: 35px 0 35px 0;
                    color: $text-color;
                }
                a {
                    color: $primary-color;
                    font-style: italic;
                }
            }
        }
    }
    
</style>