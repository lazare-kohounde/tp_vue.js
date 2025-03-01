<script setup>
import { ref } from "vue";
let text = ref("Hello world");
let is_active = ref(false);

let names = ref(["bob", "voleur", "opa", "retori", "obssed"]);
function add(){
  names.value.push(text.value);
  text.value = "";
  console.log(names.value);
};
</script>

<template>
<h1 :class="is_active?'title':''">{{text}}</h1>
<button @click="is_active=!is_active">change{{is_active}}</button>
<input v-model="text" type="text" name="text" id="" >
<button @click="add()">Ajout</button>

<p v-for="(name, index) in names" :key="index">{{name}}</p>

</template>

<style scoped>
.title{
  color: red;
}
</style>
