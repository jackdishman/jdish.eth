<script setup lang="ts">
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import Links from "./components/Links.vue";

let playAudio: boolean = false;
function toggleAudio(): void {
	playAudio = !playAudio;
	const myVideo: HTMLVideoElement = document.getElementById(
		"squiggles"
	) as HTMLVideoElement;
	if (myVideo) {
		myVideo.muted = playAudio;
	}
}
</script>

<template>
	<!-- Top header -->
	<div class="fixed w-full flex flex-row justify-between top-0 z-20">
		<Links class="bg-neutral-100/50 rounded-br-3xl px-4 py-2" />
		<div class="text-right">
			<a
				href="https://www.capsule.social/about/team"
				target="_blank"
				class="bg-neutral-100/50 rounded-bl-3xl px-4 py-2 text-right"
				>Capsule Social</a
			>
		</div>
	</div>
	<div class="z-10 fixed w-full h-screen">
		<!-- Center title -->
		<div class="w-full h-full flex items-center justify-center">
			<h1
				class="
					bg-neutral-100/50
					text-5xl
					px-4
					py-2
					rounded-3xl
					font-extra
					shadow-lg
				"
			>
				Jack Dishman
			</h1>
		</div>
	</div>
	<!-- Bottom controls & link -->
	<div
		class="
			fixed
			bottom-0
			z-10
			w-full
			flex flex-col
			sm:justify-between sm:flex-row
		"
	>
		<h6 class="bg-neutral-100/50 sm:rounded-tr-3xl px-4 py-2">
			<a
				href="https://superrare.com/artwork-v2/skate-squiggles-26797"
				target="_blank"
				>"Skate Squiggles" by Nate Mohler (SuperRare)</a
			>
			<button class="ml-5" @click="toggleAudio">Audio</button>
		</h6>
		<h6 class="bg-neutral-100/50 sm:rounded-tl-3xl px-4 py-2">
			Made with Vue 3, Vite, and TailwindCSS
		</h6>
	</div>
	<video
		class="w-full h-screen fixed object-cover"
		id="squiggles"
		autoplay
		loop
		muted
	>
		<source
			src="https://ipfs.pixura.io/ipfs/QmWqrEVVhWKykouXrb1gzdMghoerR5GdFWA7ueASag94Rc/sideview_scribles_LowBitrate.mp4"
			type="video/mp4"
		/>
	</video>
</template>

<style></style>
