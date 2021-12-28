<template>
  <form @submit.prevent="submitData">
    <div>
      <label>Name</label>
      <input type="text" v-model="enteredName" />
    </div>
    <div>
      <label>age</label>
      <input type="text" v-model="enteredAge" />
    </div>
    <div>
      <button>Add</button>
    </div>
  </form>
</template>

<script>
export default {
  emits: ['add-profile'],
  data() {
    return {
      enteredName: '',
      enteredAge: '',
    };
  },
  methods: {
    submitData() {
      this.$emit(
        'add-profile',
        this.enteredName,
        this.enteredAge,
      );
    },
  },
};
</script>
