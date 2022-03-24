<template>
  <div class="section-wrapper">
    <h4 class="subtitle">People are praising Maxcoach</h4>
    <h1 class="big-title">What make they love us?</h1>

    <div class="card-wrapper">
      <PeopleCard v-for="el in card"
      :key="el.id"
      :active="el.active"
      :title="el.title"
      :text="el.text"
      :image="el.image"
      :name="el.name"
      :info="el.info"/>
    </div>
    <div class="circle-wrapper">
      <div class="circle active"></div>
      <div class="circle"></div>
      <div class="circle"></div>
      <div class="circle"></div>  
    </div>

  </div>
</template>

<script>
import PeopleCard from './PeopleCard.vue'

export default {
  name: 'PeopleSection',
  components: {
    PeopleCard
  },
  data () {
    return {
      card: [
        {
          title: 'It is a choice of quality for people with special needs',
          text: 'I am a very strict person so I require everything to be organized and neat. Then, I will be able to make things right and shine. MaxCoach guys just got me.',
          image: require('../assets/img/testimonial-avata-03.jpg'),
          name: 'Florence Themes',
          info: '/ Multimedia Admin',
          active: false,
          id: 0
        },
        {
          title: 'High level of efficiency and scientific teaching methods',
          text: 'I am free to learn at my own pace, follow my own schedule and choose the subject I want to learn from the syllabus. Great study portal for people like me.',
          image: require('../assets/img/testimonial-avata-02.jpg'),
          name: 'Mina Hollace',
          info: '/ Freelancer',
          active: true,
          id: 1
        },
        {
          title: 'Professional team of specialists and passionate mentors at reach ',
          text: 'I need to get a certification for English proficiency and MaxCoach is my best choice. Their tutors are smart and professional when dealing with students.',
          image: require('../assets/img/testimonial-avata-04.jpg'),
          name: 'Madley Pondor',
          info: '/ IT Specialist',
          active: false,
          id: 2,
        },
      ]
    }
  }
}
</script>

<style scoped lang="scss">
  .section-wrapper{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    background-color: #F8F8F8;
    padding: 110px 50px;
    flex-wrap: wrap;

    .card-wrapper{
      display: flex;
      align-items: center;
      column-gap: 40px;
      margin: 50px 0px 30px 0px;
      flex-wrap: wrap;
    }

    .circle-wrapper{
      display: flex;
      align-items: center;
      


      .circle{
        background-color: #D8D8D8;
        width: 8px;
        height: 8px;
        margin: 30px 5px;
        border-radius: 50%;
        cursor: pointer;
      }

      .circle.active{
        background-color: black;
        transform: scale(1.5);
      }

      .circle:hover{
        background-color: black;
        transform: scale(1.5);
        transition: 300ms;
      }
    }
  }
</style>
