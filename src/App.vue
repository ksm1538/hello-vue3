<!-- 부모 컴포넌트 -->
<template>
  <div>
    <ChildComponent :parentData="myData" />
  </div>
</template>

<script>
import ChildComponent from './components/ChildComponent.vue';

export default {
components: {
  ChildComponent
},
setup() {
  const myData = "hi";
  
  return {
    myData
  };
}
}
</script>