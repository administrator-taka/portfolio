<template>
  <section class="py-2">
    <div class="card shadow-sm mb-4 w-100">
      <div class="card-body">
        <h3 class="my-3">
          {{ title }}
        </h3>
        <div class="m-2">
          <slot />
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { computed, defineProps } from 'vue'
const props = defineProps<{ title: string }>()
const title = computed(() => props.title)
</script>

<style scoped></style>
