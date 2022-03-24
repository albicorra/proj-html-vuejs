<template>
    <div class="card" :class=" active ? 'active' : ''">
        <div class="text-container">    
            <h5>{{title}}</h5>
            <p>{{text}}</p>
        </div>
        <div class="profile-container">
            <img :src="image" alt="">
            <div class="profile-info">
                <h5>{{name}}</h5>
                <p>{{info}}</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'MyFooter',
  props: {
    active: String,
    title: String,
    text: String,
    image: String,
    name: String,
    info: String,
  }
}
</script>

<style scoped lang="scss">
    .card{
        width: 30.9%; 
        padding: 30px 30px;
        display: flex;
        flex-direction: column;
        background-color: #fff;
        border-radius: 5px;
        opacity: 60%;
        

        .text-container{
            margin-bottom: 50px;

            h5{
                font-size: 20px;
                color: #3f3a64; 
                font-weight: 700;
                margin-bottom: 30px;
                line-height: 32px;
            }

            p{
                font-size: 18px;
                color: #696969;
                font-weight: 500;
                line-height: 30px;
            }
        }

        .profile-container{
            display: flex;
            column-gap: 20px;
            align-items: center;
                   
            img{
                width: 70px;
                border-radius: 50%;
            }

            .profile-info > h5{
                color: #3f3a64;
                font-size: 15px;
                font-weight: 700;
                margin-bottom: 10px;
            }

            .profile-info > p{
                color: #7e7e7e;
                font-size: 14px;
            }

                   
        }
    }

    .card.active{
        opacity: 100%;
    }

    @media screen and (max-width: 1200px){
        .card{
            width: 100%;
            margin: 50px 0px;
            
        }
    }

</style>