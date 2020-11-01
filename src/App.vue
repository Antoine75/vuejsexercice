<template>
  <nav-bar
    @change-component="updateSelectedComponent">
    
  </nav-bar>
  <keep-alive>
    <component :is="selectedComponent"
    v-bind="currentProps"></component>
    </keep-alive>
 
  
  
</template>

<script>
import PlayerList from './components/PlayerList.vue'
import NavBar from './components/navigation/NavBar'
import ChelseaList from './components/team/ChelseaList.vue'
import TottenhamList from './components/team/TottenhamList.vue'
import ArsenalList from './components/team/ArsenalList.vue'
import ManchesterList from './components/team/ManchesterList.vue'


export default {
  name: 'App',
  components: {
    PlayerList,
    NavBar,
    ChelseaList,
    TottenhamList,
    ArsenalList,
    ManchesterList,
    
  },
  data() {
    return {
      selectedComponent: 'player-list',
      selectionArray: []
    }
  },
  computed: {
    currentProps() {
      if(this.selectedComponent == "chelsea-list") {
        return { selection: this.selectionArray }
      }
      if(this.selectedComponent == "arsenal-list") {
        return { selection: this.selectionArray }
      }
      if(this.selectedComponent == "manchester-list") {
        return { selection: this.selectionArray }
      }
      if(this.selectedComponent == "tottenham-list") {
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
