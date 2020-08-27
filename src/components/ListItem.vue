<template>
  <li v-on:click="handleClick">{{character.name}}</li>
</template>

<script>
export default {
    name: 'list-item',
    props: ['character'],
    methods: {
        handleClick: function() {
            eventBus.$emit('character-selected', this.character)
        }
    }
}
</script>

<style>

</style>