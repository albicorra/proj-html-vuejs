<template>
    <div class="information-digital-card">
        <i :class="icon"></i>
        <div class="card__text">
            <h3>{{title}}</h3>
            <p>{{text}}</p>
        </div>
    </div>
</template>

<script>
export default {
  name: 'InformationDigitalCard',
  props: {
    title: String,
    text: String,
    icon: String,
  }
  
}
</script>

<style scoped lang="scss">
.information-digital-card{
    display: flex;
    gap: 20px;
    width: 32%;
    margin-bottom: 50px;
    padding: 10px;

    i{
        font-size: 40px;
    }

    .card__text{

        h3{
            font-size: 24px;
            font-weight: 600;
            margin-bottom: 20px;
        }

        p{
            font-size: 16px;
            color: #696969;
            line-height: 24px;
        }
    }
}

@media screen and (max-width: 768px){
    .information-digital-card{
        width: 48%;

        i{
            
        }
    }
}
</style>
