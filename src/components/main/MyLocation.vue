<template>
    <section class="location">
        <div class="container">
            <h2>LOCATION</h2>
            <h3>GD BUILDING, GRAND CONFERENCE ROOM</h3>
            <div class="address">
                <i class="fa-solid fa-location-arrow"></i>
                <span>11 GD Building, River Mall, New york, USA 8879</span>
            </div>
            <a href="#">Check For the accomodations Here</a>
            <span class="contacts">
                <span class="phone">
                    <i class="fa-solid fa-phone"></i>
                    <span>+1-112-222-3344</span>
                </span>
                <span class="mail">
                    <i class="fa-solid fa-envelope"></i>
                    <span>Contact@TheKeynoteTheme.com</span>
                </span>
            </span>
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
        background-position: center;
        text-align: center;
        padding: 100px 0;
        color: #fff;
        h2 {
            margin-bottom: 55px;
        }
        h3 {
            margin-bottom: 15px;
        }
        .address {
            margin-bottom: 25px;
            i {
                margin-right: 10px;
            }
        }
        a {
            color: $primary-color;
            display: block;
            margin-bottom: 50px;
        }
        .contacts {
            padding-top: 10px;
            border-top: solid 3px;
            i {
                margin-right: 10px;
            }
            .phone {
                margin-right: 20px;
            }
        }
    }
</style>