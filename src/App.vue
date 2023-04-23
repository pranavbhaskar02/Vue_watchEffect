<script setup>
  import {ref, watchEffect} from 'vue';

  const inputText = ref('');
  const updatedText = ref(); //comment this before using the below statement for console log
  //const updatedText = ref('Sample watchEffect Vue 3: Component API');
  //use the above statement only for console log and uncomment it for use and 
  watchEffect(() => {
    if (inputText.value === ''){
      updatedText.value = 'Sample watchEffect Vue 3: Component API';
      //uncomment below to check what happens in the console
      //console.log(updatedText.value)   
    }else {
      updatedText.value = inputText.value;
      //uncomment below to check what happens in the console
      //console.log(inputText.value)
    }
  })
</script>

<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <br><br>
  <input type="text" placeholder="Enter text" v-model="inputText">
  <br>
  <span style="color: gray;">Enter the text above to observe changes below</span>
  <br>
  <h2>{{ updatedText }}</h2>
</template>



<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

input{
  width: 20%;
  padding: 20px;
  font-size: 1.2rem;
  border-radius: 10px;
}
</style>
