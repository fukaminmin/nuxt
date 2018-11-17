<template lang="html">
  <div class="sample">
    <hr>
    <div :class="{seven: isSeven}">{{ count }}</div>
    <button @click="increment">1つ増えるよ</button>
  </div>
</template>
​
<script>
export default {
  data() {
    return {
      count: 1
    }
  },
  computed: {
    isSeven() {
      return this.count === 7
    }
  },
  mounted() {
    console.log('mouted')
  },
  methods: {
    increment() {
      this.count++
    }
  }
}
</script>
​
<style lang="scss" scoped>
.seven {
  color: red;
}
</style>
