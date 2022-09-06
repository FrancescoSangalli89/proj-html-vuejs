<template>
    <section>
        <div class="d-flex mapsContainer">
            <img class="map" v-for="(map, index) in maps" :key="index" :src="map.url" alt="">
            <img class="object google" src="../../assets/images/google4.png" alt="">
            <div class="object visualization">
                <img class="view" src="../../assets/images/image (4).svg" alt="">
                <div class="zoom">
                    <div>
                        <img class="plus" src="../../assets/images/image (7).svg" alt="">
                    </div>
                    <div class="line"></div>
                    <div>
                        <img class="min" src="../../assets/images/image (8).svg" alt="">
                    </div>
                </div>
            </div>
            
            <img class="object position" src="../../assets/images/default_marker.png" alt="">
        </div>
    </section>
</template>

<script>
export default {
    name: 'myMaps',
    data() {
        return {
            maps: [
                {
                    url: require('../../assets/images/vt1.png')
                },
                {
                    url: require('../../assets/images/vt2.png')
                },
                {
                    url: require('../../assets/images/vt3.png')
                },
                {
                    url: require('../../assets/images/vt4.png')
                },
                {
                    url: require('../../assets/images/vt5.png')
                },
                {
                    url: require('../../assets/images/vt6.png')
                },
                {
                    url: require('../../assets/images/vt7.png')
                },
                {
                    url: require('../../assets/images/vt8.png')
                },
                {
                    url: require('../../assets/images/vt9.png')
                },
                {
                    url: require('../../assets/images/vt10.png')
                },
                {
                    url: require('../../assets/images/vt11.png')
                },
                {
                    url: require('../../assets/images/vt12.png')
                },
                {
                    url: require('../../assets/images/vt13.png')
                },
                {
                    url: require('../../assets/images/vt14.png')
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">
    @import '../../assets/styles/vars.scss';
    .mapsContainer {
        flex-wrap: wrap;
        position: relative;
        .map {
            width: calc(100% / 7);
        }
        .object {
            position: absolute;
        }
        .google {
            bottom: 0;
        }
        .position {
            right: 50%;
            top: 50%;
            transform: translate(-50%, -50%);
        }
        .visualization {
            right: 10px;
            bottom: 10px;
            text-align: center;
            .line {
                height: 1px;
                width: 60%;
                margin: auto;
                background-color: $text-color;
            }
            .zoom, .view {
                background-color: #fff;
                padding: 5px;
            }
        }
    }
</style>