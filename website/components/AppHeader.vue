<template>
    <header>
        <img src="/shared/logo.svg" alt="">
        <nav>
            <div class="hamburger" @click="toggleNav">
            <i class="icon">☰</i> <!-- Simple representation, consider using a proper icon -->
            </div>
            <ul v-if="showNav">
            <li><b>00</b> Home</li>
            <li><b>01</b> Destination</li>
            <li><b>02</b> Crew</li>
            <li><b>03</b> Technology</li>
            </ul>
        </nav>
    </header>
</template>
  
  <script>
  export default {
    data() {
      return {
        showNav: false,
      };
    },
    methods: {
      toggleNav() {
        this.showNav = !this.showNav;
      },
    },
  };
  </script>
  
  <style>
  header{
    display: flex;
    justify-content: space-between;
  }

  header img{
    width: 20px;
    height: 20px;
  }

  /* Simple styling, update according to your needs */
  .hamburger {
    cursor: pointer;
  }

  nav{
    text-align: right;
  }

  nav ul{
    text-align: left;
  }
  
  nav ul li {
    list-style: none;
  }
  
  li b {
    display: none;
  }
  
  /* Show menu when `showNav` is true */
  nav ul.show {
    display: block;
  }
  @media screen and (min-width: 600px) {
    li > b {
      display: block;
    }
  }
  </style>
  