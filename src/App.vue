<template>
  <div>
    <AppHeader :wishlistCount="wishlistCount" />
    <div class="catalogue">
      <CourseCard
        v-for="course in courses"
        :key="course.id"
        :title="course.title"
        :chef="course.chef"
        :level="course.level"
        :price="course.price"
        :available="course.available"
        @save="wishlistCount++"
      />
    </div>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue'
import CourseCard from './components/CourseCard.vue'
import courses from './data/courses.js'

export default {
  name: 'App',
  components: { AppHeader, CourseCard },
  data() {
    return {
      courses: courses,
      wishlistCount: 0
    }
  }
}
</script>

<style>
.catalogue {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
  gap: 24px;
  padding: 32px;
}
</style>
