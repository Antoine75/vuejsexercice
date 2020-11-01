<template>
<h1>Liste des joueurs de {{ playersData.team }} </h1>
  <div>
 <player-card
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