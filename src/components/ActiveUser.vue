<template>
  <h2>
    <strong>Name:</strong>
    {{ name }}
  </h2>
  <h3>
    <strong>Age:</strong>
    {{ age }}
  </h3>
</template>

<script>
export default {
  props: ['id', 'name' , 'age'],
  data() {
    return {
      
    };
  }
};
</script>
