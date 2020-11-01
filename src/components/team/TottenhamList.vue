<template>
  <div
    class="border border-green-900 m-2 p-2 rounded flex justify-between"
    :class="IsInTottenham"
  >
  <div>
    <h3 class="text-lg font-bold">{{ player.first_name }} {{ player.last_name }}</h3>
      <p>{{ player.position }} </p>
  </div>
  </div>
</template>

<script>
export default {
    name: "tottenham-list",
  props: ['player'],
  computed: {
    IsInTottenham() {
      if(this.player.team == "tottenham"){
        return true
      }
      return false
    },
    
  },
  }
  

</script>

<style>

</style>