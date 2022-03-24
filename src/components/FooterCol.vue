<template>
  <li>
      {{text}}
  </li>
</template>

<script>
export default {
  name: 'FooterCol',
  props: {
    text: String
  }
}
</script>

<style scoped lang="scss">
li{
    color: #ababab;
    font-size: 14px;
    font-weight: 500;
    line-height: 24px;
    margin-bottom: 20px;
    cursor: pointer;
}

li:hover{
    transition: 300ms;
    color: #20ad96;
}
</style>
