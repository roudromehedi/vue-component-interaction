<script setup>
const props = defineProps(["message"]);
const emit = defineEmits(["update:modelValue"]);

function messageEmitted() {
  props.name = emit("update:message", "Let's start learning!");
}
</script>

<template>
  <div
    class="ml-2 max-w-sm p-6 bg-white border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700"
  >
    <div
      class="relative w-10 h-10 overflow-hidden bg-gray-100 rounded-full dark:bg-gray-600"
    >
      <svg
        class="absolute w-12 h-12 text-gray-400 -left-1"
        fill="currentColor"
        viewBox="0 0 20 20"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          fill-rule="evenodd"
          d="M10 9a3 3 0 100-6 3 3 0 000 6zm-7 9a7 7 0 1114 0H3z"
          clip-rule="evenodd"
        ></path>
      </svg>
    </div>

    <a href="#">
      <h5
        class="mb-2 mt-2 text-2xl font-semibold tracking-tight text-gray-900 dark:text-white"
      >
        Child Component
      </h5>
    </a>
    <p class="mb-3 font-normal text-gray-500 dark:text-gray-400">
      {{ message }}
    </p>

    <button
      @click="messageEmitted()"
      class="bg-blue-500 hover:bg-blue-700 text-white font-bold my-8 py-2 px-4 rounded"
    >
      Button
    </button>
  </div>
</template>

<style scoped></style>
