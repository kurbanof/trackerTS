<script setup>
import { currentPage, navigate } from '@/router'
import { PAGE_TIMELINE } from '@/constants'
import { ICON_FIRE } from '@/icons'
import { scrollToCurrentHour } from '@/timeline-items'
import BaseIcon from './UI/BaseIcon.vue'

function handleClick() {
  currentPage.value === PAGE_TIMELINE ? scrollToCurrentHour(true) : navigate(PAGE_TIMELINE)
}
</script>

<template>
  <a
    :href="`#${PAGE_TIMELINE}`"
    class="flex origin-left rounded bg-gray-600 p-1 text-white"
    @click="handleClick"
  >
    <BaseIcon :name="ICON_FIRE" class="mr-2 h-5 w-5" />
    <span>Tt</span>
  </a>
</template>
