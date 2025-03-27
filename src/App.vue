<script setup>
import { RouterLink, RouterView } from "vue-router"
</script>

<template>
	<div>
		<nav class="mb-4 bg-white shadow p-5 flex justify-between">
			<RouterLink to="/"><img class="w-5 h-auto text-white" src="../src/assets/bars-solid .png" alt="" /></RouterLink>
			<RouterLink to="/login" class="bg-sky-600 pl-4 pr-4 pt-2 pb-2 rounded text-white">登入</RouterLink>
		</nav>
	</div>

	<RouterView />
</template>

<style scoped></style>
