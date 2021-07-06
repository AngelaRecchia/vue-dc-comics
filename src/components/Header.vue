<template>
    <header>
        <div class="container">
            <img src="../assets/img/dc-logo.png" alt="logo dc">
            <ul>
                <li v-for="(item, index) in navLi" :key="index" :class="{active : item.current}"><a href="item.link">{{item.text}}</a></li>
            </ul>
        </div>
    </header>
</template>
    
<script>
export default {
    name: "Header",
    data() {
        return {
            navLi: [
                {
                    text: "Characters",
                    link: "#",
                    current: false
                },
                {
                    text: "Comics",
                    link: "#",
                    current: true
                },
                {
                    text: "Movies",
                    link: "#",
                    current: false
                },
                {
                    text: "Tv",
                    link: "#",
                    current: false
                },
                {
                    text: "Games",
                    link: "#",
                    current: false
                },
                {
                    text: "Collectibles",
                    link: "#",
                    current: false
                },
                {
                    text: "Videos",
                    link: "#",
                    current: false
                },
                {
                    text: "Fans",
                    link: "#",
                    current: false
                },
                {
                    text: "News",
                    link: "#",
                    current: false
                },
                {
                    text: "Shop",
                    link: "#",
                    current: false
                }
            ]
        }
    }
};
</script>

<style lang="scss" scoped>
    @import "../style/vars.scss";
    header {
        background-color: #fff;
        .container {
            height: 100px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            img {
                height: 70%;
            }
            ul {
                flex-grow: 1;
                text-align: right;
                line-height: 95px;
                li {
                    display: inline-block;
                    text-transform: uppercase;
                    font-weight: bold;
                    color: grey;
                    margin: 0 2%;
                    &:hover {
                        color: $blue;
                    }
                }
                .active {
                    color: $blue;
                    border-bottom: 5px solid $blue;
                }
            }
                     
        }                
    }
</style>
