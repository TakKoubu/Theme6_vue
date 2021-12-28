<template>
  <section>
    <user-data @add-profile="addUser"></user-data>
    <active-user
      v-for="user in users"
      :key="user.id"
      :id="user.id"
      :name="user.name"
      :age="user.age"
      class="inlineblock"
    ></active-user>
  </section>
</template>

<script>
import UserData from './components/UserData.vue';
export default {
  components: { UserData },
  data() {
    return {
      users: [
        {
          id: 'manuel',
          name: 'Manuel Lorenz',
          age: '10'
        },
        {
          id: 'julie',
          name: 'Julie Jones',
          age: '21'
        },
      ],
    };
  },
  methods: {
    addUser(name, age) {
      const newUser = {
        id: new Date().toISOString(),
        name: name,
        age: age
      };
      this.users.push(newUser);
    },
  },
};
</script>
