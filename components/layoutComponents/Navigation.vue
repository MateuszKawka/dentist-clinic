<template>
  <nav class="nav" :class="{'nav--visible': visible}">
    <ul class="menu">
      <li class="menu__item" v-for="item in navLinks" :key="item.name">
        <a :href="item.href" class="menu__link">{{ item.name }}</a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "Navigation",
  props: {
    navLinks: Array,
    visible: Boolean
  }
};
</script>