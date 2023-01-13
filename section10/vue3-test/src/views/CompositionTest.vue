<template>
  <div>
    CompositionTest
    <p>{{ name }}</p>
    <p>{{ age }}</p>
    <p>{{ nameRef }}</p>
  </div>
</template>

<script>
import { ref } from 'vue';

export default {
  setup() {
    let name = '大谷';
    const age = 30;

    const nameRef = ref('錦織');

    console.log('setup');
    console.log(this);
    console.log(nameRef);
    console.log(nameRef.value);

    return {
      name,
      age,
      nameRef,
    }
  },
  data() {
    return {
      number: 1,
      sports: 'サッカー',
    }
  },
  created() {
    console.log('created');
    console.log(this);
  },
  mounted() {
    console.log('mounted');
  }
}
</script>

<style>

</style>
