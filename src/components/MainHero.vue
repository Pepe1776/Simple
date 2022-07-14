<template>
    <div>
        <Transition name="fade">
            <img src="../assets/hero.jpeg" alt="hero" />
        </Transition>
        <div class="black"></div>
        <Transition name="fade">
            <img class="float" src="../assets/121212.png" alt="hero" />
        </Transition>
        <router-link to="/">
            <img src="../assets/Satoshi-logo.png" alt="Satoshi logo" class="logo" />
        </router-link>
        <router-link class="call pulse">
Hire Me
        </router-link>
    </div>
</template>
<script lang="ts" setup>

</script>
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Rubik+Moonrocks&display=swap');

.fade-enter-active,
.fade-leave-active {
    transition: opacity 5s ease;
}

.fade-enter-from,
.fade-leave-to {
    opacity: 0;
}
    img {
        width: 100vw;
        height: 100vh;
        position: absolute;
        inset: 0;
        opacity: 0.1;
    }
    .black {
        background-color: #000000;
        width: 100vw;
        height: 100vh;
        position: absolute;
        inset: 0;
        top: 100vh;
        opacity: 0.5;
    }
    .logo {
        width: 300px;
        height: auto;
        position: absolute;
        top: 3%;
        left: 3%;
        z-index: 2;
        opacity: 0.8;
        cursor: crosshair;
    }
    .float {
        display: none;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        z-index: 3;
        opacity: 1;
        width: 500px;
        height: auto;
        border-radius: 50%;
    }
    .call {
        position: absolute;
        top: 88%;
        left: 50%;
        transform: translate(-50%, -50%);
        z-index: 2;
        opacity: 0.8;
        cursor: crosshair;
        font-size: 9rem;
        color: rgba(51, 255, 0, 0.666);
        width: auto;
        height: 300px;
        text-align: center;
        display: flex;
        justify-content: center;
        align-items: center;
        font-family: 'Rubik Moonrocks', cursive;
    }
        .pulse {
            animation: pulse 5s infinite;
            cursor: pointer;
            color: rgba(51, 255, 0, 0.666);
           
        }
    
        .pulse:hover {
            animation: none;
        }
    
    
        @keyframes pulse {
            0% {
                    color: rgba(51, 255, 0, 0);
                }
            
                50% {
                    color: rgba(51, 255, 0, 0.256);
                }
            
                100% {
                    -color: rgba(51, 255, 0, 0.666);
                }
                50% {
                    color: rgba(51, 255, 0, 0.256);
                }
                0% {
                    color: rgba(51, 255, 0, 0);
                }
        }

</style>