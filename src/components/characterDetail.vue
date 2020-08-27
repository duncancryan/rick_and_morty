<template>
  <div v-if="character">
      <h3>{{character.name}}</h3>
      <p></p>
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