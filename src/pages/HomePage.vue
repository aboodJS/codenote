<script setup lang="ts">
import { javascript } from '@codemirror/lang-javascript';
import CodeMirror from 'vue-codemirror6';
import { ref } from 'vue';

const lang = javascript()

const value = ref("console.log('hello world')")
</script>

<template>
   <code-mirror v-model="value" :lang="lang" />
</template>

<style scoped></style>