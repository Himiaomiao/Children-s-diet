<template>
  <div class="CenterLeft">
    <div class="left1">
      <span>
        <p>知识播报</p>
      </span>
    </div>
    <div class="left2">
      <div class="left22">
        <img class="img-responsive" :src="log9" @click="getpassage1" />
      </div>
      <div class="p2">食物营养素含量</div>
    </div>
    <div class="left3">
      <div class="left33">
        <img class="img-responsive" :src="log9" @click="getpassage2" />
      </div>
      <div class="p3">营养标准知识</div>
    </div>
    <div class="left4">
      <div class="left44">
        <img class="img-responsive" :src="log9" @click="getpassage3" />
      </div>
      <div class="p4">食物禁忌</div>
    </div>
    <div class="left5">
      <div class="left55">
        <img class="img-responsive" :src="log9" @click="getpassage4" />
      </div>
      <div class="p5">营养素知识</div>
    </div>
    <div class="middle">
      <div class="middle1">
        <img class="img-responsive" :src="mid" />
      </div>
      <!-- eslint-disable-next-line -->
      <textarea class="passage1" @click="getpassage1" v-if="myshow1"></textarea>
      <textarea class="passage2" @click="getpassage2" v-if="myshow2">456</textarea>
      <textarea class="passage3" @click="getpassage3" v-if="myshow3">789</textarea>
      <textarea class="passage4" @click="getpassage4" v-if="myshow4">90</textarea>
    </div>
  </div>
</template>

<script>
import pic from "@/assets/log9.gif";
import pic2 from "@/assets/mid.gif";
export default {
  name: "CenterLeft",
  data() {
    return {
      myshow1: true,
      myshow2: false,
      myshow3: false,
      myshow4: false,

      log9: pic,
      mid: pic2
    };
  },
  methods: {
    getpassage1() {
      this.myshow1 = true;
      this.myshow2 = false;
      this.myshow3 = false;
      this.myshow4 = false;
    },
    getpassage2() {
      this.myshow2 = true;
      this.myshow1 = false;
      this.myshow3 = false;
      this.myshow4 = false;
    },
    getpassage3() {
      this.myshow3 = true;
      this.myshow1 = false;
      this.myshow2 = false;
      this.myshow4 = false;
    },
    getpassage4() {
      this.myshow4 = true;
      this.myshow1 = false;
      this.myshow2 = false;
      this.myshow3 = false;
    }
  }
};
</script>

<style  scoped>
.CenterLeft {
  width: 263px;
  height: 500px;
  background-color: #3adc0099;
}
.left1 {
  width: 253px;
  height: 35px;
  position: absolute;
  opacity: 0.5;
  background-color: azure;
  margin-top: 2px;
  margin-left: 3px;
  text-align: center;
}
.left1 span {
  line-height: -0.73rem;
  font-size: 15px;
}
.left2 {
  width: 253px;
  height: 35px;
  position: absolute;
  opacity: 0.5;
  background-color: azure;
  margin-top: 52px;
  margin-left: 3px;
  text-align: center;
}
.left22 {
  width: 27px;
  height: 27px;
  position: absolute;
  margin-left: 30px;
  margin-top: -3px;
}
.p2 {
  font-size: 15px;
}
.left3 {
  width: 253px;
  height: 35px;
  position: absolute;
  opacity: 0.5;
  background-color: azure;
  margin-top: 109px;
  margin-left: 3px;
  text-align: center;
}
.left33 {
  width: 27px;
  height: 27px;
  position: absolute;
  margin-left: 30px;
  margin-top: -3px;
}
.p3 {
  font-size: 15px;
}
.left4 {
  width: 253px;
  height: 35px;
  position: absolute;
  opacity: 0.5;
  background-color: azure;
  margin-top: 161px;
  margin-left: 3px;
  text-align: center;
}
.left44 {
  width: 27px;
  height: 27px;
  position: absolute;
  margin-left: 30px;
  margin-top: -3px;
}
.p4 {
  font-size: 15px;
}
.left5 {
  width: 253px;
  height: 35px;
  position: absolute;
  opacity: 0.5;
  background-color: azure;
  margin-top: 210px;
  margin-left: 3px;
  text-align: center;
}
.left55 {
  width: 27px;
  height: 27spx;
  position: absolute;
  margin-left: 30px;
  margin-top: -3px;
}
.p5 {
  font-size: 15px;
}
.middle {
  width: 810px;
  height: 500px;
  position: absolute;
  margin-left: 277px;
  margin-top: 0px;
  background-color: white;
}
.middle1 {
  width: 120px;
  height: 95px;
  position: absolute;
  margin-left: 10px;
  margin-top: 10px;
}
.passage1 {
  width: 567px;
  height: 397px;
  background-color: antiquewhite;
  position: absolute;
  margin-top: 79px;
  margin-left: -1.619rem;
  font-size: 15px;
}
.passage2 {
  width: 567px;
  height: 397px;
  background-color: antiquewhite;
  position: absolute;
  margin-top: 79px;
  margin-left: -1.619rem;
  font-size: 15px;
}
.passage3 {
  width: 567px;
  height: 397px;
  background-color: antiquewhite;
  position: absolute;
  margin-top: 79px;
  margin-left: -1.619rem;
  font-size: 15px;
}
.passage4 {
  width: 567px;
  height: 397px;
  background-color: antiquewhite;
  position: absolute;
  margin-top: 79px;
  margin-left: -1.619rem;
  font-size: 15px;
}
</style>
