<template>
  <div id="register">
<<<<<<< HEAD
    <div class="reg-top">
      <div class="py-container top">
        <div class="top_left">
          <refHeader></refHeader>
          <p class="title">账户注册</p>
        </div>
        <span class="go">我已注册，<router-link :to="{path: '/login'}">马上登录</router-link>></span>
      </div>
=======
    <keep-alive>
      <router-view></router-view>
    </keep-alive>
    <div class="reg-top">
      <div class="py-container">
      <div class="top">
      <div class="top_left">
        <div class="h-logo" ref='logoIsCursor'>
          <router-link :to="{path: isHome}" ><img src="static/img/logo-118-69.png"></router-link>
        </div>
        <p class="title">账户注册</p>
      </div>
      <span class="go">我已注册，<router-link :to="{path: '/login'}">马上登录</router-link>></span>
    </div>
    </div>
>>>>>>> remotes/origin/master
    </div>
    <div class="reg-middle">
      <div class="py-container">
        <div class="middle">
          <section class="middle-title">
<<<<<<< HEAD
            <div class="title">
              <a class="title_com" :href="AFTERIP + '/#/register'" target="_blank">企业账户注册</a>
            </div>
            <div class="title active">
              <a class="fixed-height">
                <img src="static/img/reg/reg_slice_active1.png" class="reduce-height">
                <p class="title-text">个人账户注册</p>
=======
            <div class="title " :class="{active: show === 0}" @click="companyShow()">
              <a class="fixed-height" @click="changeShowType='company'">
              <img :src="show ===0? 'static/img/reg/reg_rectangle_active1.png' :'./../../static/img/reg/reg_rectangle1.png'">
              <p class="title-text ">企业账户注册</p>
              </a>
            </div>
            <div class="title" :class="{active: show === 1}" @click="personShow()">
              <a class="fixed-height" @click="changeShowType='person'">
              <img :src=" show===1? 'static/img/reg/reg_slice_active1.png' :'static/img/reg/reg_slice1.png'" class="reduce-height">
              <p class="title-text">个人账户注册</p>
>>>>>>> remotes/origin/master
              </a>
            </div>
          </section>
          <transition>
<<<<<<< HEAD
            <section>
              <span class="explain">无企业营业执照的个人用户请注册个人账户。权益如下：做个人实名认证；作为买家身份采购；</span>
              <div class="info">
                <form class="sui-form form-horizontal" @submit.prevent>
                  <div class="control-group">
                    <label class="control-label">会员名：</label>
                    <div class="controls">
                      <input type="text" placeholder="设置会员名" class="input-xfat input-xlarge" v-model="userName">
=======
            <section class="middle-contaiber " v-show="changeShowType ==='company'" :class="{ back: isAgree===false}">
              <span class="explain">有企业营业执照（含个体工商户）的用户请注册。权益如下：做企业实名认证；作为卖家身份开店；作为买家身份采购。</span>
              <div class="agreement" v-show="isAgree === false">
                <div class="regagreement">注册协议</div>
                <hr>
                <div class="agreement-detail">
                  <p>
                    <strong>【审慎阅读】</strong>您在申请注册流程中点击同意前，应当认真阅读以下协议。请您务必 <strong>审慎阅读、充分理解协议中相关条款内容，
                    其中包括：</strong>
                  </p>
                  <p> <strong>1、与您约定免除或限制责任的条款；</strong></p>
                  <p><strong>2、与您约定法律适用和管辖的条款；</strong></p>
                  <p><strong>3、其他以粗体下划线标识的重要条款</strong></p>
                  <p><strong>如您对协议有任何疑问，可向服务中心（请点击）咨询</strong></p>
                  <p>
                    <strong>
                      【特别提示】
                      您已充分理解，猴尾巴中国站是一个商业贸易采购平台内容 ，而并非面向消费者的消费购买市场，当您按照注册页面提示填写信息、阅读并同意协议且完成全部注册程序后，
                      即表示您已充分阅读、理解并接受协议的全部内容，并将基于您的真实贸易需求而使用平台服务。</strong>如您因平台服务与猴尾巴发生争议应适用《平台服务条款》处理;
                    如您在使用平台服务中与其他用户发生争议，依您与其他用户达成的协议处理。
                  </p>
                  <p><strong>阅读协议的过程中，如果您不同意相关协议或其中任何条款约定，您应立即停止注册程序。</strong></p>
                  <p><router-link :to="{name:'paas'}">《平台服务条款》</router-link></p>
                  <p><router-link :to="{name: 'privacy'}">《隐私权政策》</router-link></p>
                  <p><router-link :to="{name:'legal'}">《法律声明》</router-link></p>
                  <p><router-link :to="{name: 'pay'}">《支付交易协议》</router-link></p>
                </div>
                <button class="btn_agree" @click="agree()">同意并继续</button>
              </div>
              <div class="info"  v-show="isAgree === true">
                <form class="sui-form form-horizontal">
                  <div class="control-group">
                    <label class="control-label">会员名：</label>
                    <div class="controls">
                      <input type="text"  placeholder="设置会员名" class="input-xfat input-xlarge" v-model="userName">
                    </div>
                  </div>
                  <div class="control-group">
                    <label for="inputPassword" class="control-label">登录密码：</label>
                    <div class="controls">
                      <input type="password" placeholder="设置你的登录密码" class="input-xfat input-xlarge" v-model="password">
                    </div>
                  </div>
                  <div class="control-group">
                    <label for="inputPassword" class="control-label">确认密码：</label>
                    <div class="controls">
                      <input type="password" placeholder="请再次输入你的登录密码" class="input-xfat input-xlarge" v-model="REpassword">
                    </div>
                  </div>
                  <div class="control-group">
                    <label  class="control-label">联系人姓名：</label>
                    <div class="controls">
                      <input type="text"  placeholder="请输入真实名字" class="input-xfat input-xlarge" >
                    </div>
                  </div>
                  <div class="control-group">
                    <label class="control-label">企业名称：</label>
                    <div class="controls">
                      <input type="text" placeholder="请输入营业执照上的企业名称" class="input-xfat input-xlarge">
                    </div>
                  </div>
                  <div class="control-group">
                    <label class="control-label">手机号码：</label>
                    <div class="controls">
                      <select>
                        <option>中国大陆&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;+86</option>
                        <option>中国香港</option>
                      </select>
                      <input type="text" class="input-xfat input-xlarge mobile" maxlength="16" v-model="phoneValue">
                    </div>
                  </div>
                  <div class="control-group">
                    <label class="control-label">验证码：</label>
                    <div class="controls">
                      <input type="text" placeholder="请输入验证码" class="input-xfat input-xlarge" >
                    </div>
                  </div>
                  <div class="control-group">
                    <div class="controls">
                      <el-checkbox v-model="checked" >创建网站账号的同时，我同意遵守：<br><a ref="https://www.baidu.com">《平台服务条款》</a>及 <a ref="https://www.baidu.com">《隐私声明》</a></el-checkbox>
                    </div>
                  </div>
                  <div class="control-group">
                    <div class="controls btn-reg">
                      <a class="sui-btn btn-block btn-xlarge btn-danger" @click="register">同意并注册</a>
                    </div>
                  </div>
                </form>
              </div>
            </section>
          </transition>
          <transition>
            <section  v-show="changeShowType ==='person'">
              <span class="explain">无企业营业执照的个人用户请注册个人账户。权益如下：做个人实名认证；作为买家身份采购；</span>
              <div class="info">
                <form class="sui-form form-horizontal">
                  <div class="control-group">
                    <label class="control-label">会员名：</label>
                    <div class="controls">
                      <input type="text"  placeholder="设置会员名" class="input-xfat input-xlarge" v-model="userName">
>>>>>>> remotes/origin/master
                    </div>
                  </div>
                  <div class="control-group">
                    <label for="inputPassword" class="control-label">登录密码：</label>
<<<<<<< HEAD
                    <div class="controls password">
                      <input type="password" placeholder="设置你的登录密码" class="input-xfat input-xlarge" v-model="password">
                      <span>密码由数字、字母和字符组成 且长度为6-18位</span>
=======
                    <div class="controls">
                      <input type="password" placeholder="设置你的登录密码" class="input-xfat input-xlarge" v-model="password">
>>>>>>> remotes/origin/master
                    </div>
                  </div>
                  <div class="control-group">
                    <label for="inputPassword" class="control-label">确认密码：</label>
                    <div class="controls">
                      <input type="password" placeholder="请再次输入你的登录密码" class="input-xfat input-xlarge" v-model="REpassword">
                    </div>
                  </div>
                  <div class="control-group">
                    <label class="control-label">手机号码：</label>
                    <div class="controls">
<<<<<<< HEAD
                      <span class="select">中国大陆&nbsp;+86</span>
                      <input type="text" class="input-xfat input-xlarge mobile" maxlength="16" v-model="phoneValue">
                      <button class="getPhoneCode sui-btn" @click="sendCode()" v-if="time===60">获取验证码</button>
                      <button class="getPhoneCode" v-else>{{this.time}}秒后可重新获取</button>
=======
                      <select>
                        <option>中国大陆&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;+86</option>
                        <option>中国香港</option>
                      </select>
                      <input type="text" class="input-xfat input-xlarge mobile" maxlength="16" v-model="phoneValue">
                      <button class="getPhoneCode" @click="sendCode()">获取手机验证码</button>
>>>>>>> remotes/origin/master
                    </div>
                  </div>
                  <div class="control-group">
                    <label class="control-label">验证码：</label>
                    <div class="controls">
                      <input type="text" placeholder="请填写验证码" class="input-xfat input-xlarge" maxlength="16" v-model="smsCode">
                    </div>
                  </div>
                  <div class="control-group">
<<<<<<< HEAD
                    <div class="controls checkbox">
                      <input type="checkbox" name="" v-model="checked"><span>创建网站账号的同时，我同意遵守：</span><router-link :to="{path: '/register/paas', query:{person: true}}" style="color: #FF4606">《平台服务条款》</router-link>及 <router-link :to="{path: '/register/legal', query:{person: true}}" style="color: #FF4606">《隐私声明》</router-link>
=======
                    <div class="controls">
                      <el-checkbox v-model="checked" >创建网站账号的同时，我同意遵守：<br><a ref="https://www.baidu.com">《平台服务条款》</a>及<a ref="https://www.baidu.com">《隐私声明》</a></el-checkbox>
>>>>>>> remotes/origin/master
                    </div>
                  </div>
                  <div class="control-group">
                    <div class="controls btn-reg">
                      <a class="sui-btn btn-block btn-xlarge btn-danger " @click="register">同意并注册</a>
                    </div>
                  </div>
                </form>
              </div>
            </section>
          </transition>
          <div class="question">
<<<<<<< HEAD
            <img src="static/img/reg/reg_monkey1.png">
            <div class="know-more">
              <p>了解更多</p>
              <ul>
                <li><a>手机收不到验证码?</a></li>
                <li><a>会员账户注册不成功?</a></li>
                <li><a>个人账户可以开店吗?</a></li>
                <li><a>账户如何换名字?</a></li>
                <li><a>个人账户需要营业执照吗?</a></li>
                <li><a>其他问题</a></li>
              </ul>
              <div class="clikeme">
                <img src="static/img/reg/reg_oval1.png" />
                <span class="text">?</span>
                <a class="a">点我提问</a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <regFooter></regFooter>
  </div>
</template>
<script>
import regFooter from '@/components/regFooter'
import refHeader from '@/components/regHeader'
import { isMobile, isPassword } from '@/common/utils'
=======
        <img src="static/img/reg/reg_monkey1.png">
        <div class="know-more">
          <p>了解更多</p>
          <ul>
            <li><a>手机收不到验证码?</a></li>
            <li><a>会员账户注册不成功?</a></li>
            <li><a>个人账户可以开店吗?</a></li>
            <li><a>账户如何换名字?</a></li>
            <li><a>个人账户需要营业执照吗?</a></li>
            <li><a>其他问题</a></li>
          </ul>
          <div class="clikeme">
            <img src="static/img/reg/reg_oval1.png"/>
            <span class="text">?</span>
            <a class="a">点我提问</a>
          </div>
        </div>
      </div>
      </div>
      </div>
    </div>
    <div class="reg-bottom">
      <div class="py-container">
        <footer>
          <ul class="footer-list">
              <li class="footer-list-item">
                <a ref="http://www.baidu.com" >关于MKtail</a>&nbsp;&nbsp;||
              </li>
              <li class="footer-list-item">
                <a ref="http://www.baidu.com" >联系我们</a>&nbsp;&nbsp;||
              </li>
              <li class="footer-list-item">
                <a ref="http://www.baidu.com" >友情链接</a>&nbsp;&nbsp;||
              </li>
              <li class="footer-list-item">
                <a ref="http://www.baidu.com" >法律声明</a>&nbsp;&nbsp;||
              </li>
              <li class="footer-list-item">
                <a ref="http://www.baidu.com" >用户体验提升计划</a>&nbsp;&nbsp;||
              </li>
              <li class="footer-list-item">
                <a ref="http://www.baidu.com" >会员认证</a>&nbsp;&nbsp;||
              </li>
            </ul>
          <p>MKtail公司版权所有-粤ICP备京公网安备 <img src="static/img/reg/reg_ghs1.png">11010820220134号-京ICP证110507</p>
        </footer>
      </div>
    </div>
    <transition>
      <router-view></router-view>
    </transition>
  </div>
</template>
<script>
import { apiAxios } from '../../common/utils'
import { api } from '../../common/api'
>>>>>>> remotes/origin/master
export default {
  data () {
    return {
      userName: '', // 用户名
      password: '', // 密码
      REpassword: '', // 再次输入密码
      checked: false,
      phoneValue: '', // 13109098765
      flag: false, // 是否已发送验证码
      time: 60, // 验证码限制时间
      newsTip: '获取短信验证码',
<<<<<<< HEAD
      smsCode: ''
    }
  },
  components: {regFooter, refHeader},
=======
      smsCode: '',
      isHome: '',
      changeShowType: 'company', // 企业注册
      show: 0,
      isAgree: false // 是否同意注册条款
    }
  },
>>>>>>> remotes/origin/master
  methods: {
    sendCode () {
      if (this.flag) {
        this.$message.warning('验证码已发送，' + this.time + '秒后可重新获取')
        return false
      }
      if (this.phoneValue === null || this.phoneValue === '') {
<<<<<<< HEAD
        this.$message.warning('请输入手机号')
        return false
      }
      if (!isMobile(this.phoneValue)) {
        this.$message.warning('请输入正确的手机号')
        return false
      }
      this.API.sendCode({phoneNumbers: this.phoneValue}).then(res => {
        this.$message.success('验证码已发送')
        this.flag = true
        this.newsTip = this.time + '秒后可重新获取'
        this.setTime()
      })
    },
=======
        this.$message.warning('请输入填写手机号')
        return false
      }
      if (this.phoneValue.length !== 11) {
        this.$message.warning('请输入正确的手机号')
        return false
      }
      apiAxios.AxiosG({
        url: api.sendCode,
        params: {phone: this.phoneValue}
      }, rtn => {
        if (rtn.data.success) {
          this.$message.success(rtn.data.message)
          this.flag = true
          this.smsCode = rtn.data.data
          console.log(this.smsCode)
          this.newsTip = this.time + '秒后可重新获取'
          this.setTime()
        } else {
          this.$message.error(rtn.data.message)
        }
      })
    },
    change () {
      if (this.isActive === true) {
        this.isActive = false
      } else {
        this.isActive = true
      }
    },
>>>>>>> remotes/origin/master
    register () {
      // 比较两次输入的密码是否一致
      if (!this.userName || !this.password) {
        this.$message.warning('请输入完整信息')
        return false
      }
<<<<<<< HEAD
      if (!isPassword(this.password)) {
        this.$message.warning('输入密码至少包含字符、数字、字母中的两种')
        return false
      }
=======
>>>>>>> remotes/origin/master
      if (this.password !== this.REpassword) {
        this.$message.warning('两次输入密码不一致，请重新输入')
        return false
      }
      if (this.phoneValue === null || this.phoneValue === '') {
<<<<<<< HEAD
        this.$message.warning('请输入手机号')
        return false
      }
      if (!isMobile(this.phoneValue)) {
=======
        this.$message.warning('请输入填写手机号')
        return false
      }
      if (this.phoneValue.length !== 11) {
>>>>>>> remotes/origin/master
        this.$message.warning('请输入正确的手机号')
        return false
      }
      if (!this.flag) {
        this.$message.warning('请先获取验证码，再输入')
        return false
      }
      if (!this.smsCode) {
        this.$message.warning('请获取验证码')
        return false
      }
      if (!this.checked) {
        this.$message.warning('请先同意并且勾选协议~')
        return false
      }
<<<<<<< HEAD
=======
      console.log(this.smsCode, this.userName, this.userName)
>>>>>>> remotes/origin/master
      // 新增
      let user = {
        username: this.userName,
        password: this.password,
        phone: this.phoneValue
      }
<<<<<<< HEAD
      this.API.register(user, this.smsCode).then(res => {
        if (res.success === false) return false
        this.smsCode = ''
        this.time = 60
        this.password = ''
        this.REpassword = ''
        this.$message.success('注册成功')
        this.$router.push({path: '/login'})
      }).catch(() => {
        this.smsCode = ''
        this.time = 60
=======
      console.log(user, this.smsCode)
      apiAxios.AxiosP({
        url: api.register,
        params: {smscode: this.smsCode},
        data: user
      }, rtn => {
        if (rtn.data.success) {
          this.smsCode = ''
          this.time = 60
          this.password = ''
          this.REpassword = ''
          this.$message.success(rtn.data.message)
          this.$router.push({path: '/login'})
        } else {
          this.smsCode = ''
          this.time = 60
          this.$message.error(rtn.data.message)
        }
>>>>>>> remotes/origin/master
      })
    },
    setTime () {
      if (this.time === 1 || this.time === 0) {
<<<<<<< HEAD
=======
        console.log('可免费获取验证码' + this.time)
>>>>>>> remotes/origin/master
        this.time = 60
      } else {
        this.time--
        setTimeout(() => { this.setTime() }, 1000)
      }
<<<<<<< HEAD
=======
    },
    companyShow () {
      this.show = 0
    },
    personShow () {
      this.show = 1
    },
    agree () {
      this.isAgree = true
>>>>>>> remotes/origin/master
    }
  },
  watch: {
    time (newTime, oldTime) {
      if (newTime === 60) {
        this.newsTip = '获取短信验证码'
        this.flag = false
      } else {
        this.newsTip = newTime + '秒后可重新获取'
      }
    }
  },
<<<<<<< HEAD
  mounted () {
    if (this.$cookies.get('user-key')) { // 已登录
      this.$router.push({path: '/home'})
=======
  created () {
    let curRoute = this.$route.path
    this.isHome = (curRoute === '/home' ? '' : '/home')
  },
  mounted () {
    if (!this.isHome) {
      this.$refs.logoIsCursor.children[0].style.cursor = 'default'
>>>>>>> remotes/origin/master
    }
  }
}
</script>
<style scoped>
<<<<<<< HEAD
  input:focus {
    outline: none;
  }
  button:focus {
    outline: none;
  }
  button:hover {
    outline: none;
  }
  /* 注册页面*/
  #register{
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  #register> * {
    padding-left: calc(100vw - 100%);
  }
=======
  /* 注册页面*/
>>>>>>> remotes/origin/master
  .py-container{
    width: 1226px;
    margin: 0 auto;
  }
  .reg-top{
    background: #F4F4F4;
  }
<<<<<<< HEAD
  .reg-middle {
    flex-grow: 1;
=======
  .reg-bottom{
    background: #ececec;
>>>>>>> remotes/origin/master
  }
  .top{
    height:90px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .top img{
    width:110px;
    height:63px;
    margin-left:70px;
    margin-bottom:14px;
  }
  .top_left{
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .top .title{
    height:31px;
    font-size:32px;
<<<<<<< HEAD
=======
    font-family:SourceHanSansCN-Regular;
>>>>>>> remotes/origin/master
    font-weight:400;
    color:rgba(74,74,74,1);
    line-height:25px;
    margin-left:8px;
  }
<<<<<<< HEAD
  .title_com {
    color: #333;
  }
  .top .go {
    font-size:14px;
=======
  .top .go {
    font-size:14px;
    font-family:SourceHanSansCN-Regular;
>>>>>>> remotes/origin/master
    font-weight:400;
    color:rgba(53,53,53,1);
    line-height:20px;
    margin:60px 70px 0 0;
  }
  .top .go a{
    color: #28a3ef;
  }
  .middle{
    position: relative;
  }
<<<<<<< HEAD
  .password {
    position: relative;
  }
  .password span{
    position: absolute;
    top: 12px;
    right: 0;
    left: 100%;
    width: 100%;
    margin-left: 15px;
    color: rgb(130, 130, 130);
    font-size: 12px;
  }
/*中部内容区域*/
=======
  /*中部内容区域*/
>>>>>>> remotes/origin/master
  .middle-title{
    display: flex;
    justify-content: center;
    align-items: center;
    height: 79px;
  }
   .middle .fixed-height{
     height:35px;
     overflow: hidden;
<<<<<<< HEAD
     cursor: pointer;
=======
>>>>>>> remotes/origin/master
   }
  .middle .fixed-height .reduce-height{
    margin-bottom: -20px;
  }
  .middle .active{
    color: #FFD704 !important;
    border-bottom: 2px solid #FFD704;
  }
  .middle-title img{
    display: inline;
  }
  .middle  .title{
    width:200px;
    margin-top: 28px;
    font-size:20px;
<<<<<<< HEAD
=======
    font-family:SimHei;
>>>>>>> remotes/origin/master
    font-weight:400;
    color:rgba(53,53,53,1);
  }
  .middle .title-text{
    display: inline;
  }
  .middle-contaiber{
    width:1225px;
    margin :0 auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    flex-wrap: nowrap;
    margin-top: -7px;
  }
  .back{
    background:rgba(129,129,129,0.29);
  }
  .middle .explain{
    margin-top: 10px;
    height:15px;
    font-size:14px;
<<<<<<< HEAD
=======
    font-family:SimHei;
>>>>>>> remotes/origin/master
    font-weight:400;
    color:rgba(53,53,53,1);
    line-height:20px;
  }
  .middle-contaiber .agreement{
    width:763px;
    height:568px;
    background:rgba(255,255,255,1);
    margin: 30px 0 46px 0 ;
    padding-bottom: 40px;
  }
  .middle-contaiber .agreement .regagreement{
    margin:16px 0 0 22px;
    width:85px;
    height:18px;
    font-size:19px;
<<<<<<< HEAD
=======
    font-family:SourceHanSansCN-Regular;
>>>>>>> remotes/origin/master
    font-weight:400;
    color:rgba(53,53,53,1);
    line-height:23px;
  }
  .agreement hr {
    color: #E3E3E3;
    margin-top: 20px;
    opacity: 0.29;
  }
  .agreement .agreement-detail{
    margin:0 auto;
    width:721px;
    font-size:14px;
<<<<<<< HEAD
=======
    font-family:SimSun;
>>>>>>> remotes/origin/master
    font-weight:400;
    color:rgba(9,9,9,1);
    line-height:24px;
  }
  .agreement .agreement-detail a{
    font-size: 13px;
    color:#FF4606;
  }
  .agreement .agreement-detail p{
    margin-top: 10px;
    font-weight: lighter;
    text-align: left;
  }
  .agreement .agreement-detail span{
    font-weight: lighter;
  }
  .agreement .btn_agree{
    width:100px;
    height:30px;
    background:rgba(255,70,6,1);
    font-size:14px;
<<<<<<< HEAD
=======
    font-family:SimHei;
>>>>>>> remotes/origin/master
    font-weight:400;
    color:rgba(254,254,254,1);
    line-height:20px;margin-top: 10px;
  }
<<<<<<< HEAD
  .sui-btn{
    cursor: pointer;
  }
/*中部右边问题框*/
=======
  /*中部右边问题框*/
>>>>>>> remotes/origin/master
  .question{
    position: absolute;
    top:200px;
    right:0;
  }
  .question img{
    margin-left: 37px;
  }
  .question .know-more{
    width:123px;
    height:312px;
    border: 2px solid #F4AC00;
    border-radius:10px;
    position: relative;
  }
  .question .know-more P {
    margin:10px 0 5px 5px;
<<<<<<< HEAD
=======
    font-family: SimHei;
>>>>>>> remotes/origin/master
    font-weight: 400;
    color: rgba(53, 53, 53, 1);
    line-height: 20px;
  }
  .question .know-more ul>li{
    line-height: 20px;
    text-align: left;
  }
  .question .know-more ul>li a{
    font-size:12px;
<<<<<<< HEAD
=======
    font-family:SourceHanSansCN-Light;
>>>>>>> remotes/origin/master
    font-weight:300;
    color:rgba(58,58,58,1);
  }
  .question .know-more ul>li:nth-of-type(odd){
    background:rgba(255,233,125,0.37);
  }
  .question .clikeme img, .question  a{
    display: inline;
    margin: 0 10px  0 10px;
  }
  .question .clikeme{
    height: 34px;
    background: #F4AC00;
    font-size:16px;
<<<<<<< HEAD
=======
    font-family:SourceHanSansCN-Light;
>>>>>>> remotes/origin/master
    font-weight:300;
    color:rgba(255,255,255,1);
    line-height:32px;
    border-radius: 0 0 8px 8px;
    position: absolute;
    top:280px;
  }
  .question .text{
    margin: 2px 0 0 -28px;
  }
  .btn-reg {
    width: 100px;
    height:40px;
    margin:5px 0 0 100px;
  }
  .top h3{
    display: inline;
  }
  .info {
    width: 600px;
    margin: 40px auto;
    text-align: left;
  }
  .control-label {
    font-size: 14px;
    width: 105px;
    text-align: right;
    line-height: 42px;
  }
  .control-group{
    display: flex;
    margin: 15px 0;
  }
  .control-group .star{
    color: orangered;
    margin-right:7px;
  }

  .control-label:before{
    content: "*";
    color:#FF4606;
    margin-right:10px;
  }
<<<<<<< HEAD
  .checkbox {
    margin-left: 113px;
    flex-wrap: wrap;
    font-size: 14px;
    color: #A3A3A3;
    width: 268px;
    line-height: 22px;
  }
  .checkbox input {
    margin-right: 10px;
  }
 .controls .select{
   height: 40px;
   box-sizing: border-box;
   line-height: 38px;
   padding: 0 10px;
   font-size: 12px;
   width: 100px;
   margin-left: 10px;
   border-right:none;
   margin-right: 0;
   border: 1px solid rgb(153, 153, 153);
 }
  .controls {
    display: flex;
    align-items: center;
  }
  .controls .mobile{
    margin-left: -5px !important;
    width: 185px!important;
=======
 .el-checkbox a{
    color:#FF4606
  }
 .controls select{
   height:40px;
   width:140px;
   margin-left: 10px;
   border-right:none;
   margin-right: 0;
 }
  .control-group .el-checkbox{
    margin-left:110px;
  }
  .controls {
    display: flex;
  }
  .controls .mobile{
    margin-left: -5px !important;
    width:145px!important;
>>>>>>> remotes/origin/master
  }
  .controls .agree{
    color: orangered;
  }
  .controls >label{
    display: flex;
    align-items: center;
  }
  .sui-form input[type=text].input-xfat.input-xlarge,
  .sui-form input[type=password].input-xfat.input-xlarge {
    width: 280px;
    border-radius: 0;
    border: 1px solid #999;
    height: 38px;
    margin-left:10px;
  }
<<<<<<< HEAD
=======
  #submit {
    padding: 5px 80px;
    font-family: "微软雅黑";
    background-color: #c81523;
  }

  .zhuce {
    *width: 221px;
    float: right
  }
>>>>>>> remotes/origin/master
  .btn-danger {
    background-color: orangered;
    padding: 4px;
    border-radius: 0;
<<<<<<< HEAD
    font-size: 15px;
=======
    font-size: 16px;
    font-family: 微软雅黑;
>>>>>>> remotes/origin/master
    word-spacing: 4px;
    width: 90px;
    height: 30px ;
    line-height: 30px;
    text-align: center;
    color: white;
<<<<<<< HEAD
    border-radius: 4px;
  }
  .getPhoneCode{
    margin-left: 10px;
    padding: 0 20px;
    height: 30px;
    border-radius: 8px;
    background-color: #FF9800;
    color: white;
=======
  }
  .copyright ul li {
    list-style-type: none;
    display: inline-block;
    *display: inline;
    *zoom: 1;
    border-right: 1px solid #e4e4e4;
    padding: 0 20px;
    margin: 15px 0
  }

  .copyright ul li:last-child {
    border-right: 0
  }
  .h-logo {
    display: flex;
    flex-direction: column;
    justify-content: center;
    margin-top: 13px;
  }
  .h-logo span {
    font-size: 27px;
    color: #754C24;
    font-family: "Bahnschrift";
    text-align: left;
    margin-left: 8px;
    margin-bottom: 30px;
  }
  /*页脚*/
  footer{
    height:120px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin-top: 0;
  }
  footer p{
    font-size:15px;
    font-family:SimHei;
    font-weight:400;
    color:rgba(88,88,88,1);
    line-height:27px;
    margin-top: -30px;
  }
  .footer-list{
    display: flex;
    justify-content: center;
    align-items: center;
    margin-bottom: 30px;
  }
  .footer-list-item{
    margin-right:5px;
    font-size:14px;
    font-family:Bahnschrift;
    font-weight:400;
    color:rgba(109,109,109,1);
  }
  footer img{
    display: inline;
  }
  .getPhoneCode{
    margin-left: 10px;
>>>>>>> remotes/origin/master
  }
</style>
