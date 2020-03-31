<template>
  <div class="nutritiousmeals">
    <Hander />
    <NutritiousMealCenter />
  </div>
</template>

<script>
import Hander from '@/components/Hander.vue'
import NutritiousMealCenter from '@/components/NutritiousMealCenter.vue'

export default {
  name: 'NutritiousMeal',
  components: {
    Hander,
    NutritiousMealCenter
  }
}
</script>

<style  scoped>
</style>
