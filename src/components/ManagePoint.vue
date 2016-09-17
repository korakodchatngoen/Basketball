<template>
  <input type="submit" value="+1" @click="addPoint(1)">
  <input type="submit" value="+2" @click="addPoint(2)">
  <input type="submit" value="+3" @click="addPoint(3)">
  <input type="submit" value="-1" @click="disPoint">
</template>

<script>
export default {
  props: ['addPoint', 'disPoint']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  color: #42b983;
}
</style>
