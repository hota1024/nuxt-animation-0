<template>
  <h1 class="title">
    <span
      v-for="(c, i) in title"
      :key="i"
      class="title-char"
      :style="charStyle(i)"
      >{{ c }}</span
    >
  </h1>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  props: {
    title: {
      type: String,
      default: '',
    },
  },
  methods: {
    charStyle(i: number) {
      return {
        animation: `title-char-in 0.6s cubic-bezier(0,.7,.3,1) both ${
          0.2 + i * 0.02
        }s`,
      }
    },
  },
})
</script>

<style scoped>
.title {
  /* Font */
  font-size: 4rem;
  color: #202040;

  /* Background */
  background-image: linear-gradient(135deg, #63aaf8, #4481e2);
  background-repeat: no-repeat;
  background-position: 10px bottom;
  padding-right: 10px;

  /* Animation */
  animation: title-background-in 1s cubic-bezier(0.6, 0.2, 0, 1) both;
}

.title-char {
  opacity: 0;
  display: inline-block;
}
</style>

<style>
@keyframes title-background-in {
  0% {
    background-size: 0 30%;
  }
  100% {
    background-size: 100% 30%;
  }
}

@keyframes title-char-in {
  0% {
    transform: translateY(50px) rotate(6deg);
    opacity: 0;
  }
  100% {
    transform: translate(0) rotate(0.1deg);
    opacity: 1;
  }
}
</style>
