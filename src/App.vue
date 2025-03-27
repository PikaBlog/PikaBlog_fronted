<script setup>
import { RouterLink, RouterView } from "vue-router"
import Sidebar from "./components/Sidebar.vue"
Sidebar
</script>

<template>
	<div>
		<!-- 側邊欄 -->
		<Sidebar />
		<nav class="mb-4 bg-white shadow p-5 flex justify-between">
			<RouterLink to="/">Home</RouterLink>
			<!-- <button><img class="w-5 h-auto text-white" src="../src/assets/bars-solid .png" alt="" /></button> -->
			<RouterLink to="/login" class="border-sky-500 border-2 px-4 py-2 rounded text-white bg-sky-500 hover:bg-sky-600 active:bg-white active:text-sky-500">
				登入
			</RouterLink>
		</nav>
	</div>

	<!-- <RouterView /> -->
</template>

<style scoped></style>
