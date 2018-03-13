<template>
  <div class="com-app">
  <div class="layout">
    <div class="content">
      <div v-bind:class="{ 'content-left': open}">
      <Sider/>
      </div>
      <div :class="{'content-right':open}">
        <div class="header">
          <Header/>
        </div>
        <div class="body">
          <Home/>
        </div>
        <div class="footer">
          <Footer/>
        </div>
      </div>
    </div>
  </div>
    <!-- <transition>
      <router-view class="child-view"></router-view>
    </transition> -->
  </div>
</template>
<script>
import Header from 'components/Header/Header'
import Sider from 'components/Sider/Sider'
import Footer from 'components/Footer/Footer'
import Home from 'page/SmartHox/Home'
  export default{
    data: function () {
      return {
        activeTab: 'tab1',
        activeList: 'list1',
        // open:true,
        // docked: true
      }
    },
    mounted: function () {
      
    },
    created() {
      
    },
    computed: {
      open:{
          get: function () {
            return this.$store.state.open
          },
          set: function (newValue) {
            this.$store.state.open = newValue
          }
      },
      docked:{
          get: function () {
            return this.$store.state.docked
          },
          set: function (newValue) {
            this.$store.state.docked = newValue
          }
      },
      
    },
    watch: {
      
    },
    components: {
      Header,
      Sider,
      Footer,
      Home
    },
    methods: {
      toggle (flag) {
        this.$store.state.open = !this.$store.state.open
        this.$store.state.docked = !flag
      },
      handleTabChange (val) {
        this.activeTab = val
      },
      handleListChange (val) {
        this.activeList = val
      }
     

    }
  }
</script>
<style lang="scss">
$width: 150px;


.layout{
}

.logo{
  font-size: 24px;
  color: white;
  text-align: center;
  color: #7e57c2;
  padding: 10px 20px;
}

.tab{
  margin: 0 auto;
  width: 400px;
}

.content{
  overflow: hidden;
}

.content-left{
  width: 0px;
  float: left;
  background-color: rgb(225, 225, 225);
  margin-bottom: -4000px;
  padding-bottom: 4000px;
}

.content-right{
  border: 0px solid blue;
  width: 100%;
  display: inline-block;
  float: right;
  background-color: rgb(236, 236, 236);
}
@media (min-width: 769px) {
  .content-left{
    width: $width;
    float: left;
    background-color: rgb(225, 225, 225);
    margin-bottom: -4000px;
    padding-bottom: 4000px;
  }

  .content-right{
    border: 0px solid red;
    width: calc(100% - #{$width});
    display: inline-block;
    float: right;
    background-color: rgb(236, 236, 236);
  }
}
.content-left-close{
  width: 0px;
  float: left;
  background-color: rgb(225, 225, 225);
  margin-bottom: -4000px;
  padding-bottom: 4000px;
}

.content-right-close{
  width: 100%;
  display: inline-block;
  float: right;
  background-color: rgb(236, 236, 236);
}

.header{
  background-color: white;
  height: 40px;
}

.body{
  min-height: 500px;
  background-color: white;
  margin: 40px 5px;
}

.footer{
  padding: 0;
  text-align: center;
}
</style>
