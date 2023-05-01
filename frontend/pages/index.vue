<template>
    <div>
      <h1 class="font-bold">If this is bold, Tailwind is working!</h1>
        <p>Count : {{ count }}
            <button @click="exampleStore.increment" type="submit" class="bg-black text-white font-bold px-2 mx-2 rounded">+</button>
            if the count is incrementing, pinia is working!
        </p>
      <NuxtWelcome />
    </div>
</template>

<script lang="ts" setup>
    import { useIncrementStore } from '~/store/increment';
    import { storeToRefs } from 'pinia';

    const exampleStore = useIncrementStore();

    const { count } = storeToRefs(exampleStore);    
</script>
  