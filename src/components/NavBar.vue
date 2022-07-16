<template>
    <div class="navbar">
        <router-link class="btn projects">Projects</router-link>
        <router-link class="btn design">Designs</router-link>
        <router-link class="btn contact">Contact Me</router-link>
        
    </div>
</template>
<script lang="ts" setup>

</script>
<style >
@import url('https://fonts.googleapis.com/css2?family=Rubik+Moonrocks&display=swap');
    .navbar {
        width: 100%;
        position: absolute;
        inset: 0;
        display: flex;
        justify-content: flex-end;
        align-items: flex-start;
        gap: 10rem;
        background-color: #00000044;
       
        
    }
    .btn {
        font-family: 'Rubik Moonrocks', cursive;
        color: rgba(51, 255, 0, 0.453);
        margin-top: 5%;
        margin-right: 10rem;
        height: 100px;
        width: auto;
        font-size: 3rem;
        cursor: crosshair;
        z-index: 5;
        padding: 10px;
        border-radius: 10px;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .btn:hover {
        transition: all 0.5s ease-in-out;
        opacity: 1;
        transform: scale(1.1);
        color: rgba(51, 255, 0, 0.544);
        box-shadow: 0 0 10px #2dff03;
    }
    router-link {
        cursor: crosshair;
    }
</style>