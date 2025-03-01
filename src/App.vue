<script setup>
import { ref } from "vue";
let text = ref("Hello world");
let is_active = ref(false);

let names = ref(["bob", "voleur", "opa", "retori", "obssed"]);
let profile = [];
function add(){
  names.value.push(text.value);
  text.value = "";
 
  
};

let personne = {
    nom:"JOB",
    prenom:"Sael",
    age:20,
    sex:"M",

    child:{
      marie:true,
      Enfants:2
    }

  }
  personne.role="Admin";
  personne.ville='Calavi'

  profile.push("Geraud");
  profile.push("Keneth");
  profile.push("Kene");
  profile.shift();
  profile.unshift("fffff");
  let option = profile.join(",");
  const myArr = [[1,2],[3,4],[5,6]];
  const newArr = myArr.flat();
  let tab2 = ["sdf", "sdf"];
  profile.push(...tab2);
  console.log(option.split(","));
  console.log(profile);
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
