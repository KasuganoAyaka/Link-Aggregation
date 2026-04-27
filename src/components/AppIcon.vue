<script setup>
import { computed, h } from 'vue'
import {
  BookOpenText,
  Camera,
  Clapperboard,
  FolderGit2,
  Gamepad2,
  Github,
  HeartHandshake,
  Mail,
  MoonStar,
  Music4,
  Palette,
  Podcast,
  ScrollText,
  Send,
  Sparkles,
  SunMedium,
  Copy,
  ArrowUpRight,
  ScanLine
} from 'lucide-vue-next'

const XBrand = {
  render() {
    return h(
      'svg',
      {
        viewBox: '0 0 24 24',
        fill: 'none',
        'aria-hidden': 'true'
      },
      [
        h('path', {
          fill: 'currentColor',
          d: 'M18.244 3h2.915l-6.367 7.277L22.28 21h-5.863l-4.59-6.56L6.085 21H3.168l6.81-7.783L2.8 3h6.012l4.15 5.934L18.244 3Zm-1.023 16.254h1.615L7.93 4.66H6.197l11.024 14.594Z'
        })
      ]
    )
  }
}

const NetworkDrive = {
  render() {
    return h(
      'svg',
      {
        viewBox: '0 0 24 24',
        fill: 'none',
        'aria-hidden': 'true'
      },
      [
        h('rect', {
          x: '4',
          y: '6',
          width: '16',
          height: '8',
          rx: '2.5',
          stroke: 'currentColor',
          'stroke-width': '1.9'
        }),
        h('path', {
          d: 'M7 18h10',
          stroke: 'currentColor',
          'stroke-width': '1.9',
          'stroke-linecap': 'round'
        }),
        h('path', {
          d: 'M12 14v4',
          stroke: 'currentColor',
          'stroke-width': '1.9',
          'stroke-linecap': 'round'
        }),
        h('circle', {
          cx: '16.5',
          cy: '10',
          r: '0.9',
          fill: 'currentColor'
        }),
        h('circle', {
          cx: '13.5',
          cy: '10',
          r: '0.9',
          fill: 'currentColor'
        })
      ]
    )
  }
}

const QQBrand = {
  render() {
    return h(
      'svg',
      {
        viewBox: '0 0 64 64',
        fill: 'none',
        'aria-hidden': 'true'
      },
      [
        h('ellipse', { cx: '32', cy: '57', rx: '18', ry: '5', fill: 'currentColor', opacity: '0.16' }),
        h('ellipse', { cx: '32', cy: '31', rx: '20', ry: '25', fill: 'currentColor' }),
        h('ellipse', { cx: '32', cy: '36', rx: '14', ry: '18', fill: '#ffffff' }),
        h('path', {
          d: 'M11 38c-2 4-4 9-4 13 0 1.2.9 2 2 1.8 2.6-.4 5.8-4.4 7.8-9.3L11 38Z',
          fill: 'currentColor'
        }),
        h('path', {
          d: 'M53 38c2 4 4 9 4 13 0 1.2-.9 2-2 1.8-2.6-.4-5.8-4.4-7.8-9.3L53 38Z',
          fill: 'currentColor'
        }),
        h('path', {
          d: 'M11.5 29.5c7.2 2.2 14.2 3.3 20.5 3.3 6.2 0 13.1-1.1 20.5-3.3v8.3c-6.8 2-13.7 3-20.5 3-6.7 0-13.6-1-20.5-3v-8.3Z',
          fill: 'currentColor'
        }),
        h('rect', {
          x: '28.2',
          y: '33',
          width: '7.6',
          height: '15',
          rx: '1.4',
          fill: 'currentColor'
        }),
        h('ellipse', { cx: '32', cy: '25.5', rx: '10', ry: '4.4', fill: 'currentColor' }),
        h('ellipse', { cx: '25.8', cy: '19.6', rx: '3.5', ry: '5', fill: '#ffffff' }),
        h('ellipse', { cx: '38.2', cy: '19.6', rx: '3.5', ry: '5', fill: '#ffffff' }),
        h('circle', { cx: '26.8', cy: '20.3', r: '1.7', fill: '#ffffff' }),
        h('path', {
          d: 'M36.5 20.6c.9-1.7 2.8-2.4 4.3-1.7 1.6.7 2.2 2.5 1.5 4.2-.6 1.6-2.4 2.7-4 2.4',
          stroke: '#ffffff',
          'stroke-width': '1.8',
          'stroke-linecap': 'round'
        })
      ]
    )
  }
}

const DiscordBrand = {
  render() {
    return h(
      'svg',
      {
        viewBox: '0 0 64 64',
        fill: 'none',
        'aria-hidden': 'true'
      },
      [
        h('path', {
          d: 'M21.5 18.5c7.1-3.1 13.9-3.1 21 0l1.4 3.2c4 1.1 6.5 3.9 7.6 8.8.9 4.4.7 8.9-.7 13.5-4.1 3.2-8.3 5.2-12.8 6.1l-2.6-3.9c1.8-.6 3.5-1.3 5.1-2.3-1.1.8-2.5 1.5-4 1.9-3 .9-6.1 1.4-9.4 1.4-3.2 0-6.3-.5-9.4-1.4-1.5-.4-2.9-1.1-4-1.9 1.6 1 3.3 1.7 5.1 2.3L16.2 50c-4.5-.9-8.7-2.9-12.8-6.1-1.4-4.6-1.6-9.1-.7-13.5 1.1-4.9 3.6-7.7 7.6-8.8l1.2-3.2Z',
          fill: 'currentColor'
        }),
        h('path', {
          d: 'M18.8 40.2c4.1 2.8 8.4 4.2 13.2 4.2 4.8 0 9.1-1.4 13.2-4.2',
          stroke: '#ffffff',
          'stroke-width': '2.6',
          'stroke-linecap': 'round',
          opacity: '0.95'
        }),
        h('circle', {
          cx: '23.5',
          cy: '31.6',
          r: '3.3',
          fill: '#ffffff'
        }),
        h('circle', {
          cx: '40.5',
          cy: '31.6',
          r: '3.3',
          fill: '#ffffff'
        }),
        h('path', {
          d: 'M22 21.5 18.2 25',
          stroke: '#ffffff',
          'stroke-width': '2.4',
          'stroke-linecap': 'round'
        }),
        h('path', {
          d: 'M42 21.5 45.8 25',
          stroke: '#ffffff',
          'stroke-width': '2.4',
          'stroke-linecap': 'round'
        })
      ]
    )
  }
}

const BowlFood = {
  render() {
    return h(
      'svg',
      {
        viewBox: '0 0 24 24',
        fill: 'none',
        'aria-hidden': 'true'
      },
      [
        h('path', {
          d: 'M5 11.5h14c0 4.3-3.1 7-7 7s-7-2.7-7-7Z',
          stroke: 'currentColor',
          'stroke-width': '1.9',
          'stroke-linejoin': 'round'
        }),
        h('path', {
          d: 'M4 11.5h16',
          stroke: 'currentColor',
          'stroke-width': '1.9',
          'stroke-linecap': 'round'
        }),
        h('path', {
          d: 'M9 8c0-1.4.8-2 1.4-2.7.6-.7 1.1-1.3 1.1-2.5',
          stroke: 'currentColor',
          'stroke-width': '1.7',
          'stroke-linecap': 'round'
        }),
        h('path', {
          d: 'M13 8.6c0-1 .5-1.5 1-2.1.5-.5.9-1 .9-2',
          stroke: 'currentColor',
          'stroke-width': '1.7',
          'stroke-linecap': 'round'
        }),
        h('path', {
          d: 'M8.5 19h7',
          stroke: 'currentColor',
          'stroke-width': '1.9',
          'stroke-linecap': 'round'
        })
      ]
    )
  }
}

const BilibiliBrand = {
  render() {
    return h(
      'svg',
      {
        viewBox: '0 0 64 64',
        fill: 'none',
        'aria-hidden': 'true'
      },
      [
        h('path', {
          d: 'M22 14 28 20',
          stroke: 'currentColor',
          'stroke-width': '4',
          'stroke-linecap': 'round'
        }),
        h('path', {
          d: 'M42 14 36 20',
          stroke: 'currentColor',
          'stroke-width': '4',
          'stroke-linecap': 'round'
        }),
        h('rect', {
          x: '14',
          y: '20',
          width: '36',
          height: '26',
          rx: '6',
          stroke: 'currentColor',
          'stroke-width': '4'
        }),
        h('path', {
          d: 'M24 28v10',
          stroke: 'currentColor',
          'stroke-width': '4',
          'stroke-linecap': 'round'
        }),
        h('path', {
          d: 'M40 28v10',
          stroke: 'currentColor',
          'stroke-width': '4',
          'stroke-linecap': 'round'
        }),
        h('path', {
          d: 'M22 50h20',
          stroke: 'currentColor',
          'stroke-width': '4',
          'stroke-linecap': 'round'
        })
      ]
    )
  }
}

const props = defineProps({
  name: {
    type: String,
    default: 'sparkles'
  }
})

const iconMap = {
  arrowUpRight: ArrowUpRight,
  bookOpenText: BookOpenText,
  bilibiliBrand: BilibiliBrand,
  bowlFood: BowlFood,
  camera: Camera,
  clapperboard: Clapperboard,
  copy: Copy,
  discordBrand: DiscordBrand,
  folderGit2: FolderGit2,
  gamepad2: Gamepad2,
  github: Github,
  heartHandshake: HeartHandshake,
  mail: Mail,
  moonStar: MoonStar,
  music4: Music4,
  networkDrive: NetworkDrive,
  palette: Palette,
  podcast: Podcast,
  qqBrand: QQBrand,
  scanLine: ScanLine,
  scrollText: ScrollText,
  send: Send,
  sparkles: Sparkles,
  sunMedium: SunMedium,
  xBrand: XBrand
}

const component = computed(() => iconMap[props.name] || Sparkles)
</script>

<template>
  <component :is="component" />
</template>
