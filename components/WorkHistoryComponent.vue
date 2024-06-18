<template>
  <div
    v-for="{ startDate, endDate, title, location, details } in history"
    :key="title"
    class="work-experience"
  >
    <div class="experience-date">
      <span>{{ startDate }} - {{ endDate }}</span>
    </div>
    <div class="experience-details">
      <h1>{{ title }}</h1>
      <h2>{{ location }}</h2>
      <p>{{ details }}</p>
    </div>
  </div>
</template>

<script setup>
// eslint-disable-next-line import/no-unresolved, import/extensions
import history from '~/data/history';
</script>

<style scoped>
.work-experience {
  display: flex;
  color: white;
  gap: 1em;
  padding-bottom: 2em;
}

.experience-date {
  flex: 1.2 1;
}

.experience-details {
  flex: 3 1;
}

.experience-details h1 {
  margin-top: 0;
}

.experience-details h2 {
  font-size: 1em;
  font-weight: 300;
  color: #466fff;
}

.experience-date span {
  background-color: #272f52;
  padding: 0.5em;
  border-radius: 10px;
  display: block;
  text-align: center;
}

@media screen and (max-width: 500px) {
  .work-experience {
    flex-direction: column;
  }
}
</style>
