<template>
    <section class="program container">
        <div class="programTop d-flex">
            <div class="d-flex">
                <h2>PROGRAM</h2>
                <div>
                    <p>This conference run through all 4 days from 23 - 26 May 2023.</p>
                    <p>We also provide free lunch and coffee break in each day.</p>
                </div>
            </div>
            <a href="#">View Full Program</a>
        </div>
        <div class="programBtm">
            <div class="programHeader d-flex">
                <div v-for="(day, index) in days" :key="index" class="programDay" :class="(activeDay==index)?'active':''" @click="selectDay(index)">
                    <h4>DAY {{day.number}}</h4>
                    <div>{{day.date}} May 2023</div>
                </div>
            </div>
            <div class="programContainer d-flex">

                <div class="programLeft">
                    <div>
                        <i class="fa-regular fa-clock"></i>
                        <span>{{programs[activeDay].hours}}</span>
                    </div>
                    <div>
                        <i class="fa-solid fa-location-arrow"></i>
                        <span>ROOM A</span>
                    </div>
                    <div>
                        <i class="fa-solid fa-user"></i>
                        <span class="name">{{programs[activeDay].name}}</span>
                    </div>
                </div>
                <div class="programRight">
                    <h3>{{programs[activeDay].title}}</h3>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Alias libero ipsa cupiditate quod nesciunt explicabo voluptatibus molestiae, itaque esse est...</p>
                    <img :src="programs[activeDay].url" :alt="programs[activeDay].name">
                </div>

            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'MyProgram',
    data() {
        return {
            activeDay: 0,
            days: [
                {
                    number: 1,
                    date: 23
                },
                {
                    number: 1,
                    date: 23
                },
                {
                    number: 2,
                    date: 24
                },
                {
                    number: 3,
                    date: 25
                },
                {
                    number: 4,
                    date: 26
                },
            ],
            programs: [
                {
                    hours: '9.30 - 10.30',
                    name: 'JANET JONES',
                    title: 'WELCOMING AND INTRODUCTION',
                    url: require('../../assets/images/speaker-5.jpg')
                },
                {
                    hours: '10.30 - 12.30',
                    name: 'PATRICK SPENCER',
                    title: 'PINCO PANCO',
                    url: require('../../assets/images/speaker-6.jpg')
                },
                {
                    hours: '9.30 - 12.30',
                    name: 'MICHAEL DOVER',
                    title: 'PANCO PINCO',
                    url: require('../../assets/images/speaker-4.jpg')
                },
                {
                    hours: '9.30 - 12.30',
                    name: 'ANGELINA HOLY',
                    title: 'LA TAUROMACHIA',
                    url: require('../../assets/images/speaker-3.jpg')
                },
                {
                    hours: '9.30 - 14.30',
                    name: 'CHARLIE BROWN',
                    title: 'THIS IS THE END',
                    url: require('../../assets/images/speaker-2.jpg')
                }
            ]
        }
    },
    methods: {
        selectDay(position) {
            this.activeDay = position;
        }
    }
}
</script>

<style scoped lang="scss">
    @import '../../assets/styles/vars.scss';
    .program {
        padding: 120px 0 80px 0;
        .programTop {
            align-items: center;
            justify-content: space-between;
            margin-bottom: 75px;
            h2 {
                margin-right: 50px;
            }
            p {
                color: $text-color;
            }
            a {
                font-style: italic;
                color: $primary-color;
            }
        }
        .programBtm {
            .programHeader {
                background-color: $primary-color;
                .programDay {
                    padding: 15px;
                    width: calc(100% / 6);
                    color: #fff;
                    background-color: $primary-color;
                    border-right: 0.2px solid #333;
                    cursor: pointer;
                    &:hover, &.active {
                        background-color: $primary-color-hover;
                    }
                    h4 {
                        margin-bottom: 10px;
                    }
                }
            }
            .programContainer {
                background-color: $section-background;
                .programLeft {
                    width: 30%;
                    padding: 50px;
                    div {
                        color: $text-color;
                        margin: 20px 0;
                        i {
                            margin-right: 10px;
                        }
                        .name {
                            color: $primary-color;
                        }
                    }
                }
                .programRight {
                    padding: 50px;
                    h3 {
                        font-weight: 400;
                    }
                    p {
                        color: $text-color;
                        margin: 35px 0;
                    }
                    img {
                        width: 100px;
                    }
                }
            }
        }
    }
    
</style>