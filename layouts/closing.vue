<script setup lang="ts">

export interface Link {
  name: string
  url: string
}
export interface Props {
  link1: Link
  link2: Link
}
const props = withDefaults(defineProps<Props>(), {
  link1: null,
  link2: null,
})
</script>
<template>
  <div class="slidev-layout closing text-center">
    <div class="my-auto h-full flex flex-col">
      <h1>Thank you</h1>
      <div class="links flex-1">
        <span v-if="link1">
          <a href="{{ link1.url }}" target="_blank">{{ link1.name }}</a>
        </span>
        <span> | </span>
        <span v-if="link2">
          <a href="{{ link2.url }}" target="_blank">{{ link2.name }}</a>
        </span>
      </div>
      <div class="footer">
        <slot name="footer"></slot>
      </div>
    </div>
  </div>
</template>
