<template>
    <section class="location">
        <div class="container">
            <h2>LOCATION</h2>
            <h3>GD BUILDING, GRAND CONFERENCE ROOM</h3>
            <div>
                <i class="fa-solid fa-location-arrow"></i>
                <span>11 GD Building, River Mall, New york, USA 8879</span>
            </div>
            <a href="#">Check For the accomodations Here</a>
            <div>
                <span>
                    <i class="fa-solid fa-phone"></i>
                    <span>+1-112-222-3344</span>
                </span>
                <span>
                    <i class="fa-solid fa-envelope"></i>
                    <span>Contact@TheKeynoteTheme.com</span>
                </span>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'MyLocation'
}
</script>

<style scoped lang="scss">
    @import '../../assets/styles/vars.scss';
    .location {
        background-image: url(../../assets/images/location-bg.jpg);
        height: 300px;
        text-align: center;
        padding: 100px 0;
        color: #fff;
        h2 {
            margin-bottom: 55px;
        }
    }
</style>