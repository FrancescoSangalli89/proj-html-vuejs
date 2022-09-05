<template>
    <section class="aboutUs container">
        <ul class="aboutUsList d-flex">
            <li class="aboutUsCard"  v-for="(card, index) in aboutUs" :key="index">
                <div class="d-flex">
                    <i class="fa-solid" :class="card.icon"></i>
                    <div>
                        <h4>{{card.title}}</h4>
                        <p>{{card.text}}</p>
                        <a :href="card.url">Learn More</a>
                    </div>
                </div>
            </li>
        </ul>
    </section>
</template>

<script>
export default {
    name: 'MyAboutUs',
    data() {
        return {
            aboutUs: [
                {
                    icon: 'fa-trophy',
                    title: 'WHO WE ARE',
                    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptas nulla ipsam beatae? Facilis doloremque earum veniam ad illo praesentium eveniet?',
                    url: '#'
                },
                {
                    icon: 'fa-bolt-lightning',
                    title: 'WHAT WE DO',
                    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptas nulla ipsam beatae? Facilis doloremque earum veniam ad illo praesentium eveniet?',
                    url: '#'
                },
                {
                    icon: 'fa-question',
                    title: 'WHY US?',
                    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptas nulla ipsam beatae? Facilis doloremque earum veniam ad illo praesentium eveniet?',
                    url: '#'
                }
            ]
        }
    }
}
</script>

<style lang="scss">
    @import '../../assets/styles/vars.scss';
    .aboutUsList {
        margin: 70px 0;
        justify-content: space-between;
        align-items: center;
        .aboutUsCard {
            width: 30%;
            i {
                padding-right: 20px;
                font-size: 30px;
                color: $text-color;
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
</style>