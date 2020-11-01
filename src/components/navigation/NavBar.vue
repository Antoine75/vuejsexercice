<template>
  <div class="bg-blue-500 p-2">

    <a 
      v-for="(link, index) in navigation"
      :key="index"
      href="#" 
      @click="selectComponent(link.component)" 
    >
      {{ link.name }}  |
        </a>
    
  </div>
  
</template>

<script>
export default {
  name: "nav-bar",
  data() {
    return {
      navigation: [
        { name: "Tous les joueurs", component: "player-list"},
        { name: "Tottenham", component: "tottenham-list"},
        { name:"Chelsea",component:"chelsea-list"},
        { name: "ManchesterUnited", component: "manchester-list"},
        { name: "Arsenal", component: "arsenal-list"},
      ]
    }
  },
  methods: {
    selectComponent(comp) {
      this.$emit('change-component', comp)
    }
  }
}
</script>

<style>

</style>