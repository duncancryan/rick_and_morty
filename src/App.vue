<template>
  <div>
    <h1>Characters</h1>
    <div class="main-container">
      <character-list :characters="characters"></character-list>
      <character-detail></character-detail>
    </div>
  </div>
</template>

<script>
import CharacterList from './components/CharacterList.vue'
export default {
  name: 'app',
  data(){
    return {
      characters: [],
      selectedCharacter: null
    };
  },
  mounted(){
    fetch('https://rickandmortyapi.com/api/character')
    .then(response => response.json())
    .then(characters => this.characters = characters.results)
  },
  components: {
    "character-list": CharacterList
  }

}
</script>

<style>

</style>
