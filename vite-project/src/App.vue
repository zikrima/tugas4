<template>
  <div id="app">
    <h1>Welcome to the App</h1>
    <ParentComponent>
      <!-- Ini adalah konten yang akan disisipkan ke slot ParentComponent -->
      <div class="slot-content">Ini adalah konten yang dimasukkan ke dalam slot ParentComponent.</div>
    </ParentComponent>
  </div>
</template>

<script>
import ParentComponent from './components/ParentComponent.vue';

export default {
  name: 'App',
  components: {
    ParentComponent
  }
}
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

h1 {
  color: #42b983;
}

.slot-content {
  border: 1px dashed #42b983;
  padding: 10px;
  margin-top: 20px;
  background-color: #f0fff0;
}
</style>
