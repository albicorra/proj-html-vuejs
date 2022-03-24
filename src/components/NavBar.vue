<template>
    <li><a href="#" class="link">{{item}}</a></li>
</template>

<script>
export default {
  name: 'NavBar',
  props: {
    item: String,
  }
  
}
</script>

<style scoped lang="scss">
    li{
        margin: 0px 5px;
        
        a{
          padding: 15px 15px;
          font-size: 16px;
          font-weight: 500;
        }

        a:hover{
          color: #20ad96;
          border-bottom: 1px solid #20ad96;
        }
    }
    @media screen and (max-width: 1200px){

      li{
          border-bottom: 2px solid #67607D;
          width: 100%;
          color: #fff;
          z-index: 2;
          
  
          .link{
            line-height: 80px;
            font-size: 24px;
          }
  
          .link:hover{
              opacity: 50%;
              color: #fff;
              border: none;
          }
      }
    }
</style>
