<template>
  <div>
      <div>
          <h3>{{ player.first_name }} ({{ player.last_name }})</h3>
        <span>Joue au poste de {{ player.position }}</span>
        <img v-bind:src="'../assets/img/hugolloris.jpg'">
      </div>





  </div>
</template>

<script>
export default {
    name: "chelsea-list",
  props: ['selection'],

}
</script>

<style>

</style>