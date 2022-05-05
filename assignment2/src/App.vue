<template>
  <div id="app">
    <BaseButton @isClicked='test("Hey Hey Hey")' :staySameText="primary"></BaseButton>
    <BaseButton @isClicked='reverse' :isReverse="reverseText"></BaseButton>
  </div>
</template>

<script>
import BaseButton from "./components/button.vue"


export default {
  
  name: 'App',
  components: {
    BaseButton,
  },
  data() {
    return {
      reverseText: "Primary" ,
      primary: "Primary"
    }
  },

  methods: {
    test(string) {
      alert(string);
    },
    reverse(title) {
      console.log(title);
            this.reverseText = title.split("").reverse().join("");
            console.log(this.reverseText);
        }
  }
}
</script>

<style>
*{
  margin: 0;
  padding: 0;
}

#app {
  width: 80%;
  margin-left: auto;
  margin-right: auto;
  padding-top: 70px;
  height: 400px;
  background-color: rgba(184, 233, 148, 0.6);
  border-top: 5px solid rgba(68, 189, 50,1.0);
}
</style>
