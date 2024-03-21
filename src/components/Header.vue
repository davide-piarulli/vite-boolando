<script>
export default {
  data() {
    return {};
  },
};
</script>

<template>
  <header>
    <div class="topbar">
      <div class="container d-flex">
        <nav class="menu left">
          <ul class="d-flex">
            <li><a href="#">Donna</a></li>
            <li><a href="#">Uomo</a></li>
            <li><a href="#">Bambini</a></li>
          </ul>
        </nav>

        <div class="logo">
          <img src="../assets/img/boolean-logo.png" alt="Booleando Logo" />
        </div>

        <div class="menu right">
          <nav>
            <ul class="d-flex">
              <li>
                <a href="#"><i class="fa-solid fa-user"></i></a>
              </li>
              <li>
                <a href="#"><i class="fa-regular fa-heart"></i></a>
              </li>
              <li>
                <a href="#"><i class="fa-solid fa-bag-shopping"></i></a>
              </li>
            </ul>
          </nav>
        </div>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
@use "../assets/scss/partials/variables" as *;
header {
  background-color: $bg-color-header;
  position: fixed;
  top: 0;
  z-index: 999;
  width: 100%;
  box-shadow: 0 1px 3px grey;
  .topbar {
    padding: 10px;
    img {
      max-width: 150px;
    }
    .container {
      justify-content: space-between;
      align-items: center;
    }
    .menu {
      width: 20%;
      ul a {
        color: white;
        text-decoration: none;
        font-size: 20px;
        &:hover {
          text-decoration: underline;
        }
      }
    }
    .left li {
      padding-right: 10px;
    }
    .right li {
      padding-right: 10px;
    }
    .right ul {
      justify-content: flex-end;
    }
  }
}
</style>
