<script setup lang="ts">
import { computed } from 'vue'
import { handleBackground, buildTags} from '../helpers'
const props = defineProps({
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
      
      <span class="demo-icon">🖥️</span>
    </div>
  </div>
</template>
