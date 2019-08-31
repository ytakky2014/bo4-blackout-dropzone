<template>
  <v-app>
    <v-container text-xs-center>
      <div class="hello">
        <h1>{{ msg }}</h1>
        <v-card
          max-width="800"
          max-height="600"
          class="mx-auto"
        >
          <v-col class="shirnk">
            <v-img
              v-bind:src="require('@/assets/bomap.png')">
            </v-img>
          </v-col>
          <v-col class="text-center">
            <v-btn x-large dark @click="generate">Button</v-btn>
          </v-col>
          <v-col class="text-center">
            <h2>{{ drop_zone }}</h2>
          </v-col>
        </v-card>
      </div>
    </v-container>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      msg: 'BlackOut Drop Zone Generate',
      drop_zone: ''
    }
  },
  methods: {
    generate () {
      const c = ['B', 'C', 'D', 'E', 'E', 'F', 'G', 'H']
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
