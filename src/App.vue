<template>
  <div>
    <div v-for="(value, key) in obj">
      <span>{{key}}</span>: {{ value.toFixed() }}
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  setup() {
    const obj: Record<'key1' | 'key2', number> = {
      key1: 1,
      key2: 2,
    }

    return { obj }
  }
})
</script>
