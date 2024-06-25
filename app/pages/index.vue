<script setup lang="ts">
	useSeoMeta({
		title: 'АЛЬФА КУРС || Главная страница',
	});
</script>

<template>
	<div>
		<div class="relative isolate px-6 pt-14 lg:px-8">
			<video
				class="w-full object-cover absolute -z-10 top-0 left-0 h-screen"
				autoplay
				muted
				loop>
				<source
					src="https://static.vecteezy.com/system/resources/previews/014/931/397/jesus-christ-comforts-walking-with-a-young-man-teen-boy-christian-christianity-spiritual-religion-free-video.webm"
					type="video/webm" />
			</video>
			<div
				class="absolute inset-x-0 -top-40 -z-10 transform-gpu overflow-hidden blur-3xl sm:-top-80"
				aria-hidden="true" />

			<div class="mx-auto max-w-5xl py-32 sm:py-48 lg:py-56">
				<div class="hidden sm:mb-8 sm:flex sm:justify-center" />
				<div class="text-center">
					<h1
						class="text-4xl tracking-tight sm:text-6xl text-white text-sh uppercase">
						"Исследуй вопросы жизни, веры и смысла вместе с нами!"
					</h1>

					<div class="mt-10 flex items-center justify-center gap-x-6">
						<a
							href="#"
							class="bg-orange-600 px-3.5 py-2.5 text-sm text-white shadow-sm hover:bg-orange-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-orange-600 uppercase"
							>Узнать больше</a
						>
						<a
							href="#"
							class="bg-indigo-600 px-3.5 py-2.5 text-sm text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600 uppercase"
							>Регистрация</a
						>
					</div>
				</div>
			</div>
			<div
				class="absolute inset-x-0 top-[calc(100%-13rem)] -z-10 transform-gpu overflow-hidden blur-3xl sm:top-[calc(100%-30rem)]"
				aria-hidden="true" />
		</div>
	</div>
</template>

<style scoped>
	.text-sh {
		text-shadow: 1px 1px 1px #000;
	}
</style>
