<template>
  <div class="hello" style="text-align: center">
    <h1>Hello HelloWorld</h1>
    <p>Learning Vue</p>
    <input type="text" placeholder="input your name.." v-model="namamu">
    <p>{{ namamu }}</p>
    <button @click="greet(namamu)">Say Hi</button>
    <button @click="pass(namamu)">Send to Manjemen</button>
  </div>
</template>
<script>
export default {
  name: "HelloWorld",
  data(){
    return {
      namamu: "Nurjanah"
    };
  },
  props: {
    msg: String
  },
  
  methods: {
    greet(namamu){
      alert("Hello! " + namamu);
    },
    pass(namamu){
    this.$emit("fromChild", namamu);
    }
  }
};
</script>