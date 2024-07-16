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
            />
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
              Узнать подробнее
            </a>
          </div>
        </div>
      </div>
    </section>
    <section class="py-14">
      <div
        class="max-w-screen-xl mx-auto px-4 text-center text-gray-600 md:px-8"
      >
        <div class="mt-12">
          <ul class="grid gap-y-8 gap-x-12 sm:grid-cols-2 lg:grid-cols-3">
            <li
              v-for="(item, index) in features"
              :key="index"
              class="space-y-3"
            >
              <div
                class="w-16 h-12 mx-auto text-indigo-600 rounded-full flex items-center justify-center"
              >
                <img :src="item.icon" alt="icon" class="w-auto h-auto" />
              </div>
              <h4 class="text-lg text-gray-800 font-semibold uppercase">
                {{ item.title }}
              </h4>
            </li>
          </ul>
        </div>
      </div>
    </section>
    <section class="bg-white dark:bg-gray-900 pt-20 pb-10" id="course">
      <div class="flex-col w-auto mx-auto max-w-screen-xl">
        <div
          class="font-light text-gray-500 sm:text-lg dark:text-gray-400 text-center mb-10"
        >
          <h2
            class="mb-4 text-4xl tracking-tight text-gray-900 dark:text-white uppercase"
          >
            История создания Альфа курса
          </h2>
          <p class="mb-4 md:w-[600px] mx-auto">
            Альфа курс был создан в 1977 году в Лондоне и с тех пор
            распространился по всему миру, помогая миллионам людей найти ответы
            на вопросы о жизни и вере.
          </p>
        </div>
        <div
          class="font-light text-gray-500 sm:text-lg dark:text-gray-400 text-center mb-10"
        >
          <h2
            class="mb-4 text-4xl tracking-tight text-gray-900 dark:text-white uppercase"
          >
            Принципы и цели курса
          </h2>
          <p class="mb-4 md:w-[600px] mx-auto">
            Наши цели - создать безопасное и гостеприимное пространство для
            обсуждений, поделиться основами христианской веры и помочь людям
            найти личные ответы на важные вопросы.
          </p>
        </div>
        <div
          class="font-light text-gray-500 sm:text-lg dark:text-gray-400 text-center mb-10"
        >
          <h2
            class="mb-4 text-4xl tracking-tight text-gray-900 dark:text-white uppercase"
          >
            Формат проведения
          </h2>
          <p class="mb-4 md:w-[600px] mx-auto">
            Курс состоит из 11 сессий, проводимых еженедельно. Каждая сессия
            включает в себя ужин, просмотр видеоролика и обсуждение в малых
            группах.
          </p>
        </div>
      </div>
    </section>
    <Testimonials id="reviews" />
    <section class="mx-auto max-w-screen-xl py-14">
      <h2 class="md:text-6xl text-3xl text-center pb-10">
        Основные темы и вопросы:
      </h2>
      <div class="flex flex-col md:grid grid-cols-9 mx-auto p-2 text-blue-50">
        <!-- left -->
        <div class="flex flex-row-reverse md:contents">
          <div
            class="bg-indigo-500 col-start-1 col-end-5 p-4 rounded-xl my-4 ml-auto shadow-md"
          >
            <h3 class="font-semibold text-lg mb-1">В чем смысл жизни?</h3>
          </div>
          <div class="col-start-5 col-end-6 md:mx-auto relative mr-10">
            <div class="h-full w-6 flex items-center justify-center">
              <div class="h-full w-1 bg-indigo-500 pointer-events-none" />
            </div>
            <div
              class="w-6 h-6 absolute top-1/2 -mt-3 rounded-full bg-indigo-500 shadow"
            />
          </div>
        </div>
        <!-- right -->
        <div class="flex md:contents">
          <div class="col-start-5 col-end-6 mr-10 md:mx-auto relative">
            <div class="h-full w-6 flex items-center justify-center">
              <div class="h-full w-1 bg-indigo-500 pointer-events-none" />
            </div>
            <div
              class="w-6 h-6 absolute top-1/2 -mt-3 rounded-full bg-indigo-500 shadow"
            />
          </div>
          <div
            class="bg-indigo-500 col-start-6 col-end-10 p-4 rounded-xl my-4 mr-auto shadow-md"
          >
            <h3 class="font-semibold text-lg mb-1">Кто такой Иисус?</h3>
          </div>
        </div>
        <!-- left -->
        <div class="flex flex-row-reverse md:contents">
          <div
            class="bg-indigo-500 col-start-1 col-end-5 p-4 rounded-xl my-4 ml-auto shadow-md"
          >
            <h3 class="font-semibold text-lg mb-1">Почему существует зло?</h3>
          </div>
          <div class="col-start-5 col-end-6 md:mx-auto relative mr-10">
            <div class="h-full w-6 flex items-center justify-center">
              <div class="h-full w-1 bg-indigo-500 pointer-events-none" />
            </div>
            <div
              class="w-6 h-6 absolute top-1/2 -mt-3 rounded-full bg-indigo-500 shadow"
            />
          </div>
        </div>
        <!-- left -->
        <div class="flex flex-row-reverse md:contents">
          <div
            class="bg-indigo-500 col-start-1 col-end-5 p-4 rounded-xl my-4 ml-auto shadow-md"
          >
            <h3 class="font-semibold text-lg mb-1">
              Как молиться и почему это важно?
            </h3>
          </div>
          <div class="col-start-5 col-end-6 md:mx-auto relative mr-10">
            <div class="h-full w-6 flex items-center justify-center">
              <div class="h-full w-1 bg-indigo-500 pointer-events-none" />
            </div>
            <div
              class="w-6 h-6 absolute top-1/2 -mt-3 rounded-full bg-indigo-500 shadow"
            />
          </div>
        </div>
        <!-- right -->
        <div class="flex md:contents">
          <div class="col-start-5 col-end-6 mr-10 md:mx-auto relative">
            <div class="h-full w-6 flex items-center justify-center">
              <div class="h-full w-1 bg-indigo-500 pointer-events-none" />
            </div>
            <div
              class="w-6 h-6 absolute top-1/2 -mt-3 rounded-full bg-indigo-500 shadow"
            />
          </div>
          <div
            class="bg-indigo-500 col-start-6 col-end-10 p-4 rounded-xl my-4 mr-auto shadow-md"
          >
            <h3 class="font-semibold text-lg mb-1">
              Как читать и понимать Библию?
            </h3>
          </div>
        </div>
      </div>
    </section>
    <section class="mx-auto max-w-screen-xl py-14">
      <div class="flex justify-center items-center flex-col">
        <h3 class="text-2xl md:text-3xl text-center pb-10">
          Присоединяйтесь к нам!<br />
          Регистрация занимает всего пару минут.
        </h3>
        <button
          class="bg-[#f00] px-3.5 py-2.5 text-sm text-white shadow-sm hover:bg-orange-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-orange-600 uppercase"
        >
          Регистрация
        </button>
      </div>
    </section>
    <section class="bg-blue-50 dark:bg-gray-900" id="contact">
      <div class="mx-auto max-w-7xl px-4 py-16 sm:px-6 lg:px-8 lg:py-20">
        <div class="mb-4">
          <div
            class="mb-6 max-w-3xl text-center sm:text-center md:mx-auto md:mb-12"
          >
            <h2 class="md:text-6xl text-3xl text-center pb-10 text-white">
              Контакты
            </h2>
          </div>
        </div>
        <div class="flex items-stretch justify-center">
          <div class="grid md:grid-cols-2">
            <div class="h-full p-5 md:p-12">
              <ul class="mb-6 md:mb-0">
                <li class="flex">
                  <div
                    class="flex h-10 w-10 items-center justify-center rounded bg-blue-900 text-gray-50"
                  >
                    <svg
                      xmlns="http://www.w3.org/2000/svg"
                      width="24"
                      height="24"
                      viewBox="0 0 24 24"
                      fill="none"
                      stroke="currentColor"
                      stroke-width="2"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      class="h-6 w-6"
                    >
                      <path d="M9 11a3 3 0 1 0 6 0a3 3 0 0 0 -6 0"></path>
                      <path
                        d="M17.657 16.657l-4.243 4.243a2 2 0 0 1 -2.827 0l-4.244 -4.243a8 8 0 1 1 11.314 0z"
                      ></path>
                    </svg>
                  </div>
                  <div class="ml-4 mb-4">
                    <h3
                      class="mb-2 text-lg font-medium leading-6 text-gray-900 dark:text-white"
                    >
                      Адрес:
                    </h3>
                    <p class="text-gray-600 dark:text-slate-400">
                      ул. Примерная, 123
                    </p>
                    <p class="text-gray-600 dark:text-slate-400">
                      г. Краснодар
                    </p>
                  </div>
                </li>
                <li class="flex">
                  <div
                    class="flex h-10 w-10 items-center justify-center rounded bg-blue-900 text-gray-50"
                  >
                    <svg
                      xmlns="http://www.w3.org/2000/svg"
                      width="24"
                      height="24"
                      viewBox="0 0 24 24"
                      fill="none"
                      stroke="currentColor"
                      stroke-width="2"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      class="h-6 w-6"
                    >
                      <path
                        d="M5 4h4l2 5l-2.5 1.5a11 11 0 0 0 5 5l1.5 -2.5l5 2v4a2 2 0 0 1 -2 2a16 16 0 0 1 -15 -15a2 2 0 0 1 2 -2"
                      ></path>
                      <path d="M15 7a2 2 0 0 1 2 2"></path>
                      <path d="M15 3a6 6 0 0 1 6 6"></path>
                    </svg>
                  </div>
                  <div class="ml-4 mb-4">
                    <h3
                      class="mb-2 text-lg font-medium leading-6 text-gray-900 dark:text-white"
                    >
                      Контакты:
                    </h3>
                    <p class="text-gray-600 dark:text-slate-400">
                      Телефон: +7 (123) 456-78-90
                    </p>
                    <p class="text-gray-600 dark:text-slate-400">
                      Email: info@alphacourse.ru
                    </p>
                  </div>
                </li>
              </ul>
            </div>
            <div class="card h-fit max-w-6xl p-5 md:p-12" id="form">
              <h2 class="mb-4 text-2xl dark:text-white">
                У вас остались вопросы?
              </h2>
              <Form />
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<style>
  .text-sh {
    text-shadow: 1px 1px 1px #000;
  }
  .bg-index {
    background-image: url('/assets/img/bg.jpeg');
    background-size: cover;
    background-repeat: no-repeat;
  }
  html {
    scroll-behavior: smooth;
  }
</style>
