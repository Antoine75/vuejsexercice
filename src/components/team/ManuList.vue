<template>
  <div>
      <div>
          <h3>{{ player.first_name }} ({{ player.last_name }})</h3>
        <span>Joue au poste de {{ player.position }}</span>
        <img :src="playerPhoto(player.photo)" alt="">
      </div>





  </div>
</template>

<script>
export default {
    name: "manchesterUnited-list",
  props: ['selection'],
  


}
</script>

<style>

</style>