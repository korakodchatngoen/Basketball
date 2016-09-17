<template>
  <div id="app">
    <div>
      Home <br>
      <display :point = "pointHome"></display>
      <br><br>
      <manage-point :add-point="addPointHome">
    </div>
    <br><br>
    <div>
      Away <br>
      <display :point = "pointAway"></display>
      <br><br>
      <manage-point :add-point="addPointAway">
    </div>
  </div>
</template>

<script>
import ManagePoint from './components/ManagePoint'
import Display from './components/Display'

export default {
  components: {
    ManagePoint,
    Display
  },
  data () {
    return {
      pointHome: 0,
      pointAway: 0
    }
  },
  methods: {
    addPointHome: function (point) {
      this.pointHome += point
    },
    addPointAway: function (point) {
      this.pointAway += point
    }
  }
}
</script>

<style>
html {
  height: 100%;
}

body {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
}

#app {
  color: #2c3e50;
  margin-top: -100px;
  max-width: 600px;
  font-family: Source Sans Pro, Helvetica, sans-serif;
  text-align: center;
}

#app a {
  color: #42b983;
  text-decoration: none;
}

.logo {
  width: 100px;
  height: 100px
}
</style>
