<template>
  <div class="card">
    <img :src="image" :alt="title" class="course-image"/>
    <h2>{{ title }}</h2>
    <p>Chef: {{ chef }}</p>
    <p>Level: {{ level }}</p>
    <p>Price: R{{ price }}</p>
    <button v-if="available" @click="saveClicked">Save</button>
    <p v-else class="sold-out">Sold Out</p>
    
  </div>
</template>

<script>
export default {
  name: 'CourseCard',
  props: {
    title: String,
    chef: String,
    level: String,
    price: Number,
    available: Boolean,
    image: String
  },
  methods: {
    saveClicked() {
      this.$emit('save')
    }
  }
}
</script>

<style scoped>
.card {
  background-color: white;
  border-radius: 10px;
  padding: 20px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
}

h2 {
  font-size: 1.2rem;
  margin-bottom: 8px;
  color: #000000;
}

p {
  color: #000000;
  margin-bottom: 6px;
  font-size: 0.95rem;
}

button {
  margin-top: 12px;
  padding: 8px 20px;
  background-color: #191919;
  color: rgb(243, 247, 243);
  border: none;
  border-radius: 6px;
  cursor: pointer;
  font-size: 0.9rem;
}

button:hover {
  background-color: #3d423c;
  color:#f7f5f5
}

.sold-out {
  margin-top: 12px;
  color: #000000;
  font-weight: bold;
}

.course-image {
  width: 100%;
  height: 160px;
  object-fit: cover;
  border-radius: 8px;
  margin-bottom: 12px;
}
</style>