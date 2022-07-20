<template>
    <div>
        <Transition name="fade" appear>
            <video autoplay v-if="action6" src="../assets/mapvid.mp4" class="vid pulse2" />
        </Transition>
        <Transition name="fade" appear>
            <video autoplay v-if="action7" src="../assets/codevid.mp4" class="vid2" />
        </Transition>
        <div class="black"></div>
        <div class="black0"></div>
        <Transition name="fade" appear>
            <img class="float" src="../assets/Apple_Watch_R Shadowless.png" alt="hero" />
        </Transition> 
            <button v-if="action2" class="btn2" @click="Play(), action2 = !action2">Jump into the future!</button>
        <Transition name="fade" appear>
            <p id="action1" class="action1 pulse" v-if="action1">Simulation is rendering .....</p>
        </Transition>
        <Transition name="fade" appear>
            <p id="action1" class="action2" v-if="action3">Welcome to the Future <br> of how we do business online</p>
        </Transition>
        <Transition name="fade" appear>
            
        </Transition>
        <Transition name="fade" appear>
            <p id="action1" class="action2" v-if="action4">We are experts in <br> the field of digitalization</p>
        </Transition>
        <Transition name="fade" appear>
            <p id="action1" class="action2" v-if="action8">Let us build you a <br> custom tailored website </p>
        </Transition>
        <Transition name="fade" appear>
            <p id="action1" class="action2" v-if="action9">Bring in new customers <br> while building your brand </p>
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
const action7 = ref(false);
const action8 = ref(false);
const action9 = ref(false);
const action10 = ref(false);
function Play() {
    setTimeout(() => {
        action1.value = true;
    }, 1000);
    setTimeout(() => {
        action6.value = false;
    }, 11500);
    setTimeout(() => {
        action7.value = true;
    }, 12500);
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
    setTimeout(() => {
        action8.value = true;
    }, 17500);
    setTimeout(() => {
        action8.value = false;
    }, 25000);
    setTimeout(() => {
        action9.value = true;
    }, 25500);
    setTimeout(() => {
        action9.value = false;
    }, 32000);
    setTimeout(() => {
        action10.value = true;
    }, 32500);
    setTimeout(() => {
        action10.value = false;
    }, 40000);
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
    .vid {
            width: 100vw;
                height: 100vh;
                position: absolute;
                inset: 0;
                opacity: 0.5;
                z-index: 3;
                curser: none;
                object-fit: fill;
    }
    .vid2 {
            width: 100vw;
                height: 100vh;
                position: absolute;
                inset: 0;
                opacity: 0.5;
                z-index: 3;
                curser: none;
                object-fit: fill;
                filter: opacity(0.3);
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
            left:33%;
            top: 77%;
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
             color: rgb(0, 204, 255);
             font-family: 'Noto Sans', sans-serif;
             font-weight: 900;
             justify-content: center;
             align-items: center;
             display: flex;
             text-shadow: #000000 0px 0px 30px;
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
                        transform: scale(1);
                        color: rgba(51, 255, 0, 0);;
                        border-radius: 100%;
                    }
        
                    50% {
                        color: rgba(6, 142, 176, 0.607);
                    }
        
                    100% {
                        transform: scale(1.3);
                        color: rgba(0, 204, 255, 0.607);
                    }
                }

</style>