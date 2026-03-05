<template>
    <div class="player-card">
        <img :src="player.image"/>
        <div>{{ player.name }} - {{ player.position }}</div>
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