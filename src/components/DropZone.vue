<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div class="center">
      <img src="@/assets/bomap.png" width="1024" height="500"/>
    </div>
    <div class="text-center">
      <v-btn x-large dark @click="generate">Button</v-btn>
    </div>
    <h2>{{ drop_zone }}</h2>
  </div>
</template>

<script>
export default {
  name: 'BlackOut Drop Zone Generate',
  data () {
    return {
      msg: 'BlackOut Drop Zone Generate',
      drop_zone: ''
    }
  },
  methods: {
    generate () {
      const c = ['A', 'B', 'C', 'D', 'E', 'F', 'G', 'H']
      var tx = Math.floor(Math.random() * 8)
      var y = Math.floor(Math.random() * 8 + 1)
      var dz = c[tx] + y
      this.drop_zone = dz
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
.center {
  text-align:center;
}
</style>
