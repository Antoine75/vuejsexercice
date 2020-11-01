<template>
  <player-list></player-list>
 
  
</template>

<script>
import PlayerList from './components/PlayerList.vue'


export default {
  name: 'App',
  components: {
    PlayerList

    
  },
  data() {
    return {
      selectedComponent: 'player-list',
      selectionArray: []
    }
  },
  computed: {
    currentProps() {
      if(this.selectedComponent == "selection-list") {
        return { selection: this.selectionArray }
      }
      return false
    }
  },
  methods: {
    updateSelectedComponent(comp) {
      this.selectedComponent = comp
    },
    updateSelection(player) {
      this.selectionArray.push(player)
    }
  }
}
 

</script>
<style>

</style>
