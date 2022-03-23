<template>
  <div class="section-wrapper">
    <div class="container-large">
        <img src="../assets/img/maxcoach-shape-07-150x150.png" class="shape-01" alt="">
        <div class="hero-video">
            <div class="image-wrapper">
                <img src="../assets/img/home-business-video-poster-670x450.jpg" alt="">
                <img src="../assets/img/icon-youtube-play.png" class="icon-youtube" alt="">
            </div>
        </div>

        <div class="text-wrapper">
            <h2 class="title">To Thrive In Business Today, You’ll Need a Good Plan</h2>
            <div v-for="el in textInformation" :key="el.id" class="information-wrapper">
                <h4 @click="activeText(el.id)" :class="el.classElement"><i class="fa-solid fa-circle-chevron-down"></i>{{el.title}}</h4>
                <p class="information" :class="el.classElement">{{el.information}}</p>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'VideoSection',
  data () {
    return{
      
      textInformation:[
        {
          title: 'How can we help?',
          information: 'How many courses you’ve been on, using however many techniques and methods. Unless you’ve come to realize the value of mindset, then you’ve yet to understand how success comes. With everyone else’s mindset involved impacting too. Hence why business coaching is so crucial for success.',
          classElement: '',
          id: 0
        },
        {
          title: 'Why would I need a business COACH?',
          information: 'Every great entrepreneur is surrounded by coaches and advisors. A great business coach will listen and guide you to success. Perhaps most importantly, a business coach will make you focus on your goals and hold you accountable to the things you should do, and to where you want your business to be.',
          classElement: '',
          id: 1
        },
        {
          title: 'What is one-on-one coaching?',
          information: 'We understand that every business is at a different stage of development; this is why we’ve also developed multiple Group Coaching programs to fit the needs of every kind of business. Unlike a consultant, your personal MaxCoach will do more than just show you what to do – he or she will be with you when you need them most.',
          classElement: '',
          id: 2
        },
      ]
    }
  },
  methods: {
    activeText: function(index){
      if (this.textInformation[index].classElement == '') {
        
        this.textInformation[index].classElement = 'active'
      }else{
        this.textInformation[index].classElement = ''
      }
    },
  }
}
</script>

<style scoped lang="scss">
    .section-wrapper{
        background-color: #313043;
        background-image: url('../assets/img/background-map-dots-top-right-transparent.png');
        background-position: right;
        background-size: auto;
        background-repeat: no-repeat;
        color: #fff;

        .container-large{
            display: flex;
            padding: 100px 50px;
            align-items: center;
            position: relative;
            
            .shape-01{
                width: 170px;
                position: absolute;
                bottom: 0;
                left: 0px;
            }

            .hero-video{
                width: 50%;
                padding: 40px;
                display: flex;
                justify-content: center;
                align-items: center;
                
                .image-wrapper{
                    position: relative;
                    border-radius: 5px;
                    overflow: hidden;
                    cursor: pointer;

                    img{
                        display: block;
                    }

                    .icon-youtube{
                        width: 100px;
                        position: absolute;
                        top: 50%;
                        left: 50%;
                        transform: translate(-50%, -50%);
                    }
                }
            }

            .text-wrapper{
                padding: 80px;
                width: 50%;
                display: flex;
                flex-direction: column;

                .title{
                    font-size: 48px;
                    font-weight: 700;
                    margin-bottom: 50px;
                }

                .information-wrapper{
                    border-bottom: 2px solid #474555;

                    h4{
                        font-size: 24px;
                        font-weight: 600;
                        padding: 20px 0px;
                        cursor: pointer;

                        i{
                            margin-right: 20px;
                        }
                    }

                    h4.active{
                        color: #20ad96;
                    }
                    
                    .information{
                        display: none;
                        font-size: 15px;
                        line-height: 26px;
                        padding: 0px 0px 20px 46px;
                    }

                    .information.active{
                        display: block;
                    }
                }
                }

        }
    }
</style>
