<script setup lang="ts">

export interface Link {
    name: string
    url: string
}
export interface Props {
    red: boolean
    links: Array<Link> | null
}

withDefaults(defineProps<Props>(), {
    links: new Array<Link>(),
    red: false
})

</script>
<template>
    <div class="slidev-layout closing text-center" :class="{ alternative: red}">
        <div class="my-auto h-full flex flex-col">
            <h1>Thank you</h1>
            <div class="links flex-1">
                <span v-if="links" v-for="(link, index) in links">
                    <a v-bind:href="link.url" target="_blank">{{ link.name }}</a>
                    <span v-if="index < links.length-1"> | </span>
                </span>
            </div>
            <div class="footer">
                <slot name="footer"></slot>
            </div>
        </div>
    </div>
</template>
