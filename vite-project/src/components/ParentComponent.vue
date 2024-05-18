<template>
  <div class="parent">
    <h1>Parent Component</h1>
    <child-component1 @send-data="receiveData"></child-component1>
    <child-component2 @send-data="receiveData"></child-component2>
    <p>Data dari child: {{ dataFromChild }}</p>
    <slot></slot>
  </div>
</template>

<script>
import ChildComponent1 from './ChildComponent1.vue';
import ChildComponent2 from './ChildComponent2.vue';

export default {
  components: {
    ChildComponent1,
    ChildComponent2
  },
  data() {
    return {
      dataFromChild: ''
    };
  },
  methods: {
    receiveData(data) {
      this.dataFromChild = data;
    }
  }
}
</script>

<style scoped>
.parent {
  border: 2px solid #42b983;
  padding: 20px;
  border-radius: 8px;
  background-color: #f9f9f9;
}

h1 {
  color: #35495e;
}

p {
  font-size: 16px;
  color: #2c3e50;
}
</style>
