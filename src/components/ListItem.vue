<template>
  <li v-on:click="handleClick">{{character.name}}</li>
</template>

<script>
export default {
    name: 'list-item',
    props: ['character']
}
</script>

<style>

</style>