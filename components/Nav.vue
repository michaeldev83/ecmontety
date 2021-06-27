<template>
    <nav>
        <div class="navBar">
            <h2>{{ titreMenu }}</h2>
        </div>
    </nav>
</template>

<script>

export default {
    name: 'Nav',
    props: ['titreMenu'],
}
</script>

<style scoped>
nav{
    position:fixed;
    top:90px;
    width:100%;
    max-width:600px;
    height:40px;
    z-index:2;
    background-color:#333;  
    margin-bottom: 20px;
}
nav .navBar{
    display:flex;
    justify-content:space-between;
    align-items: center;
    max-width:500px;
    height:40px;
    padding: 0 10px;
}
nav h2{
    font-size:14px;
    color:#f1f1f1;
    font-weight: normal;
}
</style>