<template>
  <div class="land">
    <div class="hander">
      <div class="p1">
        <img :src="log1" class="img-responsive" />
      </div>
      <div class="pr1">儿童营养配餐推送平台</div>
      <div class="til1">&#xe622;</div>
      <div class="til11">健康分析</div>
      <div class="til2">&#xe60d;</div>
      <div class="til22">营养配餐</div>
      <div class="til3">&#xe628;</div>
      <div class="til33">合理食谱</div>
      <div class="log">&#xe624;</div>
      <router-link to="/register" style="color:black" class="log2">注册</router-link>
    </div>
    <div class="body">
      <div class="cen1">
        <div class="pic">
          <img :src="log2" class="img-responsive" />
        </div>
        <div id="right">
          账号：
          <input class="one" type="text" name="账号：" value="账号" v-model="username" />
          <br />密码：
          <input class="two" type="password" name="密码" value="密码" v-model="password" />
          <br />
          <input class="three" type="submit" name="登陆" value="登陆" @click="land" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import pic from '@/assets/3.gif'
import pic2 from '@/assets/5.gif'
import axios from 'axios'

export default {
  name: 'Land',
  data () {
    return {
      log1: pic,
      log2: pic2,
      username: 'root',
      password: 'root'
    }
  },
  methods: {
    land: function () {
      var self = this
      axios
        .post('http://120.76.137.149:8181/user/login', {
          username: this.username,
          password: this.password
        })
        .then(function (response) {
          console.log(response)
          console.log(self)
          self.$router.push({ path: '/home' })
        })
        .catch(function (error) {
          console.log(error)
        })
    }
  }
}
</script>

<style scoped>
@font-face {
  font-family: "iconfont"; /* project id 1630148 */
  src: url("http://at.alicdn.com/t/font_1630148_z0c6u1pkw7l.eot");
  src: url("http://at.alicdn.com/t/font_1630148_z0c6u1pkw7l.eot?#iefix")
      format("embedded-opentype"),
    url("http://at.alicdn.com/t/font_1630148_z0c6u1pkw7l.woff2") format("woff2"),
    url("http://at.alicdn.com/t/font_1630148_z0c6u1pkw7l.woff") format("woff"),
    url("http://at.alicdn.com/t/font_1630148_z0c6u1pkw7l.ttf")
      format("truetype"),
    url("http://at.alicdn.com/t/font_1630148_z0c6u1pkw7l.svg#iconfont")
      format("svg");
}
.pic {
  width: 319px;
  height: 236px;
}
.cen1 {
  width: 700px;
  height: 300px;
  background-color: white;
  position: absolute;
  left: 50%;
  top: 50%;
  margin-top: -150px;
  margin-left: -350px;
}
#right {
  width: 223px;
  height: 218px;
  background-color: #87ceeb24;
  position: absolute;
  left: 60%;
  top: 50%;
  margin-top: -111px;
  margin-left: -56px; /*组件真实宽度的一半 这里是600的一半*/
}
.log {
  font-family: "iconfont";
  position: absolute;
  width: 50px;
  height: 50px;
  font-size: 41px;
  margin-left: 1002px;
  margin-top: 49px;
}
.log2 {
  width: 69px;
  height: 34px;
  background: white;
  border: none;
  position: absolute;
  margin-top: 52px;
  margin-left: 420px;
  font-size: 21px;
}
.land {
  width: 1260px;
  height: 500px;
  background-color: white;
  margin: auto;
  position: relative;
}
.hander {
  width: 1260px;
  height: 110px;
  margin: auto;
  background-color: white;
}
.p1 {
  width: 100px;
  height: 93px;
  position: absolute;
  margin-top: 10px;
  margin-left: 167px;
}
.pr1 {
  width: 350px;
  height: 50px;
  position: absolute;
  margin-top: 20px;
  margin-left: 240px;
  font-size: 25px;
  font-style: italic;
  font-weight: bold;
  color: #3adc00;
}
.body {
  width: 1260px;
  height: 500px;
  position: relative;
  background-color: #43ff00cf;
}
.cen1 {
  width: 700px;
  height: 300px;
  background-color: white;
  position: absolute;
  left: 50%;
  top: 50%;
  margin-top: -150px;
  margin-left: -350px;
}
#right {
  width: 223px;
  height: 218px;
  background-color: #87ceeb24;
  position: absolute;
  left: 60%;
  top: 50%;
  margin-top: -111px;
  margin-left: -56px; /*组件真实宽度的一半 这里是600的一半*/
  font-size: 15px;
}
.one {
  width: 139px;
  height: 25px;
  margin-top: 20px;
  margin-left: -3px;
  background-color: gainsboro;
}
.two {
  width: 139px;
  height: 25px;
  margin-top: 25px;
  margin-left: -3px;
  background-color: gainsboro;
}
.three {
  width: 176px;
  height: 38px;
  margin-top: 27px;
  margin-left: 29px;
  background-color: gainsboro;
}
.til1 {
  font-family: "iconfont";
  width: 70px;
  height: 50px;
  position: absolute;
  font-size: 22px;
  margin-left: 570px;
  margin-top: 25px;
}
.til11 {
  width: 67px;
  height: 10px;
  position: absolute;
  margin-left: 615px;
  margin-top: 28px;
  font-size: 15px;
}
.til2 {
  font-family: "iconfont";
  width: 70px;
  height: 50px;
  position: absolute;
  font-size: 22px;
  margin-left: 680px;
  margin-top: 25px;
}
.til22 {
  width: 67px;
  height: 10px;
  position: absolute;
  font-size: 15px;
  margin-left: 720px;
  margin-top: 30px;
}
.til3 {
  font-family: "iconfont";
  width: 70px;
  height: 50px;
  position: absolute;
  font-size: 22px;
  margin-left: 790px;
  margin-top: 25px;
}
.til33 {
  width: 67px;
  height: 10px;
  font-size: 15px;
  position: absolute;
  margin-left: 835px;
  margin-top: 29px;
}
</style>
