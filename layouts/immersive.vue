<script setup lang="ts">

import { computed } from 'vue'
import { handleBackground} from '../helpers'
 
const props = defineProps({
    red: {
        type: Boolean
    },
    image: {
        type: String,
    },
})

const style = computed(() => handleBackground(props.image))
</script>

<template>
  <div class="slidev-layout immersive h-full grid place-content-center text-center" :class="{alternative: red}" :style="style">
    <div class="w-full w-full">
        <slot/>
    </div>
  </div>
</template>
