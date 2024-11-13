<template>
    <div class="container_header">
        <div class="header">
            <h3>Home</h3>
            <h3>Sobrer</h3>
            <h3>Contato</h3>
            <h3>Portifolio</h3>
     
        </div>
    </div>
    
</template>

<script>
    export default {
        name: 'TheHeader'
    }
</script>


<style>
    .container_header{
        width: 100%;
        display: flex;
        flex-direction: column;
    }
    .header{
        height: 100px;
        background-color: #351c99;
        display: flex;
        flex-direction: row;
        gap: 50px;
        justify-content: center;
        align-items: center;
        color: #ffffff;

    }
</style>