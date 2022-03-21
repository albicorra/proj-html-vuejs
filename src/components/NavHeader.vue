<template>
  <nav class="container-navbar">
    <div class="logo">
        <img src="../assets/img/dark-logo.png" alt="">
    </div>

    <ul class="navbar">
        <li><a href="#">Home</a></li>
        <li><a href="#">Pages</a></li>
        <li><a href="#">Courses</a></li>
        <li><a href="#">Features</a></li>
        <li><a href="#">Blog</a></li>
        <li><a href="#">Shop</a></li>
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
        <i class="fa-solid fa-magnifying-glass"></i>
    </div>

  </nav>
</template>

<script>
export default {
  name: 'NavHeader',
  
}
</script>

<style scoped lang="scss">
  .container-navbar{
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 80px;
    background-color: cadetblue;

    .logo{
      padding: 20px 20px 20px 140px;

      img{
        width: 160px;
      }
    }

    .navbar{
      display: flex;
      align-items: center;
      font-size: 16px;
      font-weight: 500;

      li{
        margin: 0px 5px;
        
        a{
          padding: 15px 15px;
        }
      }
        
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
        font-size: 18px;
      }

      .search-bar{
        padding: 32px 20px;
        height: 100%;
        border: none;
        width: 180px;
      }
    }
  }
</style>
