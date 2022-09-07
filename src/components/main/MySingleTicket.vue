<template>
    <a href="#" class="ticket">
        <div class="ticketHeader">
            <h4>{{ticket.title}}</h4>
            <div>{{ticket.price}}</div>
            <div class="trapezoid" :class="ticket.featured?'stickyOn':'stickyOff'">Featured!</div>
        </div>
        <div class="ticketMain">
            <div>{{ticket.daysAcces}} Day Access</div>
            <div>Coffee Break</div>
            <div>Lunch(International Buffet)</div>
            <div>Documents Sheets</div>
            <div>{{ticket.discount}}USD Voucher For Next Event</div>
        </div>
        <div class="ticketFooter">BOOK NOW</div>
    </a>
</template>

<script>
export default {
    name: 'MySingleTicket',
    props: {
        ticket: Object
    }
}
</script>

<style scoped lang="scss">
    @import '../../assets/styles/vars.scss';
    .ticket {
        width: calc(100% / 3 - 20px);
        .ticketHeader {
            background-color: $section-background;
            padding: 20px;
            position: relative;
            h4 {
                color: #000;
            }
            div {
                margin-top: 10px;
                color: $primary-color;
            }
            .trapezoid {
                line-height: 30px;
                color: #fff;
                position: absolute;
                width: 80px;
                height: 30px;
                background: $primary-color;
                transform: perspective(20px) rotateX(27deg);
                rotate: 45deg;
                margin: 50px;
                top: -37px;
                right: -62px;
            }
        }
        .ticketMain {
            background-color: #fff;
            padding: 20px 40px;
            div {
                margin: 20px 0;
                color: $text-color;
                font-style: italic;
            }
        }
        .ticketFooter {
            background-color: $primary-color;
            color: #fff;
            padding: 20px;
        }
    }
    .ticket {

    }
</style>