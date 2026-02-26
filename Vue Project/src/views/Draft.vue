<template>
  <h1>2025 Draft</h1>
  <gr class="grid">
    <li v-for="player in draftees" class="player-card">
      <img :src="player.image" class="image" />
      <span class="player-info">{{ player.name }} - {{ player.position }}</span>
      <div> ${{ player.salary }}</div>
    </li>
  </gr>
</template>


<script setup>
import { ref } from 'vue';
const draftees = ref([
  { name: "Cam Ward", salary: 49000000, position: "QB", image: "https://a.espncdn.com/combiner/i?img=/i/headshots/nfl/players/full/4688380.png&w=350&h=254" },
  { name: "Travis Hunter", salary: 47000000, position: "WR", image: "https://a.espncdn.com/combiner/i?img=/i/headshots/nfl/players/full/4685415.png&w=350&h=254" },
  { name: "Abdul Carter", salary: 45000000, position: "DE", image: "https://a.espncdn.com/combiner/i?img=/i/headshots/nfl/players/full/4725996.png&w=350&h=254" },
  { name: "Will Campbell", salary: 44000000, position: "OT", image: "https://a.espncdn.com/combiner/i?img=/i/headshots/nfl/players/full/4685298.png&w=350&h=254" },
  { name: "Mason Graham", salary: 41000000, position: "DT", image: "https://a.espncdn.com/combiner/i?img=/i/headshots/nfl/players/full/4873232.png&w=350&h=254" },
  { name: "Ashton Jeanty", salary: 36000000, position: "RB", image: "https://a.espncdn.com/combiner/i?img=/i/headshots/nfl/players/full/4890973.png&w=350&h=254" },
  { name: "Armand Membou", salary: 32000000, position: "OT", image: "https://a.espncdn.com/combiner/i?img=/i/headshots/nfl/players/full/4789907.png&w=350&h=254" },
  { name: "Tetairoa McMillan", salary: 28000000, position: "WR", image: "https://a.espncdn.com/combiner/i?img=/i/headshots/nfl/players/full/4685472.png&w=350&h=254" },
  { name: "Kelvin Banks Jr.", salary: 28000000, position: "OT", image: "https://a.espncdn.com/combiner/i?img=/i/headshots/nfl/players/full/4685260.png&w=350&h=254" },
  { name: "Colston Loveland", salary: 27000000, position: "TE", image: "https://a.espncdn.com/combiner/i?img=/i/headshots/nfl/players/full/4723086.png&w=350&h=254" },
  { name: "Mykel Williams", salary: 25000000, position: "DE", image: "https://a.espncdn.com/combiner/i?img=/i/headshots/nfl/players/full/4685623.png&w=350&h=254" },
  { name: "Tyler Booker", salary: 23000000, position: "G", image: "https://a.espncdn.com/combiner/i?img=/i/headshots/nfl/players/full/4685263.png&w=350&h=254" },
  { name: "Kenneth Grant", salary: 22000000, position: "DT", image: "https://a.espncdn.com/combiner/i?img=/i/headshots/nfl/players/full/4894654.png&w=350&h=254" },
  { name: "Tyler Warren", salary: 21000000, position: "TE", image: "https://a.espncdn.com/combiner/i?img=/i/headshots/nfl/players/full/4431459.png&w=350&h=254" },
  { name: "Jalon Walker", salary: 21000000, position: "LB", image: "https://a.espncdn.com/combiner/i?img=/i/headshots/nfl/players/full/4685597.png&w=350&h=254" },
  { name: "Walter Nolen", salary: 19000000, position: "DT", image: "https://a.espncdn.com/combiner/i?img=/i/headshots/nfl/players/full/4685503.png&w=350&h=254" },
  { name: "Shemar Stewart", salary: 19000000, position: "DE", image: "https://a.espncdn.com/combiner/i?img=/i/headshots/nfl/players/full/4685562.png&w=350&h=254" },
  { name: "Grey Zabel", salary: 18000000, position: "G", image: "https://a.espncdn.com/combiner/i?img=/i/headshots/nfl/players/full/4693346.png&w=350&h=254" },
  { name: "Emeka Egbuka", salary: 18000000, position: "WR", image: "https://a.espncdn.com/combiner/i?img=/i/headshots/nfl/players/full/4567750.png&w=350&h=254" },
  { name: "Jahdae Barron", salary: 18000000, position: "CB", image: "https://a.espncdn.com/combiner/i?img=/i/headshots/nfl/players/full/4430925.png&w=350&h=254" },
  { name: "Derrick Harmon", salary: 18000000, position: "DT", image: "https://a.espncdn.com/combiner/i?img=/i/headshots/nfl/players/full/4682980.png&w=350&h=254" },
  { name: "Omarion Hampton", salary: 18000000, position: "RB", image: "https://a.espncdn.com/combiner/i?img=/i/headshots/nfl/players/full/4685382.png&w=350&h=254" },
  { name: "Matthew Golden", salary: 18000000, position: "WR", image: "https://a.espncdn.com/combiner/i?img=/i/headshots/nfl/players/full/4701936.png&w=350&h=254" },
  { name: "Donovan Jackson", salary: 17000000, position: "G", image: "https://a.espncdn.com/combiner/i?img=/i/headshots/nfl/players/full/4431553.png&w=350&h=254" },
  { name: "Jaxson Dart", salary: 17000000, position: "QB", image: "https://a.espncdn.com/combiner/i?img=/i/headshots/nfl/players/full/4689114.png&w=350&h=254" },
  { name: "James Pearce Jr.", salary: 17000000, position: "DE", image: "https://a.espncdn.com/combiner/i?img=/i/headshots/nfl/players/full/5081394.png&w=350&h=254" },
  { name: "Malaki Starks", salary: 17000000, position: "S", image: "https://a.espncdn.com/combiner/i?img=/i/headshots/nfl/players/full/4685530.png&w=350&h=254" },
  { name: "Tyleik Williams", salary: 16000000, position: "DT", image: "https://a.espncdn.com/combiner/i?img=/i/headshots/nfl/players/full/4431615.png&w=350&h=254" },
  { name: "Josh Conerly Jr.", salary: 16000000, position: "OT", image: "https://a.espncdn.com/combiner/i?img=/i/headshots/nfl/players/full/4685326.png&w=350&h=254" },
  { name: "Maxwell Hairston", salary: 15000000, position: "CB", image: "https://a.espncdn.com/combiner/i?img=/i/headshots/nfl/players/full/4688931.png&w=350&h=254" },
  { name: "Jihaad Campbell", salary: 15000000, position: "LB", image: "https://a.espncdn.com/combiner/i?img=/i/headshots/nfl/players/full/4685287.png&w=350&h=254" },
  { name: "Josh Simmons", salary: 15000000, position: "OT", image: "https://a.espncdn.com/combiner/i?img=/i/headshots/nfl/players/full/4569659.png&w=350&h=254" }
]);
</script>


<style>
h1 {
    text-align: center;
}
.grid {
    display: flex;
    flex-wrap: wrap; 
    gap: 20px; 
    list-style: none;
    padding: 0;
}
.player-card {
    display: flex;
    flex-direction: column; 
    align-items: center; 
    text-align: center; 
    gap: 8px;
    flex: 0 0 calc(25% - 20px); 
}
.image {
    object-fit: cover;
    border-radius: 10px;
}
</style>