<script setup lang="ts">
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import { ref } from "vue";
import { inject } from "vue";

const searchValue = ref(``);
const axios: any = inject(`axios`);
const apiKey = `8YAJ4YEIYUFABUU26S8N6UVM457QFNYYET`;
</script>

<template>
	<h1>dish</h1>
</template>

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
