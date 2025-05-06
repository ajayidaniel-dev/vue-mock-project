<script setup>
import JobListing from '../components/JobListing.vue'
import Hero from '../components/Hero.vue'
import HomeCards from '../components/HomeCards.vue'
</script>

<template>
  <Hero />
  <HomeCards />
  <JobListing :limit="3" :showViewAll="true" />
</template>
