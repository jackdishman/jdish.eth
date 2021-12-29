<script setup lang="ts">
import Vue from "vue";
const plugin = document.createElement("script");
plugin.setAttribute("src", "https://platform.twitter.com/widgets.js");
plugin.async = true;
document.head.appendChild(plugin);
</script>
<template>
	<a
		class="twitter-timeline"
		href="https://twitter.com/JackDishman?ref_src=twsrc%5Etfw"
		>Tweets by JackDishman</a
	>
</template>
