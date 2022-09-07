<template>
    <section class="ticketsSection">
        <div class="container">
            <h2>TICKETS</h2>
            <div class="tickets d-flex">
                <MySingleTicket v-for="(ticket, index) in tickets" :key="index" :ticket="ticket"/>
            </div>
        </div>
    </section>
</template>

<script>

    import MySingleTicket from './MySingleTicket.vue';

export default {
    name: 'MyTickets',
    components: {
        MySingleTicket
    },
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
        }
    }
</style>