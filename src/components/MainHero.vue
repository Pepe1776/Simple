<template>
    <div>
        <Transition name="fade" appear>
            <img v-if="action6" class="pulse2" src="../assets/hero.jpeg" alt="hero" />
        </Transition>
        <div class="black"></div>
        <div class="black0"></div>
        <Transition name="fade" appear>
            <img class="float" src="../assets/121212.png" alt="hero" />
        </Transition> 
            <button v-if="action2" class="btn2" @click="Play(), action2 = !action2">Jump into the future!</button>
        <Transition name="fade" appear>
            <p id="action1" class="action1 pulse" v-if="action1">Simulation is rendering .....</p>
        </Transition>
        <Transition name="fade" appear>
            <p id="action1" class="action2" v-if="action3">Welcome to the Future <br> of we do business online</p>
        </Transition>
        <Transition name="fade" appear>
            <img class="img-action" v-if="action5" src="../assets/web3_primer_1.gif" alt="web3_primer_1">
        </Transition>
        <Transition name="fade" appear>
            <p id="action1" class="action2" v-if="action4">We are a team of experts in the field of digitalization</p>
        </Transition>
        <router-link to="/">
            <img src="../assets/Satoshi-logo-bw.png" alt="Satoshi logo" class="logo" />
        </router-link>
        <router-link id="call" class="call">
            Hire Me
        </router-link>
    </div>
</template>
<script lang="ts" setup>
import { Transition } from "vue";
import { ref } from "vue";

const action1 = ref(false);
const action2 = ref(true);
const action3 = ref(false);
const action4 = ref(false);
const action5 = ref(false);
const action6 = ref(true);
function Play() {
    setTimeout(() => {
        action1.value = true;
    }, 1000);
    setTimeout(() => {
        action6.value = false;
    }, 500);
    setTimeout(() => {
        action1.value = false;
    }, 5000);

    setTimeout(() => {
        action3.value = true;
    }, 7000);

    setTimeout(() => {
        action5.value = true;
    }, 7000);
    setTimeout(() => {
        action5.value = false;
    }, 17000);

    setTimeout(() => {
        action3.value = false;
    }, 11000);
    setTimeout(() => {
        action4.value = true;
    }, 13000);
    setTimeout(() => {
        action4.value = false;
    }, 17000);
}
</script>
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Rubik+Moonrocks&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans:ital,wght@1,100;1,400;1,900&display=swap');

.fade-enter-active,
.fade-leave-active {
    transition: opacity 0.7s ease;
}

.fade-enter-from,
.fade-leave-to {
    opacity: 0;
}

.slide-fade-enter-active {
    transition: all 0.3s ease-out;
}

.slide-fade-leave-active {
    transition: all 0.8s cubic-bezier(1, 0.5, 0.8, 1);
}

.slide-fade-enter-from,
.slide-fade-leave-to {
    transform: translateX(20px);
    opacity: 0;
}

    img {
        width: 100vw;
        height: 100vh;
        position: absolute;
        inset: 0;
        opacity: 0.2;
        z-index: 3;
        curser: none;
    }
    .img-action {
        opacity: 0.2;
    }
        .btn2 {
            font-family: 'Noto Sans', sans-serif;
            font-weight: 900;
            color: rgba(0, 204, 255, 0.607);
            height: 200px;
            width: auto;
            font-size: 5rem;
            cursor: crosshair;
            z-index: 7;
            padding: 50px;
            left:28%;
            top: 75%;
            border-radius: 10px;
            display: flex;
            justify-content: center;
            align-items: center;
            position: absolute;
            background: transparent;
            border: 1px solid rgba(0, 204, 255, 0.607);
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
    .black0 {
        background-color: #000000;
        width: 100vw;
        height: 400vh;
        position: absolute;
        inset: 0;
        top: 0;

    }
    .logo {
        width: 300px;
        height: auto;
        position: fixed;
        top: 3%;
        left: 3%;
        z-index: 5;
        opacity: 0.6;
        cursor: crosshair;
    }
    .logo:hover {
        transition: all 0.5s ease-in-out;
        opacity: 1;
        transform: scale(1.1);
       
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
    #call {
        position: absolute;
        top: 378%;
        left: 40%;
        z-index: 5;
        opacity: 0.6;
        font-size: 9rem;
        color: rgba(0, 204, 255, 0.607);
        width: auto;
        height: 300px;
        text-align: center;
        display: flex;
        justify-content: center;
        align-items: center;
        font-family: 'Rubik Moonrocks', cursive;
        transition: all 0.5s ease-in-out;
    }
         #call:hover {
             opacity: 1;
             transform: scale(1.1);
             color: rgba(0, 204, 255, 0.607);
         }
         .action1 {
             position: absolute;
             top: 50%;
             left: 25%;
             transform: translate(-50%, -50%);
             z-index: 3;
             opacity: 1;
             width: 50%;
             height: auto;
             font-size: 5rem;
             color: rgba(0, 204, 255, 0.607);
            font-family: 'Noto Sans', sans-serif;
            font-weight: 900;
             transition: all 0.5s ease-in-out;
             
         }
         .action2 {
             position: absolute;
             top: 50%;
             left: 50%;
             transform: translate(-50%, -50%);
             z-index: 3;
             opacity: 1;
             width: 100%;
             height: 100%;
             line-height: normal;
             font-size: 7rem;
             color: rgba(0, 204, 255, 0.607);
             font-family: 'Noto Sans', sans-serif;
             font-weight: 900;
             justify-content: center;
             align-items: center;
             display: flex;
             text-shadow: #000000 0px 0px 20px;
             transition: all 0.5s ease-in-out;
         }
        .pulse {
            animation-name: stretch;
                animation-duration: 1.5s;
                animation-timing-function: ease-in-out;
                animation-delay: 0;
                animation-direction: alternate;
                animation-iteration-count: infinite;
                animation-fill-mode: none;
                animation-play-state: running;
            cursor: pointer;
            color: rgba(0, 204, 255, 0.607);}
        .pulse2 {
            animation-name: stretch;
                animation-duration: 15s;
                animation-timing-function: ease-out;
                animation-delay: 0;
                animation-direction: alternate;
                animation-iteration-count: infinite;
                animation-fill-mode: none;
                animation-play-state: running;
            cursor: pointer;
            color: rgba(0, 204, 255, 0.607);
           
        }

   
       
    
    
        @keyframes pulse {
            0% {
                    color: rgba(51, 255, 0, 0);
                    opacity: 0;
                }
            
                100% {
                    color: rgba(0, 204, 255, 0.607);
                    opacity: 1;
                }
               
        }
        @keyframes pulse2 {
            0% {
                    
                    opacity: 0;
                }
            
                100% {
                 
                    opacity: 1;
                }
               
        }
                @keyframes stretch {
                    0% {
                        transform: scale(.6);
                        color: rgba(51, 255, 0, 0);;
                        border-radius: 100%;
                    }
        
                    50% {
                        color: rgba(6, 142, 176, 0.607);
                    }
        
                    100% {
                        transform: scale(1);
                        color: rgba(0, 204, 255, 0.607);
                    }
                }

</style>