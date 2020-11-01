<template>
<h1>Liste des joueurs de {{ playersData.name }} </h1>

  <div>
 <player-card class="bg-blue-200"
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
import playersData from '../../assets/data/playerChelsea.json'

export default {
    name: "chelsea-list",
  
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