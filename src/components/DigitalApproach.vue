<template>
  <div class="container-small section-wrapper">
    
        <h4 class="subtitle">Let’s Dream Big Together</h4>
        <h2 class="information-digital">We are pioneers of the digital approach, using leading-edge technology to simplify procedures and apply executive coaching in the new age of digitalization.</h2>
    
        <div class="card-wrapper">
            
            <InformationDigitalCard 
            v-for="el in info" 
            :key="el.id"
            :icon="el.icon"
            :title="el.title"
            :text="el.text"/>

        </div>
        <div class="button-wrapper">
            <button class="green-button light">Learn more</button>
            <button class="green-button">Get started today</button>
        </div>
    </div>
</template>

<script>
import InformationDigitalCard from './InformationDigitalCard.vue'

export default {
  name: 'DigitalApproach',
  components: {
    InformationDigitalCard
  },
  data () {
    return {
      info: [
        {
          title: 'One to One',
          text: 'Getting the necessary clarity about the current state to help you improve your game.',
          icon: 'fa-regular fa-lightbulb',
          id: 1,
        },
        {
          title: 'Anywhere',
          text: 'Access to valuable and portable program which allow you to setup and live anywhere you want.',
          icon: 'fa-solid fa-map-location-dot',
          id: 2,
        },
        {
          title: 'On Time',
          text: 'Punctuality is our top priority because its an essential criteria to assess a program quality.',
          icon: 'fa-solid fa-clock-rotate-left',
          id: 3,
        },
        {
          title: 'Online Coures',
          text: 'Online business coaching now offers you a very powerful way to empower your business into success.',
          icon: 'fa-solid fa-laptop',
          id: 4,
        },
        {
          title: 'Consulting',
          text: 'You will get a clear sense of direction for your business, thorough assessment and faster results.',
          icon: 'fa-solid fa-user-ninja',
          id: 5,
        },
        {
          title: 'Self Development',
          text: 'Business Coaching often keep your focus and develop you both in a professional and personal way.',
          icon: 'fa-solid fa-gear',
          id: 6,
        }
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
        padding: 110px 0px;
        
        .information-digital{
            text-align: center;
            font-weight: 700;
            font-size: 34px;
            margin-bottom: 50px;
        }

        .card-wrapper{
            display: flex;
            flex-wrap: wrap;
            margin-bottom: 70px;
        }

        .button-wrapper{
            display: flex;
            align-items: center;
            gap: 30px;

            .green-button.light{
                background-color: #fff;
                color: #1FAD96;
                border: 2px solid #EEEEEE;
            }

            .green-button.light:hover{
                background-color: #3F3A64;
                color: #fff;
            }

        }

    }

</style>
