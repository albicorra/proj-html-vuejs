<template>
  <div class="container-small section-wrapper">
    <h4 class="subtitle">Wanna transform your life?</h4>
    <h1 class="big-title">Upcoming Events</h1>

    <div class="event-container">
      
      <EventCard v-for="el in event"
      :key="el.id"
      :city="el.city"
      :activity="el.activity"
      :date="el.date"
      :month="el.month"/>
    
    </div>
    <div class="motivation-text">
      <p>Excited about our event? 
        <span>View all events  <i class="fa-solid fa-arrow-right"></i></span>
      </p>
    </div>
  </div>
</template>

<script>
import EventCard from './EventCard.vue'

export default {
  name: 'EventSection',
  data () {
    return {
      event:[
        {
          city: 'Texas, US',
          activity: 'Storytelling Workshop',
          date: '22',
          month: 'apr',
          id: 1
        },
        {
          city: 'New York, US',
          activity: 'Painting Art Contest 2020',
          date: '10',
          month: 'oct',
          id: 2
        },
        {
          city: 'Hamburg, Germany',
          activity: 'International Art Fair 2020',
          date: '23',
          month: 'nov',
          id: 3
        },
        {
          city: 'Illinois, US',
          activity: 'Street Performance: Call for Artist',
          date: '15',
          month: 'dec',
          id: 3
        },
        {
          city: 'Illinois, US',
          activity: 'Consumer Food Safety Education Conference',
          date: '22',
          month: 'jul',
          id: 5
        },
        {
          city: 'Dubai',
          activity: 'How meditation improve your mental health?',
          date: '12',
          month: 'aug',
          id: 6
        },
      ]
    }
  },
  components: {
    EventCard
  }
}
</script>

<style scoped lang="scss">
  .section-wrapper{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    padding: 110px 0px 150px 0px;

    .event-container{
      display: flex;
      align-items: center;
      flex-wrap: wrap;
      gap: 30px;
      width: 100%;
      margin: 20px 0px;
    }

    .motivation-text{
      width: 570px;
      font-size: 18px;
      font-weight: 500;
      text-align: center;
      margin-top: 50px;
      color: #696969;
      cursor: pointer;

      span{
        font-weight: 700;
        color: #20ad96;
      }
    }

    .motivation-text:hover span{
    text-decoration: underline;
    }
  }
</style>
