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
<style scoped>
header {
  background-color: #ffffff;
  color: rgb(0, 0, 0);
  padding: 16px 32px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

h1 {
  font-size: 1.5rem;
}

span {
  background-color:#aeaaaa;
  padding: 6px 14px;
  border-radius: 20px;
  font-size: 0.9rem;
}
</style>