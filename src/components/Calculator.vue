<script setup>
import { ref } from 'vue';

const count = ref(0);


let displayValue=ref('0');
let result;
function HandleInput(value){
  switch(value){
    case "1":{
      if(displayValue.value==='0'){
        displayValue.value='1';
      }else{
        displayValue.value+=value;
      }
      break;
    }
    case "2":{
      if(displayValue.value==='0'){
        displayValue.value='2';
      }else{
        displayValue.value+=value;
      }
      break;
    }
    case "3":{
      if(displayValue.value==='0'){
        displayValue.value='3';
      }else{
        displayValue.value+=value;
      }
      break;
    }
    case "4":{
      if(displayValue.value==='0'){
        displayValue.value='4';
      }else{
        displayValue.value+=value;
      }
      break;
    }
    case "5":{
      if(displayValue.value==='0'){
        displayValue.value='5';
      }else{
        displayValue.value+=value;
      }
      break;
    }
    case "6":{
      if(displayValue.value==='0'){
        displayValue.value='6';
      }else{
        displayValue.value+=value;
      }
      break;
    }
    case "7":{
      if(displayValue.value==='0'){
        displayValue.value='7';
      }else{
        displayValue.value+=value;
      }
      break;
    }
    case "8":{
      if(displayValue.value==='0'){
        displayValue.value='8';
      }else{
        displayValue.value+=value;
      }
      break;
    }
    case "9":{
      if(displayValue.value==='0'){
        displayValue.value='9';
      }else{
        displayValue.value+=value;
      }
      break;
    }
    case "0":{
      if(displayValue.value==='0'){
        displayValue.value='0';
      }else{
        displayValue.value+=value;
      }
      break;
    }
    case "+":{
      if(displayValue.value==='0'){
        displayValue.value='+';
      }else{
        displayValue.value+=value;
      }
      break;
    }
    case "*":{
        if(displayValue.value==='0'){
        displayValue.value='+';
      }else{
        displayValue.value+=value;
      }
      break;
    }
    case "/":{
      if(displayValue.value === "0"){
        displayValue.value = '/';
      }
      else{
        displayValue.value += value;

      }
      break;
    }
    case "=":{
      
      result = displayValue.value;
      result = eval(result);
      console.log(result)
      displayValue.value = result;
    }
    case "back":{
displayValue.value =  displayValue.value.slice(0,-1);

break;
    }
    
  }
}
</script>

<template>
  <div class="calculator">
    <div class="calculator-display">
      <input
        type="text"
     :value=displayValue
        class="calculator-display-input"
        readonly
      />
    </div>

    <div class="calculator-button">
      <button @click="HandleInput('1')" >1</button>
       <!-- <button>{{ count}}</button> -->
      <button @click="HandleInput('2')" >2</button>
      <button @click="HandleInput('3')">3</button>
      <button @click ="HandleInput('/')">/</button>
      <button @click="HandleInput('4')">4</button>
      <button @click="HandleInput('5')">5</button>
      <button @click="HandleInput('6')">6</button>
      <button @click="HandleInput('*')">X</button>
      <button @click="HandleInput('7')">7</button>
      <button @click="HandleInput('8')">8</button>
      <button @click="HandleInput('9')">9</button>
      <button @click="HandleInput('+')">+</button>
      <button @click="HandleInput('.')">.</button>
      <button @click="HandleInput('0')">0</button>
      <button @click="HandleInput('back')"><i class="ri-arrow-left-line"></i></button>
      <button @click="HandleInput('=')">=</button>
    </div>
  </div>
</template>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-size: 62.5%;
}
.calculator {
  height: 65vh;
  width: 20vw;
  background-color: #333132;
  overflow: hidden;
  border-radius: 1rem;
}
.calculator-display {
  width: 100%;
  height: 30%;
  display: flex;
  align-items: flex-end;
}
.calculator-display-input {
  border: none;
  height: 80%;
  width: 100%;
  text-align: right;
  color: white;
  font-size: 3rem;
  padding: 1rem 2rem;;
  background-color: transparent;
  outline: none;
}
.calculator-button {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 0.5rem;
  height: 70%;
  padding: 1rem;
}
.calculator-button button {
  height: 100%;
  width: 100%;
  color: white;
  background-color: #1b464d;
  border: none;
  outline: none;
  font-size: 4em;
  border-radius: 1rem;
}
.calculator-button button:hover {
  background-color: #f7941d;
  cursor: pointer;
}
</style>
