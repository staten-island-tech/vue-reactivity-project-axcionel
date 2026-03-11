<template>
  <div class="sidebar">
    <h1>Team</h1>
    <ul>
      <li v-for="player in team" :key="player.name">
        {{ player.name }} - {{ player.position }} - ${{ player.salary.toLocaleString() }}
        <button @click="removePlayer(player)">X</button>
      </li>
      <div>Total: ${{ calculateTotal(team) }}</div>
    </ul>
    </div>
</template>

<script setup>
const props = defineProps({
  team: {
    type: Array,
    required: true,
    default: () => []
  },
  removePlayer: {
    type: Function,
    required: true
  }
});


function calculateTotal(teamArray) {
  const total = teamArray.reduce((sum, player) => sum + (player.salary || 0), 0);
  return total.toLocaleString();
}

</script>

<style scoped>
.sidebar {
  position: fixed;
  top: 0;
  right: 0;
  width: 17%;
  height: 100%;
  background-color: #ffffff;
  line-height: 1.5rem; 
  padding: 1rem;
  display: flex;
  flex-direction: column;
  overflow-y: auto;
  border: 2px solid black;
}
</style>