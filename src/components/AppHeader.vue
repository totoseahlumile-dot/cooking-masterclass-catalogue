<template>
  <header>
    <h1>Cooking Masterclass</h1>
    <span> Wishlist: {{ wishlistCount }}</span>
  </header>
</template>
<script>
export default {
  name: "AppHeader",
  props: {
    wishlistCount: {
      type: Number,
      default: 0,
    },
  },
};
</script>
