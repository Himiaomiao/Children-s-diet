<template>
  <div class="hander">
    <div class="top">
      <div class="box1">
        <img class="img-responsive" :src="log1" />
      </div>
      <div class="box11">
        <router-link to="/home" style="color:white">营养配餐系统</router-link>
      </div>
      <div class="box3">
        <img class="img-responsive" :src="log3" />
      </div>
      <div class="box33">
        <router-link to="/student" style="color:black">学生管理</router-link>
      </div>
      <div class="box4">
        <img class="img-responsive" :src="log4" />
      </div>
      <div class="box44">
        <router-link to="/nutritionalassessment" style="color:black">营养评估</router-link>
      </div>
      <div class="box5">
        <img class="img-responsive" :src="log5" />
      </div>
      <div class="box55">
        <router-link to="/nutritiousmeals" style="color:black">营养配餐</router-link>
      </div>
      <div class="box6">
        <img class="img-responsive" :src="log6" />
      </div>
      <div class="box66">
        <router-link to="/nutritionpackage" style="color:black">营养套餐</router-link>
      </div>
      <div class="box7">
        <img class="img-responsive" :src="log7" />
      </div>
      <div class="box77">
        <router-link to="/platformrecipelibrary" style="color:black">平台食谱库</router-link>
      </div>
      <div class="box8">
        <img class="img-responsive" :src="log8" />
      </div>
      <div class="box88">
        <router-link to="/" style="color:black">退出</router-link>
      </div>
    </div>
  </div>
</template>

<script>
import pic1 from "@/assets/lo1.gif";
import pic2 from "@/assets/lo2.png";
import pic3 from "@/assets/log3.png";
import pic4 from "@/assets/log4.png";
import pic5 from "@/assets/log5.png";
import pic6 from "@/assets/log6.png";
import pic7 from "@/assets/log7.png";
import pic8 from "@/assets/log8.png";

export default {
  name: "Hander",
  props: {
    msg: String
  },
  data() {
    return {
      log1: pic1,
      log2: pic2,
      log3: pic3,
      log4: pic4,
      log5: pic5,
      log6: pic6,
      log7: pic7,
      log8: pic8
    };
  },
  methods: {}
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@font-face {
  font-family: "iconfont"; /* project id 1630148 */
  src: url("http://at.alicdn.com/t/font_1630148_fts0u4tnzru.eot");
  src: url("http://at.alicdn.com/t/font_1630148_fts0u4tnzru.eot?#iefix")
      format("embedded-opentype"),
    url("http://at.alicdn.com/t/font_1630148_fts0u4tnzru.woff2") format("woff2"),
    url("http://at.alicdn.com/t/font_1630148_fts0u4tnzru.woff") format("woff"),
    url("http://at.alicdn.com/t/font_1630148_fts0u4tnzru.ttf")
      format("truetype"),
    url("http://at.alicdn.com/t/font_1630148_fts0u4tnzru.svg#iconfont")
      format("svg");
}
.top {
  width: 100vw;
  height: 100px;
  background-color: #3adc0099;
  border-bottom-style: solid;
  border-bottom-color: #3adc00;
}
.box1 {
  font-family: "iconfont";
  width: 50px;
  height: 50px;
  font-size: no 58px;
  position: absolute;
  margin-top: 10px;
  margin-left: 28px;
  color: white;
}
.box11 {
  position: absolute;
  margin-left: 92px;
  margin-top: 36px;
  font-size: 20px;
  color: white;
}
.box2 {
  width: 30px;
  height: 30px;
  position: absolute;
  margin-top: 16px;
  margin-left: 282px;
}
.box22 {
  position: absolute;
  margin-left: 262px;
  margin-top: 51px;
  font-size: 15px;
}
.box3 {
  width: 30px;
  height: 30px;
  position: absolute;
  margin-top: 18px;
  margin-left: 377px;
}
.box33 {
  position: absolute;
  margin-left: 361px;
  margin-top: 51px;
  font-size: 15px;
}
.box4 {
  width: 30px;
  height: 30px;
  position: absolute;
  margin-top: 17px;
  margin-left: 469px;
}
.box44 {
  position: absolute;
  margin-left: 450px;
  margin-top: 51px;
  font-size: 15px;
}
.box5 {
  width: 30px;
  height: 29px;
  position: absolute;
  margin-top: 18px;
  margin-left: 566px;
}
.box55 {
  position: absolute;
  margin-left: 548px;
  margin-top: 51px;
  font-size: 15px;
}
.box6 {
  width: 40px;
  height: 40px;
  position: absolute;
  margin-top: 16px;
  margin-left: 656px;
}
.box66 {
  position: absolute;
  margin-left: 644px;
  margin-top: 51px;
  font-size: 15px;
}
.box7 {
  width: 40px;
  height: 30px;
  position: absolute;
  margin-top: 23px;
  margin-left: 762px;
}
.box77 {
  position: absolute;
  margin-left: 739px;
  margin-top: 49px;
  font-size: 15px;
}
.box8 {
  width: 30px;
  height: 30px;
  position: absolute;
  margin-top: 42px;
  margin-left: 989px;
}
.box88 {
  position: absolute;
  margin-left: 1027px;
  margin-top: 47px;
  font-size: 15px;
}
</style>
