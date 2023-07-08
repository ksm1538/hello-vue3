<!-- 자식 컴포넌트(ChildComponent) -->
<template>
    <button @click="onClick">전송</button>
  </template>
  
  <script>
  export default {
    setup(props, context) {
      const childData = 'child';
      const onClick = () => {
        context.emit('alert-event', childData);
      };

      return {
        onClick
      }
    }
  }
  </script>
  
  <style></style>