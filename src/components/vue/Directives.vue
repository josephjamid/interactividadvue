<script setup>
import {ref} from 'vue';

const isChecked = ref(true)
const users = ["pepe", "ana", "juana", "mariana"]
</script>
<template>
    <ul>
        <li v-for="(user, index) in users"  :key="index" > {{ index }}  {{ user }}</li>
    </ul>

    <input type="checkbox" id="check" v-model="isChecked"/>
    <label for="check">pinchame</label>

    <div class="bg-blue-200  text-white rounded py-1 px-2 w-40" :class="{'bg-orange-500' :isChecked}">
        este es un mensaje
    </div>

    <div  v-show="isChecked">
        este es un mensaje que podria ocultar
    </div>
    <div  v-if="isChecked">
        este es un mensaje que podria ocultar
    </div>
    <div v-else>
        esto se ve porque no cumplio la concdicion del if
    </div>





</template>
    