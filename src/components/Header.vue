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
import navLi from "@/data/HeaderNavLi.js"
export default {
    name: "Header",
    data() {
        return {
            navLi: navLi
        }
    }
};
</script>

<style lang="scss" scoped>
    @import "../style/vars.scss";
    header {
        background-color: #fff;
        font-size: 17px;
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
