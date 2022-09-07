<template>
    <li class="newsCard">
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
</template>

<script>
export default {
    name: 'MySingleNew',
    props: {
        news: Object
    }
}
</script>

<style scoped lang="scss">
    @import '../../assets/styles/vars.scss';
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
</style>