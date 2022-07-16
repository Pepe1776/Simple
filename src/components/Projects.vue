<template>
    <div class="projects">
        <Transition name="fade">
            <Icon style="font-size: 10rem;" class="icon meta" icon="logos:metamask-icon" />
        </Transition>
        <Transition name="fade">
            <Icon class="icon vue" icon="logos:vue" />
        </Transition>
        <Transition name="fade">
            <Icon class="icon ang" icon="logos:angular-icon" />
        </Transition>
        <Transition name="fade">
            <Icon class="icon book" icon="emojione:blue-book" />

        </Transition>

      
    </div>
</template>
<script lang="ts" setup>
import { Icon } from '@iconify/vue';
import { ref } from 'vue';
const Icon1 = ref(false);
const Icon2 = ref(false);
const Icon3 = ref(false);
const Icon4 = ref(false);


</script>
<style scoped>
@keyframes fade {
    0% {
        opacity: 0;
    }
    100% {
        opacity: 1;
    }
}
    
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
        top: 100vh;
        opacity: 0.05;
    }
    .projects {
        position: absolute;
        width: 100%;
        height: auto;
        top: 130%;
        left: 50%;
        transform: translate(-50%, -50%);
        display: flex;
        flex-direction: row;
        gap: 15rem;
        justify-content: space-evenly;
        align-items: center;
    }
    .icon {
        width: 200px;
        height: 200px;
        z-index: 2;
        opacity: 0.7;
        cursor: crosshair;
      
    }

    .icon:hover {
        transition: all 0.5s ease-in-out;        
        opacity: 1;
        transform: scale(1.1);
        
    }
</style>