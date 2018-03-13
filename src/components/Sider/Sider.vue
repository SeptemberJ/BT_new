<template>
  <mu-drawer :open="open" :docked="docked" @close="toggle()">
    <mu-list @itemClick="docked ? '' : toggle()">
      <mu-list-item disabled  class="TextCenter">
        <img style="width: 115px;" src="static/img/logo.png">
      </mu-list-item>
      <mu-list-item class="TextCenter"><mu-icon value="cloud_download" color="orange"/><span class="DisplayBlock">物联网场景应用</span></mu-list-item>
      <mu-list-item class="TextCenter"><mu-icon value="cloud_download" color="orange"/><span class="DisplayBlock">产品与服务</span></mu-list-item>
      <mu-list-item class="TextCenter"><mu-icon value="cloud_download" color="orange"/><span class="DisplayBlock">公司</span></mu-list-item>
      <mu-list-item v-if="docked" @click.native="open = false" title="Close"/>
    </mu-list>
  </mu-drawer>
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

</style>
