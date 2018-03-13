<template>
  <mu-appbar title="" value="carbon">
    <mu-icon-button slot="left" @click="toggle()">
      <Icon type="navicon-round"></Icon>
      <!-- <img  style="width: 20px;height: 20px;"  src="static/img/Icon/bars.png"> -->
    </mu-icon-button>
    
    <div class="desktop">
      <mu-flat-button color="white" label="Hox云平台登入" slot="right"/>
      <mu-flat-button color="white" label="热线电话:  400 880 2248" slot="right"/>
      <!-- <mu-text-field icon="search" class="appbar-search-field"  slot="right" hintText="Search"/> -->
    </div>
      <mu-icon-menu class="tablet" icon="more_vert" slot="right">
        <mu-menu-item title="Hox云平台登入"/>
        <mu-menu-item title="热线电话:  400 880 2248"/>
      </mu-icon-menu>
  </mu-appbar>
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
      }
     

    }
  }
</script>
<style lang="scss">
.left{
  display: inline-block;
  float: left;
}
.right{
  display: inline-block;
  float: right;
}
.desktop{
  float: right;
  display: none;
}
.tablet{
  display: inline-block;
}
@media (min-width: 769px) {
  .desktop{
    float: right;
    display: inline-block;
  }
  .tablet{
    display: none !important;
  }

}
.appbar-search-field{
  color: #FFF;
  margin-bottom: 0;
  &.focus-state {
    color: #FFF;
  }
  .mu-text-field-hint {
    color: fade(#FFF, 54%);
  }
  .mu-text-field-input {
    color: #FFF;
  }
  .mu-text-field-focus-line {
    background-color: #FFF;
  }
}

</style>
