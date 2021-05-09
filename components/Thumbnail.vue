<template>
  <div class="thumbnail">
    <img :src="src" width="100%" height="100%" />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  props: {
    src: {
      type: String,
      default: null,
    },
  },
})
</script>

<style scoped>
.thumbnail {
  overflow: hidden;
  max-width: 640px;
  height: 100%;
  border-radius: 8px;
  box-shadow: 4px 4px 32px rgba(0, 0, 0, 0.2);

  /* Animation */
  animation: thumbnail-in 1.2s cubic-bezier(0, 0.7, 0.3, 1) both;
}

.thumbnail img {
  animation: thumbnail-zoom-out 1.2s cubic-bezier(0, 0.7, 0.3, 1) both;
}
</style>

<style>
@keyframes thumbnail-in {
  0% {
    transform: translateY(50px);
  }
  100% {
    transform: translate(0);
  }
}

@keyframes thumbnail-zoom-out {
  0% {
    transform: scale(1.2);
  }
  100% {
    transform: scale(1);
  }
}
</style>
