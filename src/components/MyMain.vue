<template>
  <div>
    <DigitalApproach/>
    <HelpYou/>
    <HelpYou2/>
    <VideoSection/>
    <EventSection/>
  </div>
</template>

<script>
import DigitalApproach from './DigitalApproach.vue'
import HelpYou from './HelpYou.vue'
import HelpYou2 from './HelpYou2.vue'
import VideoSection from './VideSection.vue'
import EventSection from './EventSection'

export default {
  name: 'MyMain',
  components: {
    DigitalApproach,
    HelpYou,
    HelpYou2,
    VideoSection,
    EventSection
  }
}
</script>

<style scoped lang="scss">

</style>
