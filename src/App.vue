<template>
  <div id="app">
    <edit-contact></edit-contact>
    <display-contacts></display-contacts>
  </div>
</template>

<script>
import EditContact from './components/EditContact.vue';
import DisplayContacts from './components/DisplayContacts.vue';

export default {
  name: "App",
  components: {
    EditContact,
    DisplayContacts,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
