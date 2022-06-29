<template>
  <div>
    <h2>Enter a new contact</h2>
    <form @submit.prevent="addContact">
      <div class="form-control">
        <label for="user-name">Name</label>
        <input
          id="user-name"
          name="user-name"
          type="text"
          v-model="form.name"
        />
      </div>
      <div class="form-control">
        <label for="age">Age (Years)</label>
        <input id="age" name="age" type="number" v-model="form.age" />
      </div>
      <div class="form-control">
        <label for="mobile">Contact number</label>
        <input id="age" name="age" type="tel" v-model="form.mobile" />
      </div>

      <div>
        <button>Save Contact</button>
      </div>
    </form>
    {{ form }}
  </div>
</template>

<script>
export default {
  name: "EditContact",

  data() {
    return {
      contactList: [],
      form: {
        name: "",
        age: "",
        mobile: "",
      },
    };
  },
  methods: {
    addContact() {
      this.contactList.push({ ...this.form });
      console.log(this.form);
      console.log(this.contactList);

      this.form.name = "";
      this.form.age = "";
      this.form.mobile = "";

      this.$emit('clicked', this.contactList)
    },
  },
};
</script>

<style scoped>
</style>
