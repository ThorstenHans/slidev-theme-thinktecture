<script setup lang="ts">

defineProps({
    name: {
        type: String,
    },
})

</script>

<template>
  <div class="slidev-layout demo h-full grid place-content-center">
    <div class="my-auto flex flex-col justify-center items-center">
        <h2 class="uppercase">Demo</h2>
        <h1>{{name}}</h1>
        <uim-airplay class="pt-7 text-8xl accent animate-ping" />
    </div>
  </div>
</template>
