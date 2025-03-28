<script setup>
import { ref } from "vue"
const isOpen = ref(false)
const toggleSidebar = () => {
	isOpen.value = !isOpen.value
}
</script>

<template>
	<!-- 漢堡選單按鈕 -->
	<button @click="toggleSidebar" class="fixed top-5 left-5 z-50 p-2 rounded cursor-pointer">
		<img class="w-6 h-auto" src="../assets/bars-solid .png" alt="menu" />
	</button>
	<!-- 遮罩層 -->
	<div v-if="isOpen" class="overlay"></div>
	<!-- 側邊欄 -->
	<div :class="['sidebar', { open: isOpen }]">
		<div>
			<!-- div 圓形 至中 -->

			<div class="circle"></div>
			<p class="text-2xl text-center">你的名字</p>
			<button class="aboutMe">個人資料</button>
			<a class="flex justify-center mt-3">#hashtag1、#hashtag2</a>
		</div>
	</div>
</template>

<style scoped>
.overlay {
	position: fixed;
	top: 85px;
	left: 0;
	width: 100%;
	height: 100%;
	background-color: rgba(0, 0, 0, 0.5);
	transition: opacity 0.3s ease-in-out;
}
.sidebar {
	position: fixed;
	top: 85px;
	left: 0;
	width: 250px;
	height: 100%;
	background-color: #f8f9fa;
	box-shadow: 2px 0 5px rgba(0, 0, 0, 0.3);
	transform: translateX(-100%);
	transition: transform 0.3s ease-in-out;
}
/* 開啟狀態 */
.sidebar.open {
	transform: translateX(0);
}
.circle {
	width: 130px;
	height: 130px;
	margin: 28px auto;
	border-radius: 50%;
	background-color: #bed1e1;
}
.aboutMe {
	background-color: white;
	display: flex;
	justify-content: center;
	align-items: center;
	border-radius: 20px;
	margin: 10px auto;
	font-size: 15px;
	padding: 3px 8px;
	border-radius: 5px;
	border: 2px solid #bed1e1;
}
.aboutMe:hover {
	background-color: #bed1e1;
	color: white;
	transition: all 0.3s ease-in-out;
	cursor: pointer;
}
.aboutMe:active {
	background-color: #95a3af;
	color: white;
	transition: all 0.3s ease-in-out;
	cursor: pointer;
}
</style>
