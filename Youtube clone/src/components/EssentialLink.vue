<template>
  <q-item
    clickable
    tag="a"
    target="_blank"
    :href="props.link"
    style="width: 80px; "
  >
    <q-item-section
      v-if="props.icon"
      avatar
      style="display: flex; flex-direction: column; gap: 6px; align-items: center;"
    >
      <q-icon :name="props.icon" />
      {{ props.title }}
    </q-item-section>
  </q-item>
</template>

<script setup>
defineOptions({
  name: 'EssentialLink'
})
const props = defineProps({
  title: {
    type: String,
    required: true
  },

  caption: {
    type: String,
    default: ''
  },

  link: {
    type: String,
    default: '#'
  },

  icon: {
    type: String,
    default: ''
  }
})
</script>
