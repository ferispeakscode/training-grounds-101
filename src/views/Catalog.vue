<template>
  <div class="catalog">
      <img alt="Vue logo" src="../assets/logo.png">
      <h1>Welcome to our catalog</h1>
  </div>
  <div>
      <CatalogFormat />
  </div>
</template>

<script>
import CatalogFormat from '@/components/CatalogFormat.vue'

export default {
    components: {
        CatalogFormat
    }

}
</script>

<style>

</style>