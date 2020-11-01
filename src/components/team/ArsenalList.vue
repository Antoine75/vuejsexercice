<template>
<h1 class="p-3">Liste des joueurs de {{ playersData.name }} </h1>

  <div class="p-5 flex content-start pr-1">
 <player-card class="bg-red-200"
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
import playersData from '../../assets/data/playerArsenal.json'

export default {
    name: "arsenal-list",
  
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