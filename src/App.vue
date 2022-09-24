<template>
  <h1>Hello World</h1>
  <!-- rendering MyComponent -->
  <!-- <my-component
    greeting="Good Morning"
    phone="9964647560"
    :UserName="UserName"
    rollNo="100"
  /> -->
  <!-- sending function to child component use v-on or @ -->
  <child-component @getDataFromChild="getDataFromChild" />
  <h3>Data of Toy from child:{{ kidsToyData }}</h3>
</template>

<script>
import ChildComponent from "./components/ChildComponent.vue";
// import MyComponent from "./components/MyComponent.vue";
export default {
  name: "App",
  components: {
    // MyComponent
    ChildComponent,
  },
  //data
  data() {
    return {
      UserName: "Raju Rastogi",
      kidsToyData: "",
    };
  },
  methods: {
    //chocolate function
    //1.In parent component create  a function and pass it to child component
    //2.call the function in child component and pass the data inside tat function
    getDataFromChild(childData) {
      console.log("chocolate function executed", childData);
      this.kidsToyData = childData;
    },
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