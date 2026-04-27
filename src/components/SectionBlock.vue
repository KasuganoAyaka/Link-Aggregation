<script setup>
import LinkCard from './LinkCard.vue'

defineProps({
  section: {
    type: Object,
    required: true
  },
  offset: {
    type: Number,
    default: 0
  }
})
</script>

<template>
  <section :id="section.id" class="section-block">
    <header class="section-block__header">
      <p>{{ section.subtitle }}</p>
      <h2>{{ section.title }}</h2>
    </header>

    <div class="section-block__cards">
      <LinkCard
        v-for="(link, index) in section.links"
        :key="`${section.id}-${link.title}`"
        :link="link"
        :delay="offset + index * 70"
      />
    </div>
  </section>
</template>
