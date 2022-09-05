<template>
    <section class="headerTop container d-flex">
        <div class="logoContainer">
            <img src="../../assets/images/logo.png" alt="logo image">
        </div>
        <div class="headerMenuContainer d-flex">
            <ul class="linksList d-flex">
                <li v-for="(link, index) in links" :key="index" class="listItem">
                        <a :href="link.url">{{link.text}}</a>
                </li>
            </ul>
            <div class="search">
                <i class="fa-solid fa-magnifying-glass"></i>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'MyHeaderTop',
    data() {
        return {
            links: [
                {
                    text: 'HOME',
                    url: '#',
                    active: false
                },
                {
                    text: 'PAGES',
                    url: '#',
                    active: false
                },
                {
                    text: 'PROGRAM',
                    url: '#',
                    active: false
                },
                {
                    text: 'TICKETS',
                    url: '#',
                    active: false
                },
                {
                    text: 'SPEAKERS',
                    url: '#',
                    active: false
                },
                {
                    text: 'PAPERS',
                    url: '#',
                    active: false
                },
                {
                    text: 'BLOG',
                    url: '#',
                    active: false
                },
                {
                    text: 'SHORTCODES',
                    url: '#',
                    active: false
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
    @import '../../assets/styles/vars.scss';
    .headerTop {
        height: 100px;
        justify-content: space-between;
        align-items: center;
        .headerMenuContainer {
            .linksList {
                .listItem {
                    padding: 0 1rem;
                    a {
                        color: $text-color;
                        padding-bottom: 0.8rem;
                        
                        &:hover {
                            color: $primary-color;
                            border-bottom: 2px solid $primary-color;
                        }
                    }
                }
            }
            .search {
                border-left: 2px solid $text-color;
                color: $text-color;
                padding: 0 1rem;
                margin-left: 1rem;
                &:hover {
                    cursor: pointer;
                }
            }
        }
    }
</style>