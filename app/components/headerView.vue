<script setup lang="ts">
import vk from './icons/vk.vue'
import wa from './icons/wa.vue'
import telegram from './icons/telegram.vue'
import burger from './icons/burger.vue'
import close from './icons/close.vue'

const mobileMenuOpen = ref(false)

const navigation = [
  { name: 'Главная', href: '#' },
  { name: 'О Курсе', href: '#' },
  { name: 'Расписание', href: '#' },
  { name: 'Регистрация', href: '#' },
  { name: 'Отзывы', href: '#' },
  { name: 'Контакты', href: '#' },
]
</script>

<template>
  <div class="bg-white">
    <header class="inset-x-0 top-0 z-50 absolute">
      <nav
        class="flex items-center justify-between p-6 lg:px-8"
        aria-label="Global"
      >
        <div class="flex lg:flex-1">
          <a
            href="#"
            class="-m-1.5 p-1.5"
          >
            <span class="sr-only">Your Company</span>
            <img
              class="h-20 w-20"
              src="/assets/img/pngegg.png"
              alt="Лого альфа курс"
            >
          </a>
        </div>
        <div class="flex lg:hidden">
          <button
            type="button"
            class="-m-2.5 inline-flex items-center justify-center rounded-md p-2.5 text-gray-700"
            @click="mobileMenuOpen = true"
          >
            <span class="sr-only">Open main menu</span>
            <burger class="hover:text-orange-600 transition-colors" />
          </button>
        </div>
        <div class="hidden lg:flex lg:gap-x-12">
          <a
            v-for="item in navigation"
            :key="item.name"
            :href="item.href"
            class="text-sm leading-6 text-white hover:text-orange-600 transition-colors uppercase"
          >{{ item.name }}</a>
        </div>
        <div class="hidden lg:flex lg:flex-1 lg:justify-end gap-3">
          <a
            href="#"
            class="text-sm leading-6 text-white"
          ><vk class="hover:text-orange-600 transition-colors" /></a>
          <a
            href="#"
            class="text-sm leading-6 text-white"
          ><telegram class="hover:text-orange-600 transition-colors" /></a><a
            href="#"
            class="text-sm leading-6 text-white"
          ><wa class="hover:text-orange-600 transition-colors" /></a>
        </div>
      </nav>
      <Dialog
        class="lg:hidden"
        :open="mobileMenuOpen"
        @close="mobileMenuOpen = false"
      >
        <div class="fixed inset-0 z-50" />
        <DialogPanel
          class="fixed inset-y-0 right-0 z-50 w-full overflow-y-auto bg-white px-6 py-6 sm:max-w-sm sm:ring-1 sm:ring-gray-900/10"
        >
          <div class="flex items-center justify-between">
            <a
              href="#"
              class="-m-1.5 p-1.5"
            >
              <span class="sr-only">Your Company</span>
              <img
                class="w-auto h-16"
                src="/assets/img/pngegg.png"
                alt="Альфа курс лого"
              >
            </a>
            <button
              type="button"
              class="-m-2.5 rounded-md p-2.5 text-gray-700 mob-button"
              @click="mobileMenuOpen = false"
            >
              <span class="sr-only">Close menu</span>
              <close class="hover:text-orange-600 transition-colors" />
            </button>
          </div>
          <div class="mt-6 flow-root">
            <div class="-my-6 divide-y divide-gray-500/10">
              <div class="space-y-2 py-6">
                <a
                  v-for="item in navigation"
                  :key="item.name"
                  :href="item.href"
                  class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50 uppercase hover:text-orange-600 transition-colors"
                >{{ item.name }}</a>
              </div>
              <div class="py-6 flex mobile gap-4">
                <a
                  href="#"
                  class="-mx-3 block rounded-lg px-3 py-2.5 text-base font-semibold leading-7 text-gray-900"
                ><vk /></a>
                <a
                  href="#"
                  class="-mx-3 block rounded-lg px-3 py-2.5 text-base font-semibold leading-7 text-gray-900"
                ><telegram /></a>
                <a
                  href="#"
                  class="-mx-3 block rounded-lg px-3 py-2.5 text-base"
                ><wa /></a>
              </div>
            </div>
          </div>
        </DialogPanel>
      </Dialog>
    </header>
  </div>
</template>

<style></style>
