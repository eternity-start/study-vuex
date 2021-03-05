<template>
  <div>
    <!-- $store.state.count 也可以，可以省略this -->
    <!-- <h3>当前最新的count值为： {{this.$store.state.count}}</h3> -->
    <h3>{{this.$store.getters.showNum}}</h3>
    <button @click="btn1">+1</button>
    <button @click="btn2">+n</button>
    <button @click="btn3">+async</button>
    <button @click="btn4">+nasync</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
    }
  },
  created() {
  },
  methods: {
    btn1() {
      this.$store.commit('add')
    },
    btn2() {
      this.$store.commit('addN', 5)
    },
    btn3() {
      this.$store.dispatch('addAsync')
    },
    btn4() {
      this.$store.dispatch('addNAsync', 5)
    }
  }
}
</script>
<style>
</style>
