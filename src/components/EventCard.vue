<script setup lang="ts">
import { type Event } from '@/types'

defineProps<{
  event: Event
}>()
</script>

<template>
  <RouterLink
    class="event-link"
    :to="{ name: 'event-detail-view', params: { id: event.id } }"
  >
  <div class="cursor-pointer border border-gray-600 p-[20px] w-[250px] mb-[18px] hover:scale-101 hover:shadow-sp">
      <h2>{{ event.title }}</h2>
      <span>@{{ event.time }} on {{ event.date }}</span>
    </div>
  </RouterLink>
</template>

<style scoped>
.event-card {
  padding: 20px;
  width: 250px;
  cursor: pointer;
  border: 1px solid #00f010;
  margin-bottom: 18px;
}
.event-card:hover {
  transform: scale(1.01);
  box-shadow: 0 3px 12px 0 rgba(245, 3, 3, 0.972);
}
.event-link {
  text-decoration: none;
  color: #bcf60d;
}
</style>
