<script>
export default {
  data() {
    return {
      menu: [
        {
          title: "Donna",
          link: "#",
        },
        {
          title: "Uomo",
          link: "#",
        },
        {
          title: "Bambini",
          link: "#",
        },
      ],
      icons: [
      {
        title: "User",
        link: "#",
        pic: '<i class="fa-solid fa-user"></i>',
      },
      {
        title: "Fav",
        link: "#",
        pic: '<i class="fa-regular fa-heart"></i>',
      },
      {
        title: "Cart",
        link: "#",
        pic: '<i class="fa-solid fa-bag-shopping"></i>',
      },
    ],
    };
  },
};
</script>

<template>
  <header>
    <div class="topbar">
      <div class="container d-flex">
        <nav class="menu left">
          <ul class="d-flex">
            <li v-for="(item, index) in menu" :key="index">
              <a href="#">{{ item.title }}</a>
            </li>
          </ul>
        </nav>

        <div class="logo">
          <img src="../assets/img/boolean-logo.png" alt="Booleando Logo" />
        </div>

        <div class="menu right">
          <nav>
            <ul class="d-flex">
              <li v-for="(item, index) in icons" :key="index">
                <a :href="item.link" v-html="item.pic"></a>
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
        color: $text-primary;
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
