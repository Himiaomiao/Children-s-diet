<template>
  <div class="right">
    <div class="box">
      <div class="box1" v-show="myshow">
        <div class="top1">
          <div class="top11" @click="isshow">&#xe798;</div>
          <div class="top12">
            <div class="top121" @click="get">&#xe604;</div>
            <div class="top122" @click="get">平台套餐库</div>
          </div>
          <div class="top13">
            <div class="top131">&#xe603;</div>
            <div class="top133">
              <el-button type="text" @click="open">新增套餐</el-button>
            </div>
          </div>
          <div class="mytop">
            <div class="mytop1">&#xe614;</div>
            <div class="mytop2">我的套餐</div>
          </div>
        </div>
      </div>
      <div class="box2" v-show="!myshow">
        <div class="top2">
          <div class="top22" @click="isshow">&#xe774;</div>
        </div>
        <div class="top23">
          <div class="top221" @click="get">&#xe603;</div>
        </div>
        <div class="top24">
          <div class="top221">&#xe604;</div>
        </div>
        <div class="top25">
          <div class="top221">&#xe614;</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "NutritionPRight",

  data() {
    return {
      myshow: true
    };
  },
  methods: {
    isshow() {
      this.myshow = !this.myshow;
      this.$emit("myEvent", this.myshow);
    },
    get() {
      this.$router.go(0);
    },
    open() {
      this.$confirm(
        "检测到未保存的内容，是否在离开页面前保存修改？",
        "确认信息",
        {
          distinguishCancelAndClose: true,
          confirmButtonText: "保存",
          cancelButtonText: "放弃修改"
        }
      )
        .then(() => {
          this.$message({
            type: "info",
            message: "保存修改"
          });
        })
        .catch(action => {
          this.$message({
            type: "info",
            message:
              action === "cancel" ? "放弃保存并离开页面" : "停留在当前页面"
          });
        });
    }
  }
};
</script>

<style  scoped>
@font-face {
  font-family: "iconfont"; /* project id 1630148 */
  src: url("http://at.alicdn.com/t/font_1630148_d9s0o9kbwk.eot");
  src: url("http://at.alicdn.com/t/font_1630148_d9s0o9kbwk.eot?#iefix")
      format("embedded-opentype"),
    url("http://at.alicdn.com/t/font_1630148_d9s0o9kbwk.woff2") format("woff2"),
    url("http://at.alicdn.com/t/font_1630148_d9s0o9kbwk.woff") format("woff"),
    url("httP://at.alicdn.com/t/font_1630148_d9s0o9kbwk.ttf") format("truetype"),
    url("httP://at.alicdn.com/t/font_1630148_d9s0o9kbwk.svg#iconfont")
      format("svg");
}

.box1 {
  width: 150px;
  height: 510px; /*no*/
  background-color: chartreuse;
}
.top1 {
  width: 150px;
  height: 40px;
  background-color: #a9a9a957;
}
.top11 {
  font-family: "iconfont";
  font-size: 30px;
  color: #eeffff70;
  position: absolute;
  margin-left: 60px;
}
.top12 {
  width: 150px;
  height: 50px;
  background-color: #a9a9a957;
  position: absolute;
  margin-top: 75px;
}
.top121 {
  font-family: "iconfont";
  font-size: 25px;
  position: absolute;
  margin-left: 30px;
  margin-top: 10px;
}
.top122 {
  font-size: 15px;
  color: black;
  position: absolute;
  margin-left: 60px;
  margin-top: 12px;
}
.top13 {
  width: 150px;
  height: 50px;
  background-color: #a9a9a957;
  position: absolute;
  margin-top: 160px;
}
.top131 {
  font-family: "iconfont";
  font-size: 25px;
  color: black;
  position: absolute;
  margin-left: 30px;
  margin-top: 10px;
}
.top133 {
  font-size: 15px;
  color: black;
  position: absolute;
  margin-left: 60px;
  margin-top: 12px;
}
.mytop {
  width: 150px;
  height: 50px;
  background-color: #a9a9a957;
  position: absolute;
  margin-top: 250px;
}
.mytop1 {
  font-family: "iconfont";
  font-size: 25px;
  color: black;
  position: absolute;
  margin-left: 30px;
  margin-top: 10px;
}
.mytop2 {
  font-size: 15px;
  color: black;
  position: absolute;
  margin-left: 60px;
  margin-top: 12px;
}
.box2 {
  width: 50px;
  height: 510px; /*no*/
  background-color: chartreuse;
}
.top2 {
  width: 50px;
  height: 50px;
  background-color: #a9a9a957;
}
.top22 {
  font-family: "iconfont";
  font-size: 30px;
  color: #eeffff70;
}
.top23 {
  width: 50px;
  height: 50px;
  background-color: #a9a9a957;
  position: absolute;
  margin-top: 75px;
}
.top221 {
  font-family: "iconfont";
  font-size: 25px;
  position: absolute;
  margin-left: 5px;
  margin-top: 10px;
}
.top24 {
  width: 50px;
  height: 50px;
  background-color: #a9a9a957;
  position: absolute;
  margin-top: 16 px;
}
.top25 {
  width: 50px;
  height: 50px;
  background-color: #a9a9a957;
  position: absolute;
  margin-top: 150px;
}
</style>
