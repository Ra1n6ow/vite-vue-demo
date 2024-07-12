<template>
  <h1>inputM:{{ msg }}</h1>
  <h1>clickM:{{ num }}</h1>
  <h1>clickO:{{ obj }}</h1>
  <vmodel-child 
    v-model:inputM="msg"
    v-model:clickM="num" 
    v-model:clickO="obj"
  />
</template>

<script setup lang="ts">
import { ref } from "vue";
import VmodelChild from "./VmodelChild.vue";
import { ClickObject } from "./types";

const msg = ref("Hello");
const num = ref(0);
const obj = ref<ClickObject>({num: 0, str: "Hello"});
</script>
