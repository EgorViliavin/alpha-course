<script setup lang="ts">
  import { ref, computed } from 'vue';
  import { z } from 'zod';

  const inputNameValue = ref('');
  const inputEmailValue = ref('');
  const inputMessageValue = ref('');

  const dataSchema = z.object({
    name: z.string(),
    email: z.string().email(),
    text: z.string(),
  });

  const isFormValid = computed(() => {
    return (
      inputNameValue.value.trim() !== '' &&
      inputEmailValue.value.trim() !== '' &&
      inputMessageValue.value.trim() !== ''
    );
  });

  const formSubmit = () => {
    const formMsgValue = computed(() => ({
      name: inputNameValue.value,
      email: inputEmailValue.value,
      text: inputMessageValue.value,
    }));

    const { data, error } = dataSchema.safeParse(formMsgValue.value);
    if (data) {
      $fetch('https://f520bbc4450801c7.mokky.dev/users', {
        method: 'POST',
        body: JSON.stringify(data),
      });

      inputEmailValue.value = '';
      inputNameValue.value = '';
      inputMessageValue.value = '';
    } else {
      inputEmailValue.value = error.message;
      inputNameValue.value = error.message;
      inputMessageValue.value = error.message;
    }
  };

  const classDisabled = computed(() => {
    return isFormValid.value
      ? 'w-full bg-blue-800 text-white px-6 py-3 font-xl rounded-md sm:mb-0 transition'
      : 'w-full  text-white bg-slate-950 px-6 py-3 font-xl rounded-md sm:mb-0 transition';
  });
</script>

<template>
  <form id="contactForm" @submit.prevent="formSubmit">
    <div class="mb-6">
      <div class="mx-0 mb-1 sm:mb-4">
        <div class="mx-0 mb-1 sm:mb-4">
          <label
            for="name"
            class="pb-1 text-xs uppercase tracking-wider"
          ></label
          ><input
            type="text"
            id="name"
            autocomplete="given-name"
            placeholder="Ваше имя"
            class="mb-2 w-full rounded-md border border-gray-400 py-2 pl-2 pr-4 shadow-md dark:text-gray-300 sm:mb-0"
            name="name"
            v-model="inputNameValue"
          />
        </div>
        <div class="mx-0 mb-1 sm:mb-4">
          <label
            for="email"
            class="pb-1 text-xs uppercase tracking-wider"
          ></label
          ><input
            type="email"
            id="email"
            autocomplete="email"
            placeholder="Ваш email"
            class="mb-2 w-full rounded-md border border-gray-400 py-2 pl-2 pr-4 shadow-md dark:text-gray-300 sm:mb-0"
            name="email"
            v-model="inputEmailValue"
          />
        </div>
      </div>
      <div class="mx-0 mb-1 sm:mb-4">
        <label
          for="textarea"
          class="pb-1 text-xs uppercase tracking-wider"
        ></label
        ><textarea
          id="textarea"
          name="textarea"
          cols="30"
          rows="5"
          placeholder="Введите сообщение"
          class="mb-2 w-full rounded-md border border-gray-400 py-2 pl-2 pr-4 shadow-md dark:text-gray-300 sm:mb-0"
          v-model="inputMessageValue"
        ></textarea>
      </div>
    </div>
    <div class="text-center">
      <button
        type="submit"
        class="w-full bg-blue-800 text-white px-6 py-3 font-xl rounded-md sm:mb-0 transition"
        :disabled="!isFormValid"
      >
        {{ isFormValid ? 'Отправить заявку' : 'Заполните поля' }}
      </button>
    </div>
  </form>
</template>
