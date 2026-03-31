<script setup lang="ts">
import { javascript } from '@codemirror/lang-javascript';
import CodeMirror from 'vue-codemirror6';
import { ref } from 'vue';

const lang = javascript()
const value = ref("console.log('hello world')")
const snippetName = ref("")

async function sendData() {
   console.log({userName: snippetName.value, code: value.value})
}

</script>

<template>
   <input type="text" placeholder="enter snippet name" v-model="snippetName">
   <code-mirror v-model="value" :lang="lang" />
   <button @click="sendData">Submit</button>
</template>

<style scoped></style>