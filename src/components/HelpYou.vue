<template>
  <div class="help-wrapper">
    <div class="container-small section-wrapper">
        <h4 class="subtitle">Let’s Dream Big Together</h4>
        <h1 class="big-title">Explore How can I help you</h1>

        <div class="card-wrapper">
            
            <HelpCard v-for="el in card"
            :key="el.id"
            :img="el.img"
            :title="el.title"
            :text="el.text"/>

            <div class="circle-wrapper">
                <div class="circle active"></div>
                <div class="circle"></div>
                <div class="circle"></div>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
import HelpCard from './HelpCard.vue'

export default {
  name: 'HelpYou',
  components: {
    HelpCard
  },
  data () {
    return{
      card:[
        {
          title: 'Consultative Training',
          text: 'With a coach addressing multiple issues that are off balance, affecting your business in various unconsidered ways.',
          img: require('../assets/img/home-business-service-slide-01-480x298.jpg'),
          id: 1,
        },
        {
          title: 'Real Deal Coaching',
          text: 'Brings an exceptionally powerful opportunity. Being able to accept, to work with that opportunity.',
          img: require('../assets/img/home-business-service-slide-02-480x298.jpg'),
          id: 2,
        },
        {
          title: 'Advisor Training Program',
          text: 'Getting high quality, entrepreneur mindset driven online business coaching, is what is needed.',
          img: require('../assets/img/home-business-service-slide-03-480x298.jpg'),
          id: 3,
        },
      ]
    }
  }
}
</script>

<style scoped lang="scss">
    .help-wrapper{
        background-color: #F8F8F8;

        .section-wrapper{
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            padding: 110px 0px;

            .card-wrapper{
                display: flex;
                flex-wrap: wrap;
                column-gap: 30px;
                margin-top: 30px;
                /* margin-bottom: 70px; */
                width: 100%;
                justify-content: center;
                
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
        }
    }
</style>
