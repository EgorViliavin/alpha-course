<script setup lang="ts">
useSeoMeta({
  title: 'АЛЬФА КУРС || Главная страница',
})
</script>

<template>
  <div>
    <div class="relative isolate px-6 pt-14 lg:px-8 bg-index">
      <div
        class="absolute inset-x-0 -top-40 -z-10 transform-gpu overflow-hidden blur-3xl sm:-top-80"
        aria-hidden="true"
      />

      <div class="mx-auto max-w-5xl py-32 sm:py-48 lg:py-56">
        <div class="hidden sm:mb-8 sm:flex sm:justify-center" />
        <div class="text-center">
          <h1
            class="text-4xl tracking-tight sm:text-6xl text-white font-semibold uppercase"
            style="text-shadow: 2px 1px 50px #ea580c"
          >
            "Исследуй вопросы жизни, веры и смысла вместе с нами!"
          </h1>

          <div class="mt-10 flex items-center justify-center gap-x-6">
            <a
              href="#"
              class="bg-[#f00] px-3.5 py-2.5 text-sm text-white shadow-sm hover:bg-orange-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-orange-600 uppercase"
            >Узнать больше</a>
            <a
              href="#"
              class="bg-indigo-600 px-3.5 py-2.5 text-sm text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600 uppercase"
            >Регистрация</a>
          </div>
        </div>
      </div>
    </div>

    <section>
      <div
        class="mx-auto max-w-screen-xl px-4 py-8 sm:px-6 sm:py-12 lg:px-8 lg:py-16"
      >
        <div class="grid grid-cols-1 gap-8 lg:grid-cols-2 lg:gap-16">
          <div
            class="relative h-64 overflow-hidden rounded-lg shadow-2xl sm:h-80 lg:order-last lg:h-full"
          >
            <img
              alt=""
              src="/assets/img/about-alfa.jpeg"
              class="absolute inset-0 h-full w-full object-cover"
            >
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
              class="mt-8 inline-block bg-indigo-600 px-12 py-3 text-sm font-medium text-white transition hover:bg-indigo-700 focus:outline-none focus:ring focus:ring-yellow-400 uppercase"
            >
              Узнать расписание
            </a>
          </div>
        </div>
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
