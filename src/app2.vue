<template>
  <div class="com-app">
     <div class="layout">
        <div class="content">
          <div v-bind:class="{ 'content_left': open}">
          <h2 v-if="open">侧边<h5 @click="toggle()">头部</h5></h2>
          </div>
          <div :class="{'content_right':open}">
            <div class="header">
            <Button type="primary" @click="toggle()">头部</Button>
            </div>
            <div class="body">
              <Row>
          <Col span="8">
            <img class="Small_icon" src="static/img/Icon/SmartHox_home_icon5.png"/>
            
          </Col>
          <Col span="8">
            <img class="Small_icon" src="static/img/Icon/SmartHox_home_icon5.png"/>
            
          </Col>
          <Col span="8">
            <img class="Small_icon" src="static/img/Icon/SmartHox_home_icon5.png"/>
            
          </Col>
      </Row>
            </div>
            <div class="footer">
              底部
            </div>
          </div>
        </div>
      </div>
  </div>
</template>
<script>
//import TopBlock from 'components/PC/Common/TopBlock'
  export default{
    data: function () {
      return {
        open:true
      }
    },
    mounted: function () {
      
    },
    created: function () {
      
    },
    computed: {
      
    },
    watch: {
      
    },
    components: {
      

    },
    methods: {
      toggle (flag) {
        this.open = !this.open
      },
     

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

.content_left{
  width: $width;
  height: 100%;
  background-color: #fff;
  position: absolute;
  top: 0px;
  left: 0px;
  z-index: 999999;
}

.content_right{
  border: 1px solid blue;
  width: 100%;
  display: inline-block;
  float: right;
  background-color: rgb(236, 236, 236);
}
@media (min-width: 769px) {
  .content_left{
    background-color: #fff;
    width: $width;
    float: left;
  }

  .content_right{
    border: 1px solid red;
    width: calc(100% - #{$width});
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
  margin: 40px 0px;
}

.footer{
  padding: 0;
  text-align: center;
}
</style>
