<template>
  <div class="home">
    <Hander />
    <CenterLeft />
  </div>
</template>

<script>
// @ is an alias to /src
import Hander from '@/components/Hander.vue'
import CenterLeft from '@/components/CenterLeft.vue'
export default {
  name: 'Home',
  components: {
    Hander,
    CenterLeft
  }
}
</script>

<style  scoped>
</style>
