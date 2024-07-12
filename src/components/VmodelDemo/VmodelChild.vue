<script setup lang="ts">
import type { ClickObject } from './types';


const InputModel = defineModel('inputM');
const ClickModel = defineModel<number>('clickM',{required:true});
const ClickObjectModel = defineModel<ClickObject>('clickO', {
  required: true,
});

const updateNum = () => {
  ClickModel.value++;
};
const updateObj = () => {
  ClickObjectModel.value.num++;
  ClickObjectModel.value.str += '+';
};
</script>

<template>
  <span>My input</span> <input v-model="InputModel" />
  <br/>
  <button @click="updateNum">UpdateNum</button>
  <button @click="updateObj">UpdateObj</button>
</template>
