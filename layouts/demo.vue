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
        <h1>DEMO</h1>
        <h2>{{name}}</h2>
      
      <span v-motion-roll-visible-once-bottom class="demo-icon">🖥️</span>
    </div>
  </div>
</template>
