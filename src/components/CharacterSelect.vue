<template>
  <div>
      <label for="character-select">Select a Character: </label>
        <select id="character-select" v-model="selectedCharacter" v-on:change="handleSelection">
            <option disabled value="">Select a Character</option>
            <option v-for="(character, index) in characters" :key="index" :character="character" :value="character">{{character.name}}</option>
        
        </select>
          <!-- <list-item v-for="(character, index) in characters" :key="index" :character="character"></list-item>
      </ul> -->
  </div>
</template>


<script>
import ListItem from './ListItem.vue'
import { eventBus } from '../main'

export default {
name: 'character-select',
props: ['characters'],
components: {
        "list-item": ListItem
    },
data(){
    return {
        selectedCharacter: null
    }
},
methods: {
    handleSelection: function(){
        eventBus.$emit('character-selected', this.selectedCharacter)
    }
}
}
</script>

<style>

</style>