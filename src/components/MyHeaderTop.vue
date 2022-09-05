<template>
    <div class="headerTop container">
        <div class="logoContainer">
            <img src="../assets/images/logo.png" alt="logo image">
        </div>
        <div class="headerMenuContainer">
            <ul class="linksList">
                <li v-for="(link, index) in links" :key="index" class="listItem">
                        <a :href="link.url">{{link.text}}</a>
                </li>
            </ul>
            <div class="search">
                <i class="fa-solid fa-magnifying-glass"></i>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'MyHeaderTop',
    props: {
        links: Array
    }
}
</script>

<style scoped lang="scss">
    @import '../assets/styles/vars.scss';
    .headerTop {
        height: 100px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        .headerMenuContainer {
            display: flex;
            .linksList {
                list-style: none;
                display: flex;
                .listItem {
                    padding: 0 1rem;
                    a {
                        text-decoration: none;
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