<template>
  <div class="com-app">
  <div class="layout">
    <div class="content">
      <div class="content-left">
        <!-- <div class="logo">
          Muse-UI
        </div> -->
        <mu-drawer :open="open" :docked="docked" @close="toggle()">
          <mu-list @itemClick="docked ? '' : toggle()">
            <mu-list-item disabled>
              <img style="width: 115px;" src="static/img/logo.png">
            </mu-list-item>
            <mu-list-item title="物联网场景应用"/>
            <mu-list-item title="产品与服务"/>
            <mu-list-item title="公司"/>
            <mu-list-item class="showToggle" @click.native="open = false" title="Close"/>
          </mu-list>
        </mu-drawer>
      </div>
      <div class="content-right">
        <div class="header">
          <mu-appbar title="">
            <mu-icon-button class="showToggle" icon="menu" slot="left" @click="toggle()"/>
            <mu-flat-button label="expand_more" slot="right"/>
            <mu-icon-button icon="expand_more" slot="right"/>
          </mu-appbar>
        </div>
        <div class="body">
          <mu-sub-header>阳光</mu-sub-header>
          <mu-content-block>
            散落在指尖的阳光，我试着轻轻抓住光影的踪迹，它却在眉宇间投下一片淡淡的阴影。调皮的阳光掀动了四月的心帘，温暖如约的歌声渐起。似乎在诉说着，我也可以在漆黑的角落里，找到阴影背后的阳光，找到阳光与阴影奏出和谐的旋律。我要用一颗敏感赤诚的心迎接每一缕滑过指尖的阳光！
          </mu-content-block>
        </div>
        <div class="footer">
          Muse-UI ©2017 Created by Muse-UI
        </div>
      </div>
    </div>
  </div>
    <!-- <div>
  <mu-raised-button label="toggle drawer" @click="toggle()"/>
  <mu-drawer right :open="open" @close="toggle()">
    <mu-appbar title="Muse UI"/>
    <mu-list>
      <mu-list-item title="Menu Item 1"/>
      <mu-list-item title="Menu Item 2"/>
      <mu-list-item title="Menu Item 3"/>
      <mu-list-item @click.native="open = false" title="Close"/>
    </mu-list>
  </mu-drawer>
</div> -->
    <!-- <transition>
      <router-view class="child-view"></router-view>
    </transition> -->
  </div>
</template>
<script>
//import TopBlock from 'components/PC/Common/TopBlock'
  export default{
    data: function () {
      return {
        activeTab: 'tab1',
      activeList: 'list1',
      docked: true
      }
    },
    mounted: function () {
      
    },
    created: function () {
      alert(this.$store.state.isMobile)
      
    },
    computed: {
      open: {
        get: function () {
          return this.$store.state.isMobile
        },
        set: function (newValue) {
          this.$store.state.isMobile = newValue
        }
      }
      
    },
    watch: {
      
    },
    components: {
      

    },
    methods: {
      toggle (flag) {
        this.$store.state.isMobile = !this.open
        this.docked = !flag
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
.layout{
}
.showToggle{
  display: block !important;
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
    width: 0%;
    float: left;
    background-color: rgb(225, 225, 225);
    margin-bottom: -4000px;
    padding-bottom: 4000px;
  }
  .content-right{
    border: 1px solid red;
    width: 100%;
    display: inline-block;
    float: right;
    background-color: rgb(236, 236, 236);
  }

@media (min-width: 769px) {
  .showToggle{
    display: none !important;
  }
  .content-left{
    width: 256px;
    float: left;
    background-color: rgb(225, 225, 225);
    margin-bottom: -4000px;
    padding-bottom: 4000px;
  }
  .content-right{
    border: 1px solid yellow;
    width: calc(100% - 256px);
    display: inline-block;
    float: right;
    background-color: rgb(236, 236, 236);
  }
}





.header{
  background-color: white;
  height: 40px;
}

.body{
  min-height: 500px;
  background-color: white;
  margin: 10px 20px;
}

.footer{
  padding: 10px 0;
  text-align: center;
}
</style>
