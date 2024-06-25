<script setup lang="ts">
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
              src="/assets/icons/img/pngegg.png"
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
            <nuxt-icon
              name="burger"
              filled
            />
          </button>
        </div>
        <div class="hidden lg:flex lg:gap-x-12">
          <a
            v-for="item in navigation"
            :key="item.name"
            :href="item.href"
            class="text-sm leading-6 text-white hover:text-orange-600 transition-all uppercase"
          >{{ item.name }}</a>
        </div>
        <div class="hidden lg:flex lg:flex-1 lg:justify-end">
          <a
            href="#"
            class="text-sm leading-6 text-gray-900"
          ><nuxt-icon name="vk" /></a>
          <a
            href="#"
            class="text-sm leading-6 text-gray-900"
          ><nuxt-icon name="telegram" /></a><a
            href="#"
            class="text-sm leading-6 text-gray-900"
          ><nuxt-icon name="wa" /></a>
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
                src="/assets/icons/img/pngegg.png"
                alt="Альфа курс лого"
              >
            </a>
            <button
              type="button"
              class="-m-2.5 rounded-md p-2.5 text-gray-700 mob-button"
              @click="mobileMenuOpen = false"
            >
              <span class="sr-only">Close menu</span>
              <nuxt-icon name="close" />
            </button>
          </div>
          <div class="mt-6 flow-root">
            <div class="-my-6 divide-y divide-gray-500/10">
              <div class="space-y-2 py-6">
                <a
                  v-for="item in navigation"
                  :key="item.name"
                  :href="item.href"
                  class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50 uppercase hover:text-orange-600 transition-all"
                >{{ item.name }}</a>
              </div>
              <div class="py-6 flex mobile">
                <a
                  href="#"
                  class="-mx-3 block rounded-lg px-3 py-2.5 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50"
                ><nuxt-icon name="vk" /></a>
                <a
                  href="#"
                  class="-mx-3 block rounded-lg px-3 py-2.5 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50"
                ><nuxt-icon name="telegram" /></a>
                <a
                  href="#"
                  class="-mx-3 block rounded-lg px-3 py-2.5 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50"
                ><nuxt-icon name="wa" /></a>
              </div>
            </div>
          </div>
        </DialogPanel>
      </Dialog>
    </header>
  </div>
</template>

<style>
	.nuxt-icon svg {
		width: 3em;
		height: 2em;
		margin-bottom: 0.125em;
		vertical-align: middle;
		color: white;
	}
	.nuxt-icon svg:hover {
		color: #ea580c;
	}
	@media (max-width: 1020px) {
		.mobile .nuxt-icon svg {
			color: #000;
		}
		.mob-button .nuxt-icon svg {
			color: #000;
		}
	}
</style>
