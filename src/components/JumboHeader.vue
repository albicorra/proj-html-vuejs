<template>
  <div class="jumbo-wrapper">
    <div class="container-small jumbo-header">
        <div class="title">
            <h4>New Challenges, New Skills</h4>
            <h1>Build your own life coaching buisness</h1>
            <p>Whole-Life coaching for committed entrepreneurs</p>
            <button class="green-button">Get started today</button>
        </div>

        <div class="hero-img">
            <img src="../assets/img/home-business-hero-avatar.png" alt="">
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

  
    .jumbo-header{
        display: flex;
        align-items: center;
        height: 100%;

        .title{
            width: 50%;
            padding-right:120px;

            h4{
                color: #20ad96;
                font-size: 24px;
                font-weight: 500;
                margin-bottom: 20px;
            }

            h1{
                font-size: 48px;
                font-weight: 800;
                line-height: 56px;
                color: #333333;
                margin-bottom: 20px;
            }

            p{
                font-size: 18px;
                font-weight: 500;
                line-height: 30px;
                color: #696969;
                margin-bottom: 20px;
            }


        }

        .hero-img{
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
  
</style>
