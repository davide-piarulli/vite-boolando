<script>
  export default {
    data(){
      return {
        
      };
    },
  }
</script>
<template>
<footer>
    <div class="bottombar">
      <div class="container d-flex">
        <div class="footer-left">
          <span>Boolando s.r.l.</span>
          <nav class="footer-menu">
            <ul class="d-flex">
              <li><a href="#">Informazioni legali</a></li>
              <li><a href="#">Informativa sulla privacy</a></li>
              <li><a href="#">Diritto di recesso</a></li>
            </ul>
          </nav>
        </div>
        <div class="footer-right">
          <p>Trovaci anche su</p>
          <nav>
            <ul class="d-flex">
              <li><a href="#"></a><i class="fa-brands fa-x-twitter"></i></li>
              <li><a href="#"></a><i class="fa-brands fa-facebook"></i></li>
              <li><a href="#"></a><i class="fa-brands fa-square-instagram"></i></li>
              <li><a href="#"></a><i class="fa-brands fa-square-pinterest"></i></li>
              <li><a href="#"></a><i class="fa-brands fa-youtube"></i></li>
            </ul>
          </nav>
        </div>
      </div>
    </div>
  </footer>
</template>


<style lang="scss" scoped>
@use "../assets/scss/partials/variables" as *;
footer {
  width: 100%;
  background-color: $bg-color-footer;
  color: $text-primary;
  ul {
    justify-content: space-between;
    padding: 5px 0;
  }
  .container {
  align-items: center;
  justify-content: space-between;
  padding: 30px 0;
}
.footer-left{
  span {
    font-size: 1.3rem;
  }
  a {
    color: $text-footer;
;
    text-decoration: none;
    padding-right: 10px;
    &:hover{
      text-decoration: underline;
    }
  }
}
.footer-right li:hover .fa-x-twitter {
  color: black;
}

.footer-right li:hover .fa-facebook {
  color: blue;
}

.footer-right li:hover .fa-square-instagram {
  color: purple;
}

.footer-right li:hover .fa-square-pinterest {
  color: red;
}

.footer-right li:hover .fa-youtube {
  color: red;
}
  
}
</style>