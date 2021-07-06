<template>
    <header>
        <div class="container">
            <img src="../assets/img/dc-logo.png" alt="logo dc">
            <ul>
                <li>Esempio</li>
                <li>Esempio</li>
                <li>Esempio</li>
                <li>Esempio</li>
            </ul>
        </div>
    </header>
</template>
    
<script>
export default {
    name: "Header"
};
</script>

<style lang="scss" scoped>
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
            li {
                display: inline-block;
            }
            
        }
        
    }
</style>
