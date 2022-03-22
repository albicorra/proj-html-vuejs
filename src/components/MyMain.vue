<template>
  <div>
    <DigitalApproach/>
    <HelpYou/>
    <HelpYou2/>
  </div>
</template>

<script>
import DigitalApproach from './DigitalApproach.vue'
import HelpYou from './HelpYou.vue'
import HelpYou2 from './HelpYou2.vue'

export default {
  name: 'MyMain',
  components: {
    DigitalApproach,
    HelpYou,
    HelpYou2
  }
}
</script>

<style scoped lang="scss">

</style>
