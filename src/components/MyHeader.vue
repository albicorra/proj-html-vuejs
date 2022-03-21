<template>
  <header>
    <NavHeader/>
    <JumboHeader/>
  </header>
</template>

<script>
import NavHeader from './NavHeader.vue'
import JumboHeader from './JumboHeader.vue'

export default {
  name: 'MyHeader',
  components: {
    NavHeader,
    JumboHeader
  }
}
</script>

<style scoped lang="scss">

</style>
