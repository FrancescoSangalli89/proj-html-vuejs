<template>
    <section class="updates">
        <div class="container">
            <div class="timeCards d-flex">
                <div class="timeCard d-flex">
                    <div class="numbers">{{days}}</div>
                    <div class="timeUnit">DAYS</div>
                </div>
                <div class="timeCard d-flex">
                    <div class="numbers">{{hours}}</div>
                    <div class="timeUnit">HOURS</div>
                </div>
                <div class="timeCard d-flex">
                    <div class="numbers">{{mins}}</div>
                    <div class="timeUnit">MINS</div>
                </div>
                <div class="timeCard d-flex">
                    <div class="numbers">{{secs}}</div>
                    <div class="timeUnit">SECS</div>
                </div>
            </div>
            <h3>SUBSCRIBE FOR UPDATES</h3>
            <form action="">
                <input type="email" placeholder="Please fill your email">
                <button>SUBSCRIBE</button>
            </form>
        </div>
    </section>
</template>

<script>
export default {
    name: 'MyUpdates',
    data() {
        return {
            countdown: '',
            secs: 60,
            mins: 59,
            hours: 23,
            days: 364
        }
    },
    watch: {
        secs: {
            handler(value) {
                if (value >= 0) {
                    setTimeout(() => {
                        this.secs--;
                    }, 1000);
                } else {
                    this.secs = 59;
                }
                if (value == 0) {
                    this.mins--;
                }
                if (this.mins == 0) {
                    this.mins = 59;
                    this.hours--;
                }
                if (this.hours == 0) {
                    this.hours = 23;
                    this.days--;
                }
            },
            immediate: true
        }
    },
}
</script>

<style scoped lang="scss">
    @import '../../assets/styles/vars.scss';
    .updates {
        padding: 100px 0;
        text-align: center;
        background-image: url('../../assets/images/coutdown-bg1.jpg');
        max-height: 500px;
        .timeCards {
            justify-content: center;
            .timeCard {
                flex-direction: column;
                justify-content: center;
                margin: 0 10px;
                min-width: 145px;
                height: 140px;
                color: #fff;
                border-radius: 5px;
                background-color: rgba($color: #000000, $alpha: 0.5);
                .numbers {
                    font-size: 50px;
                    font-weight: 600;
                }
            }
        }
        h3 {
            margin: 40px 0;
        }
        input {
            margin-right: 5px;
            padding: 10px;
            width: 400px;
            border: none;
        }
        button {
            cursor: pointer;
            padding: 10px;
            background-color: $primary-color;
            color: #fff;
            border: none;
            border-bottom: 2px solid $primary-color-hover;
            font-weight: 600;
        }
    }
</style>