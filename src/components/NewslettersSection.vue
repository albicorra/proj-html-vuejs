<template>
  <div class="container-large section-wrapper">

    <div class="newsletters-container">
        <h1>Subscribe <span>Newsletters</span></h1>
        <p>Enter your email address to register to our newsletter subscription delivered on a regular basis!</p>
        <div class="input-wrapper">
            <input type="text" placeholder="Enter your email">
            <button class="green-button">Subscribe</button>
        </div>
    </div>

    <img src="../assets/img/maxcoach-shape-09.png"  class="shape-02" alt="">
    <img src="../assets/img/maxcoach-shape-02.png" class="shape-03" alt="">
  </div>
</template>

<script>
export default {
  name: 'NewslettersSection',
  
}
</script>

<style scoped lang="scss">
    .section-wrapper{
        padding: 110px;
        display: flex;
        justify-content: center;
        align-items: center;
        position: relative;

        .shape-02{
            position: absolute;
            top: 150px;
            right: 100px;
            width: 200px;
        }

        .shape-03{
            width: 150px;
            position: absolute;
            top: 150px;
            right: 100px;
        }

        .newsletters-container{
            width: 570px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-content: center;

            h1{
                font-size: 48px;
                font-weight: 700;
                text-align: center;
                margin-bottom: 30px;

                span{
                    font-weight: 400;
                    color: #20ad96;
                }
            }

            p{
                text-align: center;
                font-size: 18px;
                font-weight: 500;
                line-height: 30px;
                margin-bottom: 50px;
            }

            .input-wrapper{
                display: flex;
                justify-content: center;
                font-weight: 700;

                input{
                    padding: 20px;
                    width: 445px;
                    border: none;
                    background-color: #f8f8f8;
                    border-radius: 5px;
                    font-size: 15px;
                    font-weight: 400;
                    color: 7c7c7c;
                }

                input:focus-within{
                    border: 1px solid #20ad96;
                }
            }
        }
    }
</style>