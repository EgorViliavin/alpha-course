<script setup lang="ts">
	useSeoMeta({
		title: 'АЛЬФА КУРС || Главная страница',
	});

	const features = [
		{
			icon: `https://img.icons8.com/hands/100/trust.png`,
			title: 'Дружелюбная атмосфера',
		},
		{
			icon: 'https://img.icons8.com/hands/100/question-mark.png',
			title: 'Интересные обсуждения',
		},
		{
			icon: 'https://img.icons8.com/hands/100/handshake.png',
			title: 'Новые знакомства',
		},
	];
</script>

<template>
	<div>
		<section class="relative isolate px-6 pt-14 lg:px-8 bg-index">
			<div
				class="absolute inset-x-0 -top-40 -z-10 transform-gpu overflow-hidden blur-3xl sm:-top-80"
				aria-hidden="true" />

			<div class="mx-auto max-w-5xl py-32 sm:py-48 lg:py-56">
				<div class="hidden sm:mb-8 sm:flex sm:justify-center" />
				<div class="text-center">
					<h1
						class="text-4xl tracking-tight sm:text-6xl text-white font-semibold uppercase"
						style="text-shadow: 2px 1px 50px #ea580c">
						"Исследуй вопросы жизни, веры и смысла вместе с нами!"
					</h1>

					<div class="mt-10 flex items-center justify-center gap-x-6">
						<a
							href="#"
							class="bg-[#f00] px-3.5 py-2.5 text-sm text-white shadow-sm hover:bg-orange-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-orange-600 uppercase"
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
		</section>

		<section>
			<div
				class="mx-auto max-w-screen-xl px-4 py-8 sm:px-6 sm:py-12 lg:px-8 lg:py-16">
				<div class="grid grid-cols-1 gap-8 lg:grid-cols-2 lg:gap-16">
					<div
						class="relative h-64 overflow-hidden rounded-lg shadow-2xl sm:h-80 lg:order-last lg:h-full">
						<img
							alt=""
							src="/assets/img/about-alfa.jpeg"
							class="absolute inset-0 h-full w-full object-cover" />
					</div>

					<div class="lg:py-24">
						<h2 class="text-3xl font-bold text-[#f00] sm:text-6xl">
							Альфа курс
						</h2>

						<p class="mt-4 text-gray-600">
							это серия интерактивных сессий, где можно свободно обсуждать
							важнейшие вопросы жизни, веры и смысла. Курс подходит для всех,
							кто интересуется христианством или хочет углубить свои знания.
						</p>

						<a
							href="#"
							class="mt-8 inline-block bg-indigo-600 px-12 py-3 text-sm font-medium text-white transition hover:bg-indigo-700 focus:outline-none focus:ring focus:ring-yellow-400 uppercase">
							Узнать подробнее
						</a>
					</div>
				</div>
			</div>
		</section>
		<section class="py-14">
			<div
				class="max-w-screen-xl mx-auto px-4 text-center text-gray-600 md:px-8">
				<div class="mt-12">
					<ul class="grid gap-y-8 gap-x-12 sm:grid-cols-2 lg:grid-cols-3">
						<li
							v-for="(item, index) in features"
							:key="index"
							class="space-y-3">
							<div
								class="w-16 h-12 mx-auto text-indigo-600 rounded-full flex items-center justify-center">
								<img
									:src="item.icon"
									alt="icon"
									class="w-auto h-auto" />
							</div>
							<h4 class="text-lg text-gray-800 font-semibold uppercase">
								{{ item.title }}
							</h4>
						</li>
					</ul>
				</div>
			</div>
		</section>
		<Testimonials />
		<section class="mx-auto max-w-screen-xl py-14">
			<h2 class="md:text-6xl text-3xl text-center pb-10">
				Основные темы и вопросы:
			</h2>
			<div class="flex flex-col md:grid grid-cols-9 mx-auto p-2 text-blue-50">
				<!-- left -->
				<div class="flex flex-row-reverse md:contents">
					<div
						class="bg-indigo-500 col-start-1 col-end-5 p-4 rounded-xl my-4 ml-auto shadow-md">
						<h3 class="font-semibold text-lg mb-1">В чем смысл жизни?</h3>
					</div>
					<div class="col-start-5 col-end-6 md:mx-auto relative mr-10">
						<div class="h-full w-6 flex items-center justify-center">
							<div class="h-full w-1 bg-indigo-500 pointer-events-none"></div>
						</div>
						<div
							class="w-6 h-6 absolute top-1/2 -mt-3 rounded-full bg-indigo-500 shadow"></div>
					</div>
				</div>
				<!-- right -->
				<div class="flex md:contents">
					<div class="col-start-5 col-end-6 mr-10 md:mx-auto relative">
						<div class="h-full w-6 flex items-center justify-center">
							<div class="h-full w-1 bg-indigo-500 pointer-events-none"></div>
						</div>
						<div
							class="w-6 h-6 absolute top-1/2 -mt-3 rounded-full bg-indigo-500 shadow"></div>
					</div>
					<div
						class="bg-indigo-500 col-start-6 col-end-10 p-4 rounded-xl my-4 mr-auto shadow-md">
						<h3 class="font-semibold text-lg mb-1">Кто такой Иисус?</h3>
					</div>
				</div>
				<!-- left -->
				<div class="flex flex-row-reverse md:contents">
					<div
						class="bg-indigo-500 col-start-1 col-end-5 p-4 rounded-xl my-4 ml-auto shadow-md">
						<h3 class="font-semibold text-lg mb-1">Почему существует зло?</h3>
					</div>
					<div class="col-start-5 col-end-6 md:mx-auto relative mr-10">
						<div class="h-full w-6 flex items-center justify-center">
							<div class="h-full w-1 bg-indigo-500 pointer-events-none"></div>
						</div>
						<div
							class="w-6 h-6 absolute top-1/2 -mt-3 rounded-full bg-indigo-500 shadow"></div>
					</div>
				</div>
				<!-- left -->
				<div class="flex flex-row-reverse md:contents">
					<div
						class="bg-indigo-500 col-start-1 col-end-5 p-4 rounded-xl my-4 ml-auto shadow-md">
						<h3 class="font-semibold text-lg mb-1">
							Как молиться и почему это важно?
						</h3>
					</div>
					<div class="col-start-5 col-end-6 md:mx-auto relative mr-10">
						<div class="h-full w-6 flex items-center justify-center">
							<div class="h-full w-1 bg-indigo-500 pointer-events-none"></div>
						</div>
						<div
							class="w-6 h-6 absolute top-1/2 -mt-3 rounded-full bg-indigo-500 shadow"></div>
					</div>
				</div>
				<!-- right -->
				<div class="flex md:contents">
					<div class="col-start-5 col-end-6 mr-10 md:mx-auto relative">
						<div class="h-full w-6 flex items-center justify-center">
							<div class="h-full w-1 bg-indigo-500 pointer-events-none"></div>
						</div>
						<div
							class="w-6 h-6 absolute top-1/2 -mt-3 rounded-full bg-indigo-500 shadow"></div>
					</div>
					<div
						class="bg-indigo-500 col-start-6 col-end-10 p-4 rounded-xl my-4 mr-auto shadow-md">
						<h3 class="font-semibold text-lg mb-1">
							Как читать и понимать Библию?
						</h3>
					</div>
				</div>
			</div>
		</section>
		<section class="mx-auto max-w-screen-xl py-14">
			<div class="flex justify-center items-center flex-col">
				<h3 class="text-4xl text-center pb-10">
					Присоединяйтесь к нам!<br />
					Регистрация занимает всего пару минут.
				</h3>
				<button
					class="bg-[#f00] px-3.5 py-2.5 text-sm text-white shadow-sm hover:bg-orange-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-orange-600 uppercase">
					Регистрация
				</button>
			</div>
		</section>
	</div>
</template>

<style scoped>
	.text-sh {
		text-shadow: 1px 1px 1px #000;
	}
	.bg-index {
		background-image: url('/assets/img/bg.jpeg');
		background-size: cover;
		background-repeat: no-repeat;
	}
</style>
