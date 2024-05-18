<template>
  <div class="child">
    <h2>Child Component 2</h2>
    <button @click="sendData">Kirim Data ke Parent</button>
  </div>
</template>

<script>
export default {
  methods: {
    sendData() {
      this.$emit('send-data', 'Data dari Child 2');
    }
  }
}
</script>

<style scoped>
.child {
  border: 2px solid #6b5b95;
  padding: 10px;
  border-radius: 8px;
  background-color: #ececff;
  margin: 10px 0;
}

h2 {
  color: #6b5b95;
}

button {
  background-color: #6b5b95;
  color: white;
  border: none;
  padding: 10px 20px;
  border-radius: 4px;
  cursor: pointer;
}

button:hover {
  background-color: #574a8a;
}
</style>
