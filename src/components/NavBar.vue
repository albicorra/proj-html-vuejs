<template>
    <li><a href="#">{{item}}</a></li>
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
    }
</style>
