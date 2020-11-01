<template>
 
<h1>Liste des joueurs de {{ playersData.name }} </h1>

  

  <player-card class="flex content-center flex-wrap"
    v-for="(player, index) in team"
    :key="index"
    :player="player"
    @add-player="addPlayerToSelection"
    >
  </player-card>
</template>

<script>
import playersData from '../assets/data/players.json'
import PlayerCard from './PlayerCard.vue'


export default {
  name: "player-List",
  components: {
    PlayerCard,
   
    
  },
  data() {
    return {
      playersData : playersData,
      team: playersData.players,
      selection: []
    }
  },
  methods: {
    addPlayerToSelection(player) {
      this.selection.push(player)
      this.$emit('update-selection', player)
    },
    selectTeam(selectedTeam){
      const newTeam = this.player.filter(player=>{player.team == selectedTeam})
      console.log(newTeam)
      this.team = newTeam
    }
  }
}
</script>

<style>

</style>