<template>
  <header class="header">
    <div class="logo">
      <img src="@/assets/logo.png" alt="Logo">
    </div>
    <nav class="nav">
      <ul class="nav-list">
        <li><a href="#about">About</a></li>
        <li><a href="#blog">Blog</a></li>
        <li><a href="#contacts">Contacts us</a></li>
      </ul>
      <button class="hamburger" @click="toggleMenu">
        &#9776;
      </button>
    </nav>

    <div v-if="isMenuOpen" class="mobile-menu">
      <ul>
        <li><a href="#about" @click="toggleMenu">About</a></li>
        <li><a href="#social" @click="toggleMenu">Social</a></li>
        <li><a href="#skills" @click="toggleMenu">Skills</a></li>
        <li><a href="#blog" @click="toggleMenu">Blog</a></li>
        <li><a href="#contacts" @click="toggleMenu">Contacts us</a></li>
      </ul>
    </div>
  </header>
</template>

<script>

export default {
    name: 'HeaderApp',
    data() {
    return {
      isMenuOpen: false
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
    }
  }
}
</script>

<style>
@import './HeaderStyle.scss'
</style>