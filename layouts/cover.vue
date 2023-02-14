<template>
  <div class="slidev-layout cover">
    <div class="my-auto w-full h-full flex flex-col">
      <div class="flex-1">
        <h1><slot/></h1>
        <h2 class="uppercase"><slot name="subtitle"/></h2>
      </div>
      <div class="flex-none">
        <slot name="footer" />
      </div>
    </div>
  </div>
</template>
