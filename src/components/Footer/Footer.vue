<template>
  <div class="foot">
    <mu-row gutter>
      <mu-col width="100" tablet="25" desktop="25">
        <h4>关于我们</h4>
        <p>公司简介</p>
        <p>Hox新闻</p>
      </mu-col>
      <mu-col width="100" tablet="50" desktop="50">
        <h4>联系方式</h4>
        <p>研发总部：江苏省常熟高新技术产业开发区汇金三路东东南汇1号楼</p>
        <p>上海公司：上海市普陀区中江路879号天地软件园12号楼4F</p>
        <p>杭州公司：杭州西湖区余杭塘路866号浙大紫金港东五教学区光及电磁波研究中心G106</p>
        <p>广州公司：广州大学城华南师范大学理五栋 (大学城西五路)</p>
        <p>电话热线：+86 400 880 4428</p>
        <p>Mail：servcie@hoxsmart.com</p>
      </mu-col>
      <mu-col width="100" tablet="25" desktop="25">
        <h4>关注我们</h4>
        <!-- <mu-grid> -->
          <img src="static/img/BT_weixin.png"/>
        <!-- </mu-grid> -->
      </mu-col>
    </mu-row>
  </div>
</template>
<script>

  export default{
    data: function () {
      return {
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
      

    },
    methods: {
     

    }
  }
</script>
<style lang="scss">
.foot{
  padding: 40px 20px;
  color: #fff;
  text-align: left;
  background-color: rgb(89,89,89);
  p{
    font-size: 12px;
  }
}
</style>
