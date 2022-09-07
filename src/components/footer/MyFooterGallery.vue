<template>
    <section class="component">
        <h5>GALLERY FROM LAST YEARS</h5>
        <div class="imageContainer">
            <a v-for="(photo, index) in photos" :key="index" href="#">
                <img :src="photo" alt="">
            </a>
        </div>
    </section>
</template>

<script>
export default {
    name: 'MyFooterGallery',
    data() {
        return {
            photos: [
                require('../../assets/images/6426608875_186070f8ca_o-150x150.jpg'), 
                require('../../assets/images/13349065283_64d09b067c_o-150x150.jpg'), 
                require('../../assets/images/card01-150x150.jpg'), 
                require('../../assets/images/card04-150x150.jpg'), 
                require('../../assets/images/photodune-6745579-modern-creative-man-relaxing-on-workspace-.jpg'), 
                require('../../assets/images/photodune-6745585-modern-creative-workspace-m-150x150.jpg'), 
                require('../../assets/images/photodune-6745606-man-wristwatch-calendar-key-and-glasses-on.jpg'), 
                require('../../assets/images/photodune-7770665-two-white-coffee-mug-with-diy-decoration-o (1).jpg'), 
                require('../../assets/images/photodune-8522811-speaker-at-business-conference-and-present (1).jpg'), 
                require('../../assets/images/photodune-8523683-speaker-at-business-convention-and-present.jpg'), 
                require('../../assets/images/photodune-8795110-overhead-of-essentials-denim-clothes-m-150.jpg'), 
                require('../../assets/images/photodune-8797753-multiethnic-people-with-startup-business-t (1).jpg')
            ]
        }
    }
}
</script>

<style scoped lang="scss">
    @import '../../assets/styles/footerComponentsUtilities.scss';
    .imageContainer {
        img {
            width: calc(100% / 4 - 5px);
            margin-right: 4px;
        }
    }
</style>