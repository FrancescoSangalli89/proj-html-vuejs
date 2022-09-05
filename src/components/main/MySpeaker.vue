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
                <div v-for="(speaker, index) in speakers" :key="index" class="card">
                    <img :src="speaker.image" :alt="speaker.name + ' image'">
                    <h3>{{speaker.name}}</h3>
                    <div>{{speaker.position}}</div>
                </div>
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
                width: 25%;
                margin: 20px;
                img {
                    height: 180px;
                    margin-bottom: 20px;
                }
                h3 {
                    font-weight: 500;
                    margin-bottom: 10px;
                }
                div {
                    color: $text-color;
                    font-style: italic;
                }
            }
        }
    }

</style>