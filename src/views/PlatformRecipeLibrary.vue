<template>
  <div class="nutritionpackage">
    <Hander />
    <div class="box">
      <div class="main">
        <div class="main1" v-show="showdata">
          <PlatformRecipeLibraryCenter />
        </div>
        <div class="main2" v-show="!showdata">
          <PlatformRecipeLibraryCenter />
        </div>
      </div>
      <div class="left">
        <PlatformRRight @myEvent="getdata" />
      </div>
    </div>
  </div>
</template>

<script>
import Hander from "@/components/Hander.vue";
import PlatformRecipeLibraryCenter from "@/components/PlatformRecipeLibraryCenter.vue";
import PlatformRRight from "@/components/PlatformRRight.vue";

export default {
  name: "PlatformRecipeLibrary",
  components: {
    Hander,
    PlatformRecipeLibraryCenter,
    PlatformRRight
  },
  data() {
    return {
      showdata: true
    };
  },
  methods: {
    getdata(data) {
      console.log(data);
      this.showdata = data;
    }
  }
};
</script>

<style  scoped>
.box {
  width: 1260px;
}
.left {
  position: absolute;
  margin-left: 0px;
}
.main1 {
  width: 1100px;

  margin-top: 20px;
  float: right;
}
.main2 {
  width: 1200px;
  margin-top: 20px;
  float: right;
}
</style>
