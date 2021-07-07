<template>
    <main>
        <div class="container">
            <a href="#"><div id="btn-current">Current Series</div></a>

            <div id="cards">

                <Card v-for="(serie, index) in series" :key="index" :serie="serie"/>

            </div>

            <div class="btn-wrap">
                <a href="#"><div id="btn-load">Load More</div></a>
            </div>

            
        </div>
    </main>
</template>

<script>
import Series from "@/data/Series.js";
import Card from "@/components/Card.vue";
export default {
    name: "Content",
    data() {
        return {
            series: Series,
        }
    },
    components: {
        Card,
    }
    
};
</script>

<style lang="scss" scoped>
@import "../style/vars.scss";
@import "../style/mixins.scss";
    main {
        background-color: black;
        color: white;
        #btn-current {
                    @include btn($blue, 28px, 5px 30px);
                    transform: translateY(-50%);
        };
        .btn-wrap {
            width: 100%;
        }
        #btn-load {
                    @include btn($blue, 16px, 5px 60px);
                    margin: auto;
        };
        #cards {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
        }        
    }
</style>
