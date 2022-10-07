<script setup>
import ModalExample from './examples/ModalExample.vue';
import ModalSizeExample from './examples/ModalSizeExample.vue';
</script>
# Vue Modal Component - Flowbite

## Demo

<ModalExample />

```vue
<script setup>
import { Modal } from 'flowbite-vue'
</script>
<template>
  <Modal>
    <template #trigger="props">
      <button @click="props.show()" type="button" class="mt-5 text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">
        Show Modal
      </button>
    </template>
    <template #header="props">
      <div class="flex justify-between">
        <div class="flex items-center text-lg">
          Terms of Service
        </div>
        <div>
          <button @click="props.hide()" type="button" class="text-gray-400 bg-transparent hover:bg-gray-200 hover:text-gray-900 rounded-lg text-sm p-1.5 ml-auto inline-flex items-center dark:hover:bg-gray-600 dark:hover:text-white">
            <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z" clip-rule="evenodd"></path></svg>
          </button>
        </div>
      </div>
    </template>
    <template v-slot:body>
      <p class="text-base leading-relaxed text-gray-500 dark:text-gray-400">
        With less than a month to go before the European Union enacts new consumer privacy laws for its citizens, companies around the world are updating their terms of service agreements to comply.
      </p>
      <p class="text-base leading-relaxed text-gray-500 dark:text-gray-400">
        The European Union’s General Data Protection Regulation (G.D.P.R.) goes into effect on May 25 and is meant to ensure a common set of data rights in the European Union. It requires organizations to notify users as soon as possible of high-risk data breaches that could personally affect them.
      </p>
    </template>
    <template #footer="props">
      <div class="flex justify-between">
        <button @click="props.hide()" type="button" class="text-gray-500 bg-white hover:bg-gray-100 focus:ring-4 focus:outline-none focus:ring-blue-300 rounded-lg border border-gray-200 text-sm font-medium px-5 py-2.5 hover:text-gray-900 focus:z-10 dark:bg-gray-700 dark:text-gray-300 dark:border-gray-500 dark:hover:text-white dark:hover:bg-gray-600 dark:focus:ring-gray-600">
          Decline
        </button>
        <button @click="props.hide()" type="button" class="text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">
          I accept
        </button>
      </div>
    </template>
  </Modal>
</template>
```

## Slot Properties 

Modal slots receive the following functions to interact with the modal:
1. `show` = show the modal 
2. `hide` = hide the modal 
3. `toggle` = toggles the modal from current state (e.g. if shown, then hide)

These properties allow your code to set the open/closed state of the modal easily. 

## Sizes 

The modal can come in the following sizes (based on TailwindCSS classes).

`xs`, `sm`, `md`, `lg`, `xl`, `2xl`, `3xl`, `4xl`, `5xl`, `6xl`, `7xl`

The default value is: `2xl`

Demo: 

<ModalSizeExample/>

```vue
<script setup>
import { Modal } from 'flowbite-vue'
</script>
<template>
    <Modal size="xs" />
    <Modal size="md" />
    <Modal size="xl" />
    <Modal size="5xl" />
</template>
```