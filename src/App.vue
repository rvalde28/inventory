<template>
  <div>
    <button @click="showSecondComponent">Show Second Component</button>
    <!-- Conditional rendering based on a boolean value -->
    <FirstComponent v-if="!showSecond"></FirstComponent>
    <CameraScannel v-if="showSecond"></CameraScannel>
  </div>
</template>

<script>
import CameraScannel from './components/CameraScanner.vue';
import FirstComponent from './components/first.vue'
const decodedText = false;


const showSecondComponent = () => {
  this.showSecond = true;
};

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>