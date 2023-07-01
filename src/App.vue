<template>
  <div>{{ name1 }}</div>
  <div>{{ name2 }}</div>
  <button 
    class="btn btn-primary"
    v-on:click="updateName"
  >
    이름 변경
  </button>
</template>

<script>
import { ref, reactive } from 'vue';

export default {
  setup() {
    let name1 = ref('Iron Man 1');	// ref
    let name2 = reactive({'name': 'Iron Man 2'}); // reactive
    const updateName = () => {
      name1.value = 'Dr.Strange 1'; // ref update
      name2.name = 'Dr.Strange 2'; // reactive update
    };
    
    return {
      name1,
      name2,
      updateName
    };
  }
}
</script>