<template>
    <section class="ticketsSection">
        <div class="container">
            <h2>TICKETS</h2>
            <div class="tickets d-flex">
                <a v-for="(ticket, index) in tickets" :key="index" href="#" class="ticket">
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
                    <div class="ticketFooter">
                        BOOK NOW
                    </div>
                </a>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'MyTickets',
    data() {
        return {
            tickets: [
                {
                    title: 'ONE DAY PASS',
                    price: 'FREE',
                    daysAcces: 'One',
                    discount: 50,
                    featured: false
                },
                {
                    title: 'FOUR DAY PASSES',
                    price: '750.00 USD',
                    daysAcces: 'Four',
                    discount: 100,
                    featured: true
                },
                {
                    title: 'TWO DAY PASSES',
                    price: '580.00 USD',
                    daysAcces: 'Two',
                    discount: 70,
                    featured: false
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">
    @import '../../assets/styles/vars.scss';
    .ticketsSection {
        background-image: url(../../assets/images/ticket-bg.jpg);
        padding: 90px 0;
        text-align: center;
        h2 {
            color: #fff;
            margin-bottom: 65px;
        }
        .tickets {
            justify-content: space-between;
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
                        background: red;
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
        }
    }
</style>