<template>
  <div class="nutritionpackage">
    <Hander />
    <div class="box">
      <div class="main">
        <div class="main1" v-show="showdata">
          <NutritionPackageCenter />
        </div>
        <div class="main2" v-show="!showdata">
          <NutritionPackageCenter />
        </div>
      </div>
      <div class="left">
        <NutritionPRight @myEvent="getdata" />
      </div>
    </div>
  </div>
</template>

<script>
import Hander from "@/components/Hander.vue";
import NutritionPackageCenter from "@/components/NutritionPackageCenter.vue";
import NutritionPRight from "@/components/NutritionPRight.vue";

export default {
  name: "NutritionPackage",
  components: {
    Hander,
    NutritionPackageCenter,
    NutritionPRight
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
