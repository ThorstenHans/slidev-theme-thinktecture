<template>
  <div class="slidev-layout two-columns">
    <div class="my-auto w-full">
      <slot />
      <div class="flex flex-row">
        <div class="flex-1">
          <slot name="left" />
        </div>
        <div class="flex-1">
          <slot name="right" />
        </div>
        </div>
      
    </div>
  </div>
</template>
