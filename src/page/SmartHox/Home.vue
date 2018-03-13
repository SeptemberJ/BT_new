<template>
  <div class="SmartHox_home">
    <div class="BlockOuter">
      <h2>全系列物联网接入网关</h2>
      <p>Smart Hox 打通物联网多协议连接，让万物互联真正融入工作和生活的每个场景，
全面支持Wi-Fi、GPRS/3G/4G、ZigBee、RS485、Modbus、蓝牙、RF433、 2.4G 、Z-Wave、CAN等终端接入技术，广泛应用于各类物联网设备。</p>
      <mu-row class="marginTB_40">
        <mu-col width="25" tablet="25" desktop="15" class="TextCenter InlineBlock">
          <img src="static/img/Icon/SmartHox_home_icon1.png"/>
          <h5>统一接口</h5>
        </mu-col>
        <mu-col width="25" tablet="25" desktop="15" class="TextCenter InlineBlock">
          <img src="static/img/Icon/SmartHox_home_icon2.png"/>
          <h5>系统简洁</h5>
        </mu-col>
        <mu-col width="25" tablet="25" desktop="15" class="TextCenter InlineBlock">
          <img src="static/img/Icon/SmartHox_home_icon3.png"/>
          <h5>安全加密</h5>
        </mu-col>
        <mu-col width="25" tablet="25" desktop="50" class="TextCenter InlineBlock">
          <img  style="width:100% "  src="static/img/Icon/SmartHox_home_icon4.png"/>
        </mu-col>
      </mu-row>

    </div>

    <Row style="background-color: rgb(89,89,89);padding-top: 20px;padding-bottom: 20px;color: #fff;">
        <Col span="8" class="TextCenter">
          <img class="Small_icon" src="static/img/Icon/SmartHox_home_icon5.png"/>
          <span>万物互联一站式解决方案提供商</span>
        </Col>
        <Col span="8" class="TextCenter">
          <img class="Small_icon" src="static/img/Icon/SmartHox_home_icon5.png"/>
          <span>IoT 数据云平台服务</span>
        </Col>
        <Col span="8" class="TextCenter">
          <img class="Small_icon" src="static/img/Icon/SmartHox_home_icon5.png"/>
          <span>物联网接入网关-Hox One</span>
        </Col>
    </Row>

    <div class="BlockOuter">
      <h2>物联网一站式纵向服务</h2>
      <p>Smart Hox 作为物联网行业极具创新能力的IoT云平台，为企业提供进入物联网必需的设备接入、设备控制、数据分析、供应链资源一站式服务，助力企业智造转型，并为其在物联网时代打造新商业模式。</p>
      <Row  class="marginTB_40">
        <Col :xs="24" :sm="{ span: 6, offset: 0 }" :md="{ span: 6, offset: 0 }"  :lg="{ span: 5, offset: 1 }">
          <img src="static/img/Icon/SmartHox_home_icon6.png"/>
          <h5 class="Bold">构建设备</h5>
          <p class="TextLeft">物联网 (IoT)始于“物”（即设备）。构建您的设备（从添加传感器到创建智能设备），才能启动您的 IoT 解决方案。</p>
        </Col>
        <Col :xs="24" :sm="{ span: 5, offset: 1 }" :md="{ span: 5, offset: 1 }" :lg="{ span: 5, offset: 1 }">
          <img src="static/img/Icon/SmartHox_home_icon7.png"/>
          <h5 class="Bold">控制您的设备</h5>
          <p class="TextLeft">部署控制、监控和管理您的设备的 IoT 解决方案，从而允许您捕获实时数据。</p>
        </Col>
        <Col :xs="24" :sm="{ span: 5, offset: 1 }" :md="{ span: 5, offset: 1 }"  :lg="{ span: 5, offset: 1 }">
          <img src="static/img/Icon/SmartHox_home_icon8.png"/>
          <h5  class="Bold">分析数据</h5>
          <p class="TextLeft">利用您收集的数据并应用高级分析以揭示新业务见解。</p>
        </Col>
        <Col :xs="24" :sm="{ span: 5, offset: 1 }" :md="{ span: 5, offset: 1 }" :lg="{ span: 5, offset: 1 }">
          <img src="static/img/Icon/SmartHox_home_icon9.png"/>
          <h5  class="Bold">针对见解采取措施</h5>
          <p class="TextLeft">通过功能强大的应用程序将见解转变为行动，从而创造新的收入和业务机会。</p>
        </Col>
      </Row>
      
    </div>

    <div class="BlockOuter">
      <Row class="TextCenter">
          <Col v-for="(Tab,Idx) in TabMenu_Product" span="8" :class="{'Active':Cur_Product == Tab.name}">
            <span class="CursorPointer"  @click="ChangeTab_Product(Tab.name)">
              <Icon :size="24" color="#000" :type="Tab.icon"></Icon>
              <p>{{Tab.name}}</p>
            </span>
          </Col>
      </Row>
      <div v-if="Cur_Product === '智能家电'">
          <mobile-tear-sheet>
            <mu-list>
              <mu-sub-header></mu-sub-header>
              <mu-list-item>
                <mu-avatar src="static/img/Icon/SmartHox_home_icon10.png" slot="leftAvatar"/>
                <h5>智能家居设备</h5>
                <p>你不必再关心你的电器, 更多的是它们开始关心你;</p>
                <p>手机控制：下班了, 拿出手机用App打开空调制热, 打开家门便是温暖;</p>
                <p>语音控制：对Amazon echo、天猫机灵等智能设备, 说一句“制暖”, 空调便开始运行;</p>
              </mu-list-item>
              <mu-list-item>
                <mu-avatar src="static/img/Icon/SmartHox_home_icon11.png" slot="leftAvatar"/>
                <p>mart Hox智能云会记录并学习消费者的动作和习惯：温度过低空调会开启制热模式；当你离开家, 空调、取暖器等会停止工作。</p>
              </mu-list-item>
              <mu-sub-header>应用产品</mu-sub-header>
              <mu-list-item>
                <mu-grid-list class="gridlist-demo">
                  <mu-flexbox>
                    <mu-flexbox-item v-for="(Product,Idx) in TabProducts" class="flex-demo InlineBlock">
                      <img style="width: 100%;" :src="Product.img"/>
                    </mu-flexbox-item>
                  </mu-flexbox>
                  
                </mu-grid-list>
              </mu-list-item>
            </mu-list>
          </mobile-tear-sheet>
        </div>
    </div>

    <!-- <div class="BlockOuter">
      <h2 class="TextCenter">Smart Hox 可以为企业提供智能化服务</h2>
      <div class="marginTB_40">
        <mu-tabs :value="activeTab" @change="handleTabChange">
          <mu-tab value="智能家电" title="智能家电"><Icon :size="24" color="#000" type="ios-monitor"></Icon></mu-tab>
          <mu-tab value="智能照明"title="智能照明"><Icon :size="24" color="#000" type="ios-lightbulb"></Icon></mu-tab>
          <mu-tab value="智能工控" title="智能工控"><Icon :size="24" color="#000" type="ios-game-controller-b"></Icon></mu-tab>
        </mu-tabs>
        <div v-if="activeTab === '智能家电'">
          <mobile-tear-sheet>
            <mu-list>
              <mu-sub-header></mu-sub-header>
              <mu-list-item>
                <mu-avatar src="static/img/Icon/SmartHox_home_icon10.png" slot="leftAvatar"/>
                <h5>智能家居设备</h5>
                <p>你不必再关心你的电器, 更多的是它们开始关心你;</p>
                <p>手机控制：下班了, 拿出手机用App打开空调制热, 打开家门便是温暖;</p>
                <p>语音控制：对Amazon echo、天猫机灵等智能设备, 说一句“制暖”, 空调便开始运行;</p>
              </mu-list-item>
              <mu-list-item>
                <mu-avatar src="static/img/Icon/SmartHox_home_icon11.png" slot="leftAvatar"/>
                <p>mart Hox智能云会记录并学习消费者的动作和习惯：温度过低空调会开启制热模式；当你离开家, 空调、取暖器等会停止工作。</p>
              </mu-list-item>
              <mu-sub-header>应用产品</mu-sub-header>
              <mu-list-item>
                <mu-grid-list class="gridlist-demo">
                  <mu-flexbox>
                    <mu-flexbox-item v-for="(Product,Idx) in TabProducts" class="flex-demo InlineBlock">
                      <img style="width: 100%;" :src="Product.img"/>
                    </mu-flexbox-item>
                  </mu-flexbox>
                  
                </mu-grid-list>
              </mu-list-item>
            </mu-list>
          </mobile-tear-sheet>
        </div>
        <div v-if="activeTab === '智能照明'">
          <h2>Tab Two</h2>
          <p>
            这是第二个 tab
          </p>
        </div>
        <div v-if="activeTab === '智能工控'">
          <h2>Tab Three</h2>
          <p>
            这是第三个 tab
          </p>
        </div>
      </div>
    </div> -->


    <!-- <div class="BlockOuter">
      <h2 class="TextCenter">与Smart Hox 合作对接流程</h2>
      <div class="marginTB_40">
        <mu-tabs :value="activeTabTwo" @change="handleTabChangeTwo">
          <mu-tab value="需求洽谈" title="需求洽谈"><Icon :size="24" color="#000" type="chatboxes"></Icon></mu-tab>
          <mu-tab value="技术对接"title="技术对接"><Icon :size="24" color="#000" type="android-options"></Icon></mu-tab>
          <mu-tab value="产品研发" title="产品研发"><Icon :size="24" color="#000" type="cube"></Icon></mu-tab>
          <mu-tab value="联合调试" title="联合调试"><Icon :size="24" color="#000" type="ios-cog"></Icon></mu-tab>
          <mu-tab value="生产上线" title="生产上线"><Icon :size="24" color="#000" type="ios-world"></Icon></mu-tab>
        </mu-tabs>
        <div v-if="activeTabTwo === '需求洽谈'">
          <h2>Tab Two</h2>
          <p>
            这是第二个 tab
          </p>
        </div>
        <div v-if="activeTabTwo === '技术对接'">
          <h2>Tab Two</h2>
          <p>
            这是第二个 tab
          </p>
        </div>
        <div v-if="activeTabTwo === '产品研发'">
          <h2>Tab Three</h2>
          <p>
            这是第三个 tab
          </p>
        </div>
        <div v-if="activeTabTwo === '联合调试'">
          <h2>Tab Three</h2>
          <p>
            这是第三个 tab
          </p>
        </div>
        <div v-if="activeTabTwo === '生产上线'">
          <h2>Tab Three</h2>
          <p>
            这是第三个 tab
          </p>
        </div>
      </div>
    </div> -->

  </div>
</template>
<script>
  export default{
    data: function () {
      return {
        activeTab: '智能家电',
        activeTabTwo: '需求洽谈',
        Cur_Product:'智能家电',
        activeStep: 1,
        Cur:0,
        TabMenu_Product:[{'name':'智能家电','icon':'ios-monitor'},{'name':'智慧照明','icon':'ios-lightbulb'},{'name':'智慧工控','icon':'ios-game-controller-b'}],
        TabProducts:[
          {'img':'static/img/Icon/SmartHox_home_icon12.png'},
          {'img':'static/img/Icon/SmartHox_home_icon13.png'},
          {'img':'static/img/Icon/SmartHox_home_icon14.png'},
          {'img':'static/img/Icon/SmartHox_home_icon15.png'},
          {'img':'static/img/Icon/SmartHox_home_icon16.png'},
          {'img':'static/img/Icon/SmartHox_home_icon17.png'},
          {'img':'static/img/Icon/SmartHox_home_icon18.png'},
          {'img':'static/img/Icon/SmartHox_home_icon19.png'}
        ],
        TabProducts2:[
          {'img':'static/img/Icon/SmartHox_home_icon1.png'},
          {'img':'static/img/Icon/SmartHox_home_icon2.png'},
          {'img':'static/img/Icon/SmartHox_home_icon3.png'},
          {'img':'static/img/Icon/SmartHox_home_icon3.png'},
        ]
      }
    },
    mounted: function () {
      
    },
    created() {
      
    },
    computed: {
      
    },
    watch: {
      
    },
    components: {
      

    },
    methods: {
      handleTabChange (val) {
        this.activeTab = val
      },
      handleTabChangeTwo (val,idx) {
        this.activeTabTwo = val
        this.Cur = idx
      },
      handleNext () {
        this.activeStep++
      },
      ChangeTab_Product(Menu){
        this.Cur_Product = Menu
      }
    }
  }
</script>
<style lang="scss">
.SmartHox_home{
  .BlockOuter{
    padding: 20px 20px;
    .mu-tabs{
      background-color: #fff !important;
    }
    .mu-tab-text{
      color: #000;
    }
    .mu-icon{
      color: #000;
    }
  }
  .Small_icon{
    width: 20px;
    height: 20px;
  }
  

}
.Active{
    border-bottom:2px solid red !important;
  }
</style>
