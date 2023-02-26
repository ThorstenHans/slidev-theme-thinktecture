<script setup lang="ts">

export interface Props {
    red: boolean
}

withDefaults(defineProps<Props>(), {
    red: false
})

</script>
<template>
  <div class="slidev-layout cover" :class="{ alternative: red}">
    <div class="my-auto w-full h-full flex flex-col">
      <div class="flex-1">
        <slot/>
        <slot name="subtitle"/>
      </div>
      <div class="flex-none">
        <slot name="footer" />
      </div>
    </div>
    <div class="logo"/>
  </div>
</template>
