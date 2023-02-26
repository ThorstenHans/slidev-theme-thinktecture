<script setup lang="ts">

defineProps({
    name: {
        type: String,
    },
})

</script>
<template>
  <div class="slidev-layout section text-center">
    <div class="w-full h-full flex flex-col justify-center">
      <h2 class="uppercase">Section</h2>
      <h1>{{ name }}</h1>
    </div>
  </div>
</template>
