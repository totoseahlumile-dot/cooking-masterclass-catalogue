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
  background-color:rgb(66, 209, 5);
  color: white;
  padding: 16px 32px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

h1 {
  font-size: 1.5rem;
}

span {
  background-color: #378705;
  padding: 6px 14px;
  border-radius: 20px;
  font-size: 0.9rem;
}
</style>