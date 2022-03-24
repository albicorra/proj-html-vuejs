<template>
    <div class="card">
        <div>
            <img :src="img" alt="">
        </div>

        <div class="card-text-wrapper">
            <h4>{{price}}</h4>
            <p>{{text}}</p>
        </div>
    </div>
</template>

<script>
export default {
  name: 'MyFooter',
  props:{
    price: String,
    text: String,
    img: String,
  }
}
</script>

<style scoped lang="scss">
    .card{
        width: 23%;
        display: flex;
        flex-direction: column;
        align-items: center;
        overflow: hidden;
        border-radius: 5px;
        cursor: pointer;
        background-color: #fff;
        position: relative;

        .card-text-wrapper{
            padding: 20px;
            position: absolute;
            top: 50%;
            bottom: 0;
            left: 0;
            right: 0;
            background: linear-gradient( to top, rgba(0,0,0,0.9), rgba(0,0,0,0));
            display: flex;
            flex-direction: column;
            justify-content: end;

            h4{
                font-size: 24px;
                font-weight: 700;
                margin-bottom: 20px;
                color: #20ad96;
            }

            p{
                font-size: 22px;
                font-weight: 700;
                color: #fff;
                margin-bottom: 10px;
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

        
    }

    .card:hover img{
        transition: 1s;
        transform: scale(1.1);
    }

    @media screen and (max-width: 1200px){
        .card{
            width: 65%;
            margin-bottom: 50px;
        }
    }
</style>
