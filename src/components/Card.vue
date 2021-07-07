<template>
    <div class="card">
        <img :src="serie.thumb" alt="">
        <div>{{serie.series}}</div>
    </div>
</template>

<script>
export default {
    name: "Card",
    props: ["serie"]
}
</script>

<style lang="scss" scoped>
    .card {
        margin-bottom: 20px;
    }
    
    img {
        width: 150px;
        height: 150px;
        object-fit: cover;
        object-position: top;
    }
    div {
        margin-top: 10px;
        max-width: 150px;
        text-transform: uppercase;
    }
</style>