<template>
  <div class="help-wrapper">
    <div class="container-large section-wrapper">
        <h4 class="subtitle">Let’s Dream Big Together</h4>
        <h1 class="big-title">Explore How can I help you</h1>

        <div class="card-wrapper">
            
            <HelpCard2 v-for="el in card"
            :key="el.id"
            :img="el.img"
            :price="el.price"
            :text="el.text"/>

            <div class="motivation-text">
                <p>Take the control of their life back and start doing things to make their dream come true. 
                    <span>View all courses <i class="fa-solid fa-arrow-right"></i></span>
                </p>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
import HelpCard2 from './HelpCard2.vue'

export default {
  name: 'HelpYou2',
  components: {
    HelpCard2
  },
  data () {
    return{
      card:[
        {
          price: '$40.00',
          text: 'Learning to write as a Professional Author',
          img: require('../assets/img/course-02-443x600.jpg'),
          id: 1,
        },
        {
          price: 'Free',
          text: 'Customer-centric Info-tech Strategies',
          img: require('../assets/img/stock-full-hd-03-443x600.jpg'),
          id: 2,
        },
        {
          price: '$19.00',
          text: 'Open Programming Courses for everyone: Pyton',
          img: require('../assets/img/stock-full-hd-04-443x600.jpg'),
          id: 3,
        },
        {
          price: '$26.00',
          text: 'Academic listening and Note-talking',
          img: require('../assets/img/stock-full-hd-06-443x600.jpg'),
          id: 4,
        },
      ]
    }
  }
}
</script>

<style scoped lang="scss">
    .help-wrapper{
        background-color: #fff;

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
                width: 100%;
                justify-content: center;

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
                        color: #333;
                    }
                }

                .motivation-text:hover span{
                    text-decoration: underline;
                }
            }
        }
    }
</style>