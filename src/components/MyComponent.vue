<template>
  <h1>Hey,This is my Component</h1>
  <!-- <h2>Name is:{{ name }} {{ greeting }} {{ phone }}</h2> -->
  <h1>UserName is: {{ UserName }} {{ rollNo }}</h1>
</template>

<script>
export default {
  // props: ["greeting", "phone", "UserName", "rollNo"],
  props: {
    greeting: {
      type: String,
      required: true,
    },
    UserName: {
      type: String,
      required: true,
    },
    rollNo: {
      type: Number,
      default: 90,
    },
  },
  data() {
    return {
      name: "Ajay",
    };
  },
};
</script>

<style></style>