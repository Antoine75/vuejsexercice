<template>
<h1>Liste des joueurs de {{ playersData.name }} </h1>
  <div class="">
 <player-card class="bg-red-600"
    v-for="(player, index) in team"
    :key="index"
    :player="player"
    @add-player="addPlayerToSelection"
    >
  </player-card>

  </div>
</template>

<script>
import PlayerCard from '../PlayerCard'
import playersData from '../../assets/data/playerManchester.json'

export default {
    name: "manchester-list",
  
  components : {
  PlayerCard,
  
  },
   data() {
    return {
      playersData : playersData,
      team: playersData.players,
      selection: []
    }
  }, 
  
 

}
</script>

<style>

</style>