<script setup>
import AppIcon from './AppIcon.vue'

defineProps({
  link: {
    type: Object,
    required: true
  },
  delay: {
    type: Number,
    default: 0
  }
})
</script>

<template>
  <a
    class="link-card"
    :href="link.href"
    target="_blank"
    rel="noreferrer"
    :style="{ '--delay': `${delay}ms` }"
  >
    <span class="link-card__shine-bar" aria-hidden="true"></span>

    <div class="link-card__icon">
      <AppIcon :name="link.icon" />
    </div>

    <div class="link-card__body">
      <div class="link-card__heading">
        <h3>{{ link.title }}</h3>
        <span v-if="link.badge" class="link-card__badge">{{ link.badge }}</span>
      </div>
      <p v-if="link.description">{{ link.description }}</p>
    </div>

    <div class="link-card__action" aria-hidden="true">
      <AppIcon name="arrowUpRight" />
    </div>
  </a>
</template>
