<script setup>
import { computed, onMounted, ref, watch } from 'vue'
import AppIcon from '@/components/AppIcon.vue'
import SectionBlock from '@/components/SectionBlock.vue'
import { profile, quickLinks, sections } from '@/data/site'

const themeKey = 'anime-link-hub-theme'
const currentTheme = ref('sky')
const copyState = ref('idle')

const themeIcon = computed(() => (currentTheme.value === 'sky' ? 'moonStar' : 'sunMedium'))
const shareLabel = computed(() => {
  if (copyState.value === 'done') return '已复制链接'
  if (copyState.value === 'error') return '复制失败'
  return '复制页面链接'
})
const copyToastText = computed(() => {
  if (copyState.value === 'done') return '链接已复制'
  if (copyState.value === 'error') return '复制失败，请手动复制地址'
  return ''
})

const applyTheme = (theme) => {
  document.documentElement.dataset.theme = theme
}

const toggleTheme = () => {
  currentTheme.value = currentTheme.value === 'sky' ? 'dusk' : 'sky'
}

const openQuickLink = (url) => {
  window.open(url, '_blank', 'noopener,noreferrer')
}

const copyCurrentUrl = async () => {
  try {
    await navigator.clipboard.writeText(window.location.href)
    copyState.value = 'done'
    window.setTimeout(() => {
      copyState.value = 'idle'
    }, 1800)
  } catch (error) {
    copyState.value = 'error'
    window.setTimeout(() => {
      copyState.value = 'idle'
    }, 2200)
    console.error('复制链接失败:', error)
  }
}

watch(currentTheme, (theme) => {
  applyTheme(theme)
  window.localStorage.setItem(themeKey, theme)
})

onMounted(() => {
  const savedTheme = window.localStorage.getItem(themeKey)
  if (savedTheme === 'sky' || savedTheme === 'dusk') {
    currentTheme.value = savedTheme
  }
  applyTheme(currentTheme.value)
})
</script>

<template>
  <div class="page-shell">
    <div class="ambient ambient--mint"></div>
    <div class="ambient ambient--lavender"></div>
    <div class="ambient ambient--cloud"></div>

    <main class="linkboard">
      <section class="hero-card">
        <div class="hero-card__confetti" aria-hidden="true">
          <span class="shape shape--star"></span>
          <span class="shape shape--bar"></span>
          <span class="shape shape--dot"></span>
          <span class="shape shape--ribbon"></span>
          <span class="shape shape--heart"></span>
          <span class="shape shape--spark"></span>
        </div>

        <div class="hero-card__actions">
          <button type="button" class="utility-button" :aria-label="shareLabel" @click="copyCurrentUrl">
            <AppIcon name="copy" />
          </button>
          <button type="button" class="utility-button" aria-label="切换主题" @click="toggleTheme">
            <AppIcon :name="themeIcon" />
          </button>
          <transition name="copy-toast">
            <div v-if="copyState !== 'idle'" class="copy-toast" :class="`copy-toast--${copyState}`">
              {{ copyToastText }}
            </div>
          </transition>
        </div>

        <div class="avatar-orbit">
          <div class="avatar-ring avatar-ring--outer"></div>
          <div class="avatar-ring avatar-ring--inner"></div>
          <div class="avatar-core">
            <img :src="profile.avatar" :alt="profile.name" />
          </div>
        </div>

        <p class="hero-card__handle">{{ profile.handle }}</p>
        <p class="hero-card__tagline">{{ profile.tagline }}</p>
        <p class="hero-card__intro">{{ profile.intro }}</p>
        <div class="status-pill">
          <span class="status-pill__light"></span>
          <span class="status-pill__text">
            <span class="status-pill__face status-pill__face--front">{{ profile.status.en }}</span>
            <span class="status-pill__face status-pill__face--back">{{ profile.status.zh }}</span>
          </span>
        </div>

        <nav class="quick-links" aria-label="Quick links">
          <button
            v-for="item in quickLinks"
            :key="item.label"
            type="button"
            class="quick-links__item"
            :aria-label="item.label"
            :title="item.label"
            @click="openQuickLink(item.href)"
          >
            <AppIcon :name="item.icon" />
          </button>
        </nav>
      </section>

      <SectionBlock
        v-for="(section, index) in sections"
        :key="section.id"
        :section="section"
        :offset="index * 140"
      />

      <footer class="page-footer">
        <p>感谢你的来访，愿这里也能成为你抵达我小宇宙的一条柔软路径。</p>
        <p>© 2026 Ayaka · Link Hub. 保留所有权利。</p>
      </footer>
    </main>
  </div>
</template>
