<template>
  <div>
    <DigitalApproach/>
    <HelpYou/>
    <HelpYou2/>
    <VideoSection/>
    <EventSection/>
    <PeopleSection/>
    <NewslettersSection/>
  </div>
</template>

<script>
import DigitalApproach from './DigitalApproach.vue'
import HelpYou from './HelpYou.vue'
import HelpYou2 from './HelpYou2.vue'
import VideoSection from './VideSection.vue'
import EventSection from './EventSection'
import PeopleSection from './PeopleSection'
import NewslettersSection from './NewslettersSection'

export default {
  name: 'MyMain',
  components: {
    DigitalApproach,
    HelpYou,
    HelpYou2,
    VideoSection,
    EventSection,
    PeopleSection,
    NewslettersSection
  }
}
</script>

<style scoped lang="scss">

</style>
