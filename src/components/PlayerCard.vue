<template>

   <div class="max-w-sm rounded overflow-hidden shadow-lg p-8 ">
  <img class="h-43 w-full" :src="playerImage(player.image)" alt="">
  <div class="px-6 py-4">
    <div class="font-bold text-xl mb-2"><h2>{{ player.first_name }} {{ player.last_name }}</h2> </div>
    <p class=" text-base">
      {{ player.last_name }} est un joueur évoluant au poste de {{ player.position }} dans le club {{ player.team }}
    </p>
  </div>
  <div class="px-6 pt-4 pb-2">
    <span class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-2">#football</span>
    <span class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-2">#sport</span>
    <span class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-2">#premierleague</span>
  </div>

   </div>
  
    
</template>

<script>
export default {
   name: "player-card",
   position: "player-position",
  props: ['player'],
  methods: {
    playerImage(img) {
      return require('@/assets/img/'+img)
    }
  },

}
</script>

<style>

</style>
