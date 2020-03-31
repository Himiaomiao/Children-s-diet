<template>
  <div class="student">
    <Hander />
    <div class="box">
      <div class="main">
        <div class="main1" v-show="showdata">
          <StudentCenter />
        </div>
        <div class="main2" v-show="!showdata">
          <StudentCenter />
        </div>
      </div>
      <div class="left">
        <Right @myEvent="getdata" />
      </div>
    </div>
  </div>
</template>

<script>
import Hander from "@/components/Hander.vue";
import StudentCenter from "@/components/StudentCenter.vue";
import Right from "@/components/Right.vue";

export default {
  name: "Student",
  components: {
    Hander,
    StudentCenter,
    Right
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
