<template>
  <div>{{ name1 }}</div>
  <div>{{ name2 }}</div>
  <button 
    class="btn btn-primary"
    v-on:click="updateName"
  >
    이름 변경
  </button>

  <br/><br/>
  {{ bindTest }}
  <input type="text" v-bind:value="bindTest"/>
  <button 
    class="btn btn-primary"
    v-on:click="updateBindTest"
  >
  값 변경
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
    
    let bindTest = ref("binding");
    const updateBindTest = () => {
      bindTest.value = "changedBinding"
    }
    return {
      name1,
      name2,
      updateName,
      bindTest,
      updateBindTest
    };
  }
}
</script>