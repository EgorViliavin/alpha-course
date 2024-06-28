<script setup>
	import vk from './icons/vk.vue';
	import wa from './icons/wa.vue';
	import telegram from './icons/telegram.vue';
</script>

<template>
	<footer
		class="bg-white shadow grid grid-cols-1 justify-center items-center gap-10 sm:grid-cols-3 p-4 sm:p-6 xl:p-8">
		<div class="w-100 flex items-center justify-center">
			<img
				src="/assets/img/pngegg.png"
				alt="Логотип"
				class="w-20" />
		</div>
		<div class="w-100">
			<p
				class="mb-4 text-sm text-center text-gray-500 dark:text-gray-400 sm:mb-0">
				&copy; 2024 Альфа курс. Все права защищены.
			</p>
		</div>
		<div class="flex justify-center items-center space-x-1 w-100">
			<a
				href="#"
				data-tooltip-target="tooltip-facebook"
				class="inline-flex justify-center p-2 text-gray-500 rounded-lg cursor-pointer">
				<vk class="hover:text-[#f00] transition" />
				<span class="sr-only">vk</span>
			</a>

			<a
				href="#"
				data-tooltip-target="tooltip-twitter"
				class="inline-flex justify-center p-2 text-gray-500 rounded-lg cursor-pointer">
				<telegram class="hover:text-[#f00] transition" />
				<span class="sr-only">Telegram</span>
			</a>

			<a
				href="#"
				data-tooltip-target="tooltip-github"
				class="inline-flex justify-center p-2 text-gray-500 rounded-lg cursor-pointer">
				<wa class="hover:text-[#f00] transition" />
				<span class="sr-only">Watshapp</span>
			</a>
		</div>
	</footer>
</template>
