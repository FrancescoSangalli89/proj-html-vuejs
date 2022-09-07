<template>
    <section class="jumbotron">
        <div class="item-container container d-flex">
            <div class="title">
                <h2>CONFERENCE ON</h2>
                <h1>SOCIAL NETWORKS</h1>
            </div>
            <div class="subTitle">
                <p>23-26 MAY 2019   /   SAN FRANCISCO   /   8 SPEAKERS</p>
            </div>
            <a href="#">
                <button class="header-button">REGISTER ONLINE</button>
            </a>
        </div>
    </section>
</template>

<script>
export default {
    name: 'MyJumbotron'
}
</script>

<style lang="scss">

    @import '../../assets/styles/vars.scss';

    .jumbotron {
        background-image: url('../../assets/images/slider-1-bg.jpg');
        height: 600px;
        color: #fff;
        text-align: center;
        .item-container {
            height: 100%;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            h2 {
                font-weight: 200;
                font-size: 3rem;
            }
            h1 {
                font-size: 5rem;
                margin: 2rem 0;
            }
            .subTitle {
                border-top: 3px solid #fff;
                padding-top: 1rem;
            }
            .header-button {
                margin-top: 3rem;
                padding: 1rem;
                background-color: $primary-color;
                border: none;
                border-radius: 5px;
                font-weight: 700;
                color: #fff;
                cursor: pointer;
            }
        }
    }
</style>