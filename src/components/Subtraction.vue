<template>
  <div>
    <!-- <h3>当前最新的count值为： {{count}}</h3> -->
    <h3>{{showNum}}</h3>
    <button @click="sub">-1</button>
    <button @click="subN(5)">-n</button>
    <button @click="subAsync">-1async</button>
  </div>
</template>

<script>
import { mapState, mapMutations, mapActions, mapGetters } from 'vuex'
export default {
  data() {
    return {
    }
  },
  computed: {
    ...mapState(['count']),
    ...mapGetters(['showNum'])
  },
  created() {
  },
  methods: {
    ...mapMutations(['sub', 'subN']),
    ...mapActions(['subAsync'])
    // btn9() {
    //   this.sub()
    // },
    // btn8() {
    //   this.subN(5)
    // },
    // btn7() {
    //   this.subAsync()
    // }
  }
}
</script>
<style>
</style>
