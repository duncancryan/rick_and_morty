<template>
  <div v-if="character">
      <h3>{{character.name}}</h3>
      <p>{{character.species}}</p>
      <p>Status: {{character.status}}</p>
      <p>Origin: {{character.origin.name}}</p>
  </div>
</template>

<script>
export default {
    name: 'character-detail',
    props: ['character']
}
</script>

<style>

</style>