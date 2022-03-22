<template>
  <nav class="container-navbar">
    <div class="logo">
        <img src="../assets/img/dark-logo.png" alt="">
    </div>

    <ul class="navbar">
        <NavBar v-for="(el) in menuItems" :key="el.id"
        :item="el.item"/>
    </ul>

    <div class="search">
        <img src="../assets/img/en.png" alt="">
        <select name="" class="language-select">
          <option value="en">English</option>
          <option value="de">Deutsch</option>
          <option value="fr">Français</option>
        </select>
        <i class="fa-regular fa-circle-user icon-user"></i>
        <input type="text" placeholder="Search.." class="search-bar">
        <i class="fa-solid fa-magnifying-glass icon-user"></i>
    </div>

  </nav>
</template>

<script>
import NavBar from './NavBar.vue'

export default {
  name: 'NavHeader',
  components: {
    NavBar,
  },
  data () {
    return {
      menuItems: [
        {
          item: 'Home',
          active: 'false',
          id: 1
        },
        {
          item: 'Pages',
          active: 'false',
          id: 2
        },
        {
          item: 'Courses',
          active: 'false',
          id: 3
        },
        {
          item: 'Features',
          active: 'false',
          id: 4
        },
        {
          item: 'Blog',
          active: 'false',
          id: 5
        },
        {
          item: 'Shop',
          active: 'false',
          id: 6
        },
      ]
    }
  }
}
</script>

<style scoped lang="scss">
  .container-navbar{
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 80px;
    background-color: #fff;

    .logo{
      padding: 20px 20px 20px 140px;

      img{
        width: 160px;
      }
    }

    .navbar{
      display: flex;
      align-items: center;
    }

    .search{
      display: flex;
      align-items: center;

      img{
        width: 25px;
        margin: 10px;
      }

      .language-select{
        line-height: 100%;
        background-color: #fff;
        border: none;
        font-size: 16px;
        font-weight: 500;
        margin: 0px;
        padding: 30px 0px;
        text-transform: uppercase;
      }
      .language-select:focus-visible{
        outline: none;
      }

      .icon-user{
        font-size: 20px;
        margin: 15px;
        cursor: pointer;
      }

      .search-bar{
        padding: 32px 20px;
        height: 100%;
        border: none;
        width: 180px;
        border-left: 1px solid #eceeef;
        font-size: 16px;
      }
    }
  }
</style>
