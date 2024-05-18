<template>
  <div class="child">
    <h2>Child Component 1</h2>
    <button @click="sendData">Kirim Data ke Parent</button>
  </div>
</template>

<script>
export default {
  methods: {
    sendData() {
      this.$emit('send-data', 'Data dari Child 1');
    }
  }
}
</script>

<style scoped>
.child {
  border: 2px solid #ff6b6b;
  padding: 10px;
  border-radius: 8px;
  background-color: #ffecec;
  margin: 10px 0;
}

h2 {
  color: #ff6b6b;
}

button {
  background-color: #ff6b6b;
  color: white;
  border: none;
  padding: 10px 20px;
  border-radius: 4px;
  cursor: pointer;
}

button:hover {
  background-color: #ff5252;
}
</style>
