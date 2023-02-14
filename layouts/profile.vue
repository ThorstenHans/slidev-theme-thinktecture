<script setup lang="ts">
import { computed } from 'vue'
import { handleBackground} from '../helpers'

export interface Blog {
  name: string
  url: string
}

export interface Props {
  speaker: string
  twitter: string
  image: string
  tags: string[]
  awards: string[]
  welcome?: string
  job?: string
  mail?: string
  blog?: Blog
}
const props = withDefaults(defineProps<Props>(), {
  welcome: 'Hi 👋🏼',
  twitter: 'thinktecture',
  job: 'Hausmeister',
  mail: 'office@thinktecture.com',
  blog: null,
  tags: [],
  awards: []
})

const style = computed(() => handleBackground(props.image))
</script>

<template>
  <div class="grid grid-cols-3 w-full h-full auto-rows-fr">
    <div class="slidev-layout profile col-span-2 flex flex-col" :class="props.class">
      <h1>{{ welcome }}, I'm {{ speaker }}</h1>
      <p>{{ job }} @ Thinktecture</p>
        
      <div class="focus">
        <h3>Technology Focus</h3>
        <div class="tags">
          <div class="tag" v-for="item in tags">
            <span class="accent">#</span>{{ item }}
          </div>
        </div>
      </div>
      
      <div class="awards flex-1">
        <h3>Awards</h3>
        <ul>
          <li v-for="item in awards">{{ item }}
          </li>
        </ul>
      </div>
      
      <div class="contact flex-none">
        <h3>Contact</h3>

        <a v-if="blog" href="{{ blog.url }}" target="_blank">{{ blog.name }}</a><br/>
        <a href="https://thinktecture.com" target="_blank">thinktecture.com</a><br/>
        <a href="mailto:{{mail}}">{{ mail }}</a><span> | </span><a href="https://twitter.com/{{ twitter }}" target="_blank">@{{ twitter }}</a>
      </div>
    </div>
    <div class="w-full w-full" :style="style" />
  </div>
</template>
