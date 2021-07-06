<template>
    <header>
        <img src="../assets/img/dc-logo.png" alt="logo dc">
        <ul>
            <li>Esempio</li>
            <li>Esempio</li>
            <li>Esempio</li>
            <li>Esempio</li>
        </ul>
    </header>
</template>
    
<script>
export default {
    name: "Header"
};
</script>

<style lang="scss" scoped>
    header {
        height: 100px;
        width: 100%;
        background-color: #fff;
        display: flex;
        justify-content: center;
        align-items: center;
        img {
            height: 80%;
        }
        li {
            display: inline-block;
        }
    }
</style>
