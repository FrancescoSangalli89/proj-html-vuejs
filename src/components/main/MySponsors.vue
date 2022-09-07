<template>
    <section class="sponsors">
        <div class="container">
            <h2>SPONSORS</h2>
            <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Labore, odio.</p>
            <div class="sponsorLogos d-flex">
                <img v-for="(sponsor, index) in sponsors" :key="index" :src="sponsor" alt="sponsor logo">
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'MySponsors',
    data() {
        return {
            sponsors: [
                require('../../assets/images/banner-1.jpg'),
                require('../../assets/images/banner-2.jpg'),
                require('../../assets/images/banner-3.jpg'),
                require('../../assets/images/banner-4.jpg'),
                require('../../assets/images/banner-5.jpg'),
                require('../../assets/images/banner-6.jpg')
            ]
        }
    }
}
</script>

<style scoped lang="scss">
    @import '../../assets/styles/vars.scss';
    .sponsors {
        background-color: $section-background;
        text-align: center;
        padding: 80px 0;
        h2 {
            margin-bottom: 40px;
        }
        p {
            width: 30%;
            margin: auto;
            margin-bottom: 60px;
            color: $text-color;
        }
        .sponsorLogos {
            justify-content: space-between;
            img {
                width: calc(100% / 6 - 20px);
            }
        }
    }
</style>