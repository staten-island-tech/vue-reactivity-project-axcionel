<template>
    <div class="player-card">
        <img :src="player.image" class="image" />
        <span class="player-card">{{ player.name }} - {{ player.position }}</span>
        <div> ${{ player.salary }}</div>
        <slot></slot>
    </div>
</template>
<script setup>
defineProps({
  player: {
    type: Object,
    required: true,
  },
})
</script>
<style>
</style>