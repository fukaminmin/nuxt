<template lang="html">
  <div class="sample">
    <div>Hello, I'm children takanorip!</div>
    <button @click="execReverseMyName()">change my name</button>
    <div>{{ reversedMyName }}</div>
  </div>
</template>
​
<script>
export default {
  data() {
    return {
      name: 'fukaminmin'
    }
  },
  computed: {
    reversedMyName() {
      return this.name
        .split('')
        .reverse()
        .join('')
    }
  },
  methods: {
    execReverseMyName() {
      this.name = this.name
        .split('')
        .reverse()
        .join('')
    }
  }
}
</script>
​
<style lang="scss" scoped>
</style>
