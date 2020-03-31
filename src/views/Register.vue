<template>
  <div class="register">
    <div class="pg_header">
      <a class="logo">LOGO</a>
      <a class="pg_dl" id="i77">注册</a>
    </div>
    <form id="form" name="tijiao">
      <div class="left"></div>
      <div class="pg_body">
        <div class="menu">用户名:</div>
        <div class="kong">
          <input id="text1" type="text" name="01" v-model="username" />
          <span id="div1" class="tian" style="margin-top: 4px">*(为必填)</span>
        </div>
        <div class="menu">密码:</div>
        <div class="kong">
          <input id="text2" type="password" name="02" onblur="check()" v-model="password" />
          <span id="div2" class="tian" style="margin-top: 5px">*(为必填)</span>
        </div>
        <div class="menu">确认密码:</div>
        <div class="kong">
          <input id="text3" type="password" name="01" onblur="check()" v-model="surepassword" />
          <span id="div3" class="tian">*(为必填)</span>
        </div>
        <div class="menu">手机号码:</div>
        <div class="kong">
          <input id="i5" type="text" name="01" v-model="phoneNumber" />
        </div>
        <div class="menu">邮箱地址:</div>
        <div class="kong">
          <input id="text4" type="text" name="01" onblur="check()" v-model="examil" />
        </div>

        <input id="i111" type="submit" name="002" value="注  册" @click="postdata" />
        <p style="width: 200px;display: inline-block;"></p>
        <input id="i222" type="button" name="004" value="取  消" />
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: 'Register',
  data () {
    return {
      username: '输入用户名',
      paaaword: '123456',
      surepassword: '123456',
      phoneNumber: ' ',
      examil: ''
    }
  },
  methods: {
    postdata () {
      var div = document.getElementById('div1')
      div.innerHTML = ''
      var a = function checkname () {
        var name1 = this.username
        if (name1 === '') {
          div.innerHTML = '用户名不能为空！'
          document.tijiao.text1.focus()
          return false
        }
        if (name1.length < 4 || name1.length > 16) {
          div.innerHTML = '长度4-16个字符'
          document.tijiao.text1.select()
          return false
        }
        var charname1 = name1.toLowerCase()
        for (var i = 0; i < name1.length; i++) {
          var charname = charname1.charAt(i)
          if (
            !(charname >= 0 && charname <= 9) &&
            !(charname >= 'a' && charname <= 'z') &&
            charname !== '_'
          ) {
            div.innerHTML = '用户名包含非法字符'
            document.form1.text1.select()
            return false
          }
        }
        return true
      }
      if (a) {
        console.log('验证成功！！!')
      }
    }
  }
}
</script>

<style scoped>
.pg_header {
  width: 1260px;
  height: 48px;
  top: 0;
  left: 0;
  right: 0;
  background-color: #2459a2;
  line-height: 48px;
}
.pg_header .logo {
  margin: 0 auto;
  float: left;
  width: 200px;
  text-align: center;
  line-height: 48px;
  font-size: 28px;
  color: white;
}
.pg_dl {
  display: inline-block;
  padding: 0 40px;
  color: white;
  font-size: 15px;
  margin-left: -8.206rem;
}
.pg_header .pg_dl:hover {
  background-color: #2459fb;
  cursor: pointer;
}
.left {
  margin-top: 20px;
  width: 400px;
  display: inline-block;
  /*   float: left;*/
}
.pg_body {
  margin-top: 50px;
  font-size: 18px;
  display: inline-block;
  width: -100px;
  margin-left: 200px;
}

.pg_body .menu {
  width: 150px;
  padding: 15px;
  font-weight: bold;
  margin-left: -100px;
}

input[type="text"] {
  width: 200px;
  height: 25px;
  border-radius: 6px;
}
input[type="password"] {
  width: 200px;
  height: 25px;
  border-radius: 6px;
}
#i111 {
  background-color: #555555;
  border: none;
  color: white;
  padding: 12px 29px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 17px;
  cursor: pointer;
  border-radius: 4px;
  position: absolute;
  margin-top: 0.150794rem;
  margin-left: -0.754rem;
}
#i222 {
  background-color: #555555;
  border: none;
  color: white;
  padding: 12px 29px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 17px;
  cursor: pointer;
  border-radius: 4px;
  position: absolute;
  margin-left: -4.198rem;
  margin-top: 0.150794rem;
}

.kong {
  margin-top: -54px;
  margin-left: 200px;
  float: left;
  padding: 15px;
}

.img {
  width: 50px;
  height: 40px;
}
.tian {
  color: red;
  float: right;
  font-size: 12px;
  margin-right: -120px;
  margin-top: 5px;
}
</style>
