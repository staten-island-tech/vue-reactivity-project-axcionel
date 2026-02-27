<template>
    <div class="player-card">
        <img :src="player.image" class="image" />
        <span>{{ player.name }} - {{ player.position }}</span>
        <div> ${{ player.salary }}</div>
        <slot></slot>
    </div>
</template>
<script>
defineProps({
  player: {
    type: Object,
    required: true,
  },
})
</script>
<style>
</style>