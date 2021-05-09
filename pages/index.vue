<template>
  <div class="container">
    <div>
      <page-title title="Gallery" />
    </div>
    <div>
      <thumbnail src="/soranokakera.png" />
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Thumbnail from '~/components/Thumbnail.vue'
import PageTitle from '~/components/PageTitle.vue'

export default Vue.extend({
  components: { PageTitle, Thumbnail },
})
</script>

<style>
.container {
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-flow: column;
}

.title {
  font-size: 4rem;
}
</style>
