<script setup lang="ts">
const reviews = [
  {
    name: 'Иван',
    description:
				'Я нашел ответы на вопросы, которые беспокоили меня долгие годы. Альфа курс изменил мою жизнь.',
  },
  {
    name: 'Анна',
    description: 'Встречи были вдохновляющими и полезными. Рекомендую всем!',
  },
]
</script>

<template>
  <section class="bg-white">
    <div class="mx-auto max-w-screen-xl px-4 py-14 sm:px-6 lg:px-8 lg:py-16">
      <h2 class="text-center text-4xl tracking-tight text-gray-900 sm:text-6xl">
        Отзывы участников:
      </h2>

      <div class="mt-8 grid grid-cols-1 gap-4 md:grid-cols-3 md:gap-8">
        <blockquote
          v-for="(user, id) in reviews"
          :key="id"
          class="rounded-lg bg-gray-50 p-6 shadow-sm sm:p-8"
        >
          <div class="flex items-center gap-4">
            <div>
              <p class="mt-0.5 text-lg font-medium text-gray-900">
                {{ user.name }}
              </p>
            </div>
          </div>

          <p class="mt-4 text-gray-700">
            {{ user.description }}
          </p>
        </blockquote>
      </div>
    </div>
  </section>
</template>
