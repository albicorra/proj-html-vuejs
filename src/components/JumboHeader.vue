<template>
  <div class="jumbo-wrapper">
    <div class="container-small jumbo-header">
        <div class="title" id="title">
            <h4 class="subtitle">New Challenges, New Skills</h4>
            <h1 class="big-title">Build your own life coaching buisness</h1>
            <p>Whole-Life coaching for committed entrepreneurs</p>
            <button class="green-button">Get started today</button>
        </div>

        <div class="hero-img-wrapper">
            <img src="../assets/img/home-business-hero-avatar.png" id="img-hero" alt="">
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'JumboHeader',
  
}
</script>

<style scoped lang="scss">
  .jumbo-wrapper{
    background-color: #ecf2f9;
    height: 770px;
    position: relative;
    background-image: url('../assets/img/home-business-hero-global-image.png');
    background-repeat: no-repeat;
    background-position: 70% center;
    background-size: auto;
    margin-top: 80px;

  
    .jumbo-header{
        display: flex;
        align-items: center;
        height: 100%;

        .title{
            width: 50%;
            padding-right:120px;

            p{
                font-size: 18px;
                font-weight: 500;
                line-height: 30px;
                color: #696969;
                margin-bottom: 20px;
            }


        }

        .hero-img-wrapper{
            width: 50%;
            height: 100%;
            display: flex;
            align-items: flex-end;
            justify-content: center;
            

            .hero-globe{
                display: inline;
                position: absolute;
                z-index: -1;

                .hero-globe img{
                    position: absolute;
                }
            }
        }
    }
  }

  @media screen and (max-width: 1200px){
    .jumbo-header{
        flex-direction: column;
        text-align: center;
        justify-content: center;

        #title{
            padding: 100px 0px;
            
            p{
                font-size: 16px;
            }
        }

        #img-hero{
            width: 250px;
        }
    }
}

@media screen and (max-width: 768px){
    #hero-img{
        width: 200px;
    }
}
  
</style>
