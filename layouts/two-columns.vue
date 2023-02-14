<template>
  <div class="slidev-layout twocols">
    <div class="my-auto w-full">
      <slot />
      <template v-slot:left>
      </template>
      <template v-slot:right>
      </template>
    </div>
  </div>
</template>
