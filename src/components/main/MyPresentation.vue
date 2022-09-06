<template>
    <section class="presentationSection container d-flex">
        <div class="presentation">
            <h4>PRESENTATION</h4>
            <iframe src="https://player.vimeo.com/video/180480556?h=588e9d91d2" width="640" height="360" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe>
        </div>
        <div class="twitter">
            <h4>TWITTER FEED</h4>
            <div class="feed d-flex" v-for="(twitter, index) in twitters" :key="index">
                <div>
                    <i class="fa-brands fa-twitter"></i>
                </div>
                <div>
                    <p>{{twitter.text}}</p><a href="#">https//t.co/{{twitter.url}}</a>
                    <div  class="timePassed">{{twitter.time}} days ago</div>
                </div>
            </div>
            
        </div>
    </section>
</template>

<script>
export default {
    name: 'MyPresentation',
    data() {
        return {
            twitters: [
                {
                    text: `Stand out and be vibrant with some of the best bright and bold templates on @Envato Elements. And add a splash of c...`,
                    time: 3, 
                    url: 'jFrsnzEJK7'
                },
                {
                    text: 'Do you need to deliver the perfect presentation or creative pitch? Sure, your ideas and plan need to be on-point, b...',
                    time: 9, 
                    url: 'nCmvsJVDpW'
                },
                {
                    text: 'Cut yourself a piece of the BFCM sales pie with a solid marketing plan. Here are 5 ways to optimize your content fo...',
                    time: 11, 
                    url: 'UZfKHshEOT'
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
    @import '../../assets/styles/vars.scss';
    .presentationSection {
        justify-content: space-between;
        padding: 100px 0;
        .presentation, .twitter {
            width: 50%;
        }
        .presentation {
            iframe {
                width: 100%;
                padding: 0 30px;
            }
        }
        .twitter {
            .feed {
                padding-top: 30px;
                i {
                    color: #46BEEE;
                    font-size: 25px;
                    margin-right: 10px;
                }
                p, .timePassed {
                    color: $text-color;
                }
                p {
                    display: inline;
                }
                a {
                    color: $primary-color;
                }
                .timePassed {
                    font-style: italic;
                    margin-top: 20px;
                }
            }
        }
    }
    h4 {
        margin-bottom: 30px;
    }
</style>