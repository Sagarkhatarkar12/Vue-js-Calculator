<script setup>
import Calculator from './components/Calculator.vue';
import { ref } from 'vue';
// in this count value static in this if give that not chane 
// const count = 0;
// if we want to change the value of count we need to use ref
const count = ref(0);
</script>

<template>
    <div class="center">
 <Calculator/>
    </div>
    
</template>

<style scoped>
.center{
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  width: 100vw;
}
</style>
