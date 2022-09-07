<template>
    <section class="speakersSection">
        <div class="container">
            <div class="speakersTop d-flex">
                <h2>SPEAKERS</h2>
                <div>
                    <button class="left">
                        <i class="fa-solid fa-angle-left"></i>
                    </button>
                    <button class="right">
                        <i class="fa-solid fa-angle-right"></i>
                    </button>
                </div>
            </div>
            <div class="speakerCards d-flex">
                <a href="#" v-for="(speaker, index) in speakers" :key="index" class="card">
                    <div class="speakerImg">
                        <img :src="speaker.image" :alt="speaker.name + ' image'">
                        <div class="overlay">
                            <a href="#">
                                <i class="fa-brands fa-twitter"></i>
                            </a>
                            <a href="#">
                                <i class="fa-brands fa-facebook-f"></i>
                            </a>
                            <a href="#">
                                <i class="fa-brands fa-linkedin-in"></i>
                            </a>
                        </div>
                    </div>
                    <h3>{{speaker.name}}</h3>
                    <div>{{speaker.position}}</div>
                </a>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'MySpeaker',
    data() {
        return {
            speakers: [
                {   
                    image: require('../../assets/images/speaker-6.jpg'),
                    name: 'PATRICK SPENCER',
                    position: 'S&P Analyzer'
                },
                {   
                    image: require('../../assets/images/speaker-5.jpg'),
                    name: 'JANET JONES',
                    position: "Newyork Post's GM"
                },
                {   
                    image: require('../../assets/images/speaker-4.jpg'),
                    name: 'MICHAEL DOVER',
                    position: "Starbuck's CEO"
                },
                {   
                    image: require('../../assets/images/speaker-3.jpg'),
                    name: 'ANGELINA HOLY',
                    position: "Maxii's Manager"
                },
                {   
                    image: require('../../assets/images/speaker-2.jpg'),
                    name: 'CHARLIE BROWN',
                    position: "Maxii's CEO"
                },
                {   
                    image: require('../../assets/images/speaker-8.jpg'),
                    name: 'PIPERITA PATTY',
                    position: "Pizzeria bella Napoli owner"
                },
                {   
                    image: require('../../assets/images/speaker-7.jpg'),
                    name: 'MAGO MERLINO',
                    position: "knight of the round"
                },
                {   
                    image: require('../../assets/images/speaker-1.jpg'),
                    name: 'GODZILLA',
                    position: "Japanise Dragon"
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
    @import '../../assets/styles/vars.scss';

    .speakersSection {
        background-color: $section-background;
        padding: 80px 0;
        .speakersTop {
            justify-content: space-between;
            align-items: center;
            margin-bottom: 65px;
            button {
                height: 30px;
                width: 30px;
                color: #fff;
                background-color: $primary-color;
                border: none;
                margin: 0 10px;
                font-size: 20px;
                cursor: pointer;
            }
        }
        .speakerCards {
            justify-content: space-between;
            overflow: scroll;
            .card {
                text-align: center;
                width: calc(100% / 4);
                margin: 20px;
                .speakerImg {
                    position: relative;
                    height: 180px;
                    img {
                        height: 100%;
                        border-radius: 5px;
                    }
                    .overlay {
                        position: absolute;
                        background-color: rgba($color: #ff0000, $alpha: 0.5);
                        top: 0;
                        left: 0;
                        width: 100%;
                        height: 100%;
                        border-radius: 5px;
                        line-height: 180px;
                        display: none;
                        a {
                            color: #fff;
                            margin-right: 5px;
                            padding: 5px;
                            font-size: 25px;
                        }
                    }
                    &:hover .overlay {
                        display: block;
                    }
                }
                h3 {
                    font-weight: 500;
                    margin-top: 20px;
                    margin-bottom: 10px;
                    color: #000;
                }
                div {
                    color: $text-color;
                    font-style: italic;
                }
            }
        }
    }

</style>