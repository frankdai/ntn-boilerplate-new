<template>
  <nav class="fixed z-40 top-0 inset-x-0 px-3" aria-label="Main Menu">
    <ul class="flex" style="max-width: 600px; margin: 0 auto">
      <li class="flex-1 pt-3 pb-3">
        <nuxt-link to="/">Home</nuxt-link>
      </li>
      <li class="flex-1 ml-2 relative pt-3 pb-3 menu-base">
        Products
        <ul class="header-menu">
          <nuxt-link to="/products/auto_parts">Auto Parts</nuxt-link>
          <nuxt-link to="/products/motor_parts">Motor Parts</nuxt-link>
          <nuxt-link to="/products/precision">Precision Accessories</nuxt-link>
        </ul>
      </li>
      <li class="flex-1 ml-2 relative pt-3 pb-3 menu-base">
        Equipments
        <ul class="header-menu">
          <nuxt-link to="/equipments/production_equipment">Production Equipments</nuxt-link>
          <nuxt-link to="/equipments/testing_equipment">Testing Equipments</nuxt-link>
        </ul>
      </li>
      <li class="flex-1 ml-2 relative pt-3 pb-3 menu-base">
        About Us
        <ul class="header-menu">
          <nuxt-link to="/pages/about-us">Company Introduction</nuxt-link>
          <nuxt-link to="/pages/contact-us">Contact Us</nuxt-link>
        </ul>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'Header',
  data: ()=>{
    return {
      showMenu: false
    }
  }
}
</script>

<style lang="postcss" scoped>
nav {
  border-bottom: 2px solid #7c7c7c;
  background: white;
}
.ml-2 {
  position: relative;
}
.header-menu {
  display: none;
  position: absolute;
  left: -12px;
  top: 47px;
  background-color: white;
  border: 2px solid #7c7c7c;
  border-top-color: white;
  padding: 12px;
  border-bottom-left-radius: 5px;
  border-bottom-right-radius: 6px;
  min-width: 220px;
}
.header-menu a {
  display: block;
  text-align: left;
}
.menu-base:hover .header-menu {
  display: block;
}
.scrim-bg {
  &::before {
    content: '';
    z-index: -1;
    background-color: var(--bg);
    @apply absolute bottom-0 inset-x-0 h-12 mb-4 transition-colors duration-200 ease-in-out;
  }
  &::after {
    content: '';
    z-index: -1;
    opacity: 1;
    animation: fadeIn1 500ms ease-in-out;
    @apply pointer-events-none absolute bottom-0 inset-x-0 h-16 -mb-12;
    background: linear-gradient(to bottom, #111827, cubic-bezier(0.15, 0, 0.45, 1), transparent);
  }
}
.nuxt-link-exact-active {
  @apply cursor-default;
}

.light {
  & .scrim-bg {
    &::after {
      animation-name: fadeIn2;
      background: linear-gradient(to bottom, #e5e7eb, cubic-bezier(0.15, 0, 0.45, 1), transparent);
    }
  }
  & .nuxt-link-exact-active {
    @apply text-primary-700;
  }
}

/* Need two because of smoother switching between color modes */
@keyframes fadeIn1 {
  from { opacity: 0; }
  to { opacity: 1; }
}
@keyframes fadeIn2 {
  from { opacity: 0; }
  to { opacity: 1; }
}
</style>
