<template>
    <div class="card">
        <div>
            <img :src="img" alt="">
        </div>

        <div class="card-text-wrapper">
            <h4>{{title}}</h4>
            <p>{{text}}</p>
        </div>

        <div class="button-discover">
            <span>Discover now  </span>
            <i class="fa-solid fa-arrow-right"></i>
        </div>

    </div>
</template>

<script>
export default {
  name: 'MyFooter',
  props:{
    title: String,
    text: String,
    img: String,
  }
}
</script>

<style scoped lang="scss">
    .card{
        width: 31%;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-items:center;
        overflow: hidden;
        border-radius: 10px;
        cursor: pointer;
        background-color: #fff;

        .card-text-wrapper{
            padding: 20px;
            text-align: center;

            h4{
                font-size: 24px;
                font-weight: 600;
                margin-bottom: 20px;
                color: #333333;
            }

            p{
                font-size: 15px;
                color: #696969;
            }
        }

        .button-discover{
            width: 100%;
            padding: 20px;
            text-align: center;
            border-top: 1px solid #eeeeee;
            font-weight: 700;
            border: none;
            transition: 300ms;
            font-size: 14px;
            color: #1FAD96;
        }

        .button-discover:hover{
            background-color: #1FAD96;
            color: #fff;
        }
    }

    .card:hover img{
        transition: 1s;
        transform: scale(1.1);
    }
    .card:hover .button-discover{
    background-color: #1FAD96;
    color: #fff;
    }
</style>
