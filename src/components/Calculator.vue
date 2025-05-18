<script scoped>

</script>

<template>
<div class="calculator">
    <div class="calculator-display">
  <input type="text" value="3939" class="calculator-display-input" readonly>

    </div>
    <div class="calculator-button">
      <button>1</button>
      <button>2</button>
      <button>3</button>
      <button>/</button>
      <button>4</button>
      <button>5</button>
      <button>6</button>
      <button>X</button>

      <button>7</button>
      <button>8</button>
      <button>9</button>
      <button>+</button>

      <button>.</button>
      <button>0</button>
      <button>0</button>
      <button>=</button>


    </div>

</div>
</template>
<style scoped>
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-size: 62.5%;
}
.calculator{
  height: 60vh;
  width: 20vw;
  background-color:#333132;
  overflow: hidden;
  border-radius: 1rem;
}
.calculator-display{
  width: 100%;
  height: 30%;
  display: flex;
  align-items: flex-end;
}
.calculator-display-input{
  border: none;
  height: 80%;
  width: 100%;
  text-align: right;
  color: white;
  font-size: 3rem;
background-color: transparent;
  outline: none;
}
.calculator-button{
  display: grid;
  grid-template-columns:repeat(4,1fr);

 
  gap: 0.5rem;
  height: 70%;
  padding: 1rem;
  /* grid-template-rows: 2rem; */
  

  /* grid-template-rows: repeat(4,2fr); */

}
.calculator-button button{
  height: 100%;
  width: 100%;
  color:white;
  background-color: #1b464d;
  border: none;
  outline: none;
  font-size: 4em;
   border-radius: 1rem;
}
.calculator-button button:hover{
  background-color: #f7941d;
  

  cursor: pointer;
}
</style>
