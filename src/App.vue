<template>
    <div id="app">
        <header v-if="!$route.meta.hideNavbar">
          <nav>

            <div class="nav-logo">
            <img src="@/assets/Hobby_Outpost-dark.png" alt="Logo" class="logo" />
            </div>

            <div class="nav-links">
            <router-link to="/">Home</router-link>
            <router-link to="/tournaments">Tournaments</router-link>
            </div>

          </nav>
        </header>
        <!-- Render the routed component -->
        <router-view />
    </div>
  </template>

  <script>
  export default {
    name: "App",
  };
  </script>


  <style>
    /* Add some basic styling (optional) */
    /* Header and Navbar Styles */

    #app {
      background-image: url('@/assets/Background_pattern.png');
      background-size: 500px; /* Adjust this value to control the size */
      background-repeat: repeat; /* Repeat the image */
      background-position: top left; /* Optional: Start tiling from the top-left corner */
      min-height: 100vh; /* Ensure it covers the viewport height */
    }


    header {
      background-color: #272727;
      color: #333(0, 0, 0);
    }

    nav {
      display: flex; /* Flexbox for horizontal layout */
      align-items: center; /* Center items vertically */
      padding: 0.5rem;
    }

    .nav-logo {
      flex-shrink: 0; /* Prevent the logo from shrinking */
      margin-right: 35px;
      margin-left: 20px;
    }

    .logo {
      width: 130px; /* Adjust size for a larger logo */
      height: auto; /* Maintain aspect ratio */
    }

    .nav-links {
      display: flex;
      gap: 30px; /* Add space between links */
      align-items: center;
    }

    .nav-links a {
      color: rgb(255, 255, 255);
      text-decoration: none;
      font-size: 1.1rem;
    }

    .nav-links a.router-link-active {
      font-weight: bold;
    }

    a:hover {
      background-color: rgb(100, 100, 100); /* Yellow highlight */
      padding: 5px 10px; /* Add padding to increase the size of the highlight */
      border-radius: 5px; /* Optional: Add rounded corners for a nicer look */
      transition: background-color 0.3s ease, padding 0.3s ease; /* Smooth transition */
    }

    </style>
