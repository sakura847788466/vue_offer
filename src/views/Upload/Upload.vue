<template>
  <div class="home">
     <div class="Box">
         <div class="left">
           <div class="header">
            <ul class="el-menu">
                  <li class="logo">
                    <img class="login-img"
                        src="../../assets/logo.png"
                        alt="">
                  </li>
                    <li class="glz">
                      <a title="应用管理">
                        <span>Dashboard</span>
                      </a>
                    </li>
                    <li class="print">
                      <a title="接口调试"
                        >
                        <span>Services</span>
                      </a>
                    </li>
                    <li class="text">
                      <a title="文档中心"
                        
                        style="text-decoration: none"
                        target="_blank">
                        <span>History</span>
                      </a>
                    </li>
                    <li class="text">
                      <a title="文档中心"
                        
                        style="text-decoration: none"
                        target="_blank">
                        <span>Actions</span>
                      </a>
                    </li>
                 <el-input
                    placeholder="请选择日期"
                    v-model="input3" style="width:300px">
                    <i slot="suffix" class="el-input__icon el-icon-search"></i>
                  </el-input>
            </ul>
           </div>
           <div class="main_box">
              <div class="main">
                 <div class="main_top">
                   <el-card class="box-card" :body-style="{ display: 'flex' }" >
                    <div slot="header" class="clearfix">
                      <span>Card</span>
                      <el-button style="float: right; padding: 3px 0" type="text">Tangname</el-button>
                    </div>
                       <div class="main_con_box "></div>
                       <div class="main_con_box"></div>
                       <div class="main_con_box"></div>
                  </el-card>
                 </div>
                 <div class="main_buttom flex">
                    <div class="main_left">
                         <el-card class="box-card" :body-style="{ display: 'flex',flexDirection:'column' }" >
                          <div slot="header" class="clearfix">
                            <span>Main Service</span>
                            <el-button style="float: right; padding: 3px 0" type="text">View all</el-button>
                          </div>
                            <div style="width:100%;display:flex;">
                                <div class="main_con_box_s ">
                                    <i class="el-icon-s-tools icon"></i>
                                     <span>Transactions</span>
                                </div>
                                <div class="main_con_box_s">
                                  <i class="el-icon-s-tools icon"></i>
                                     <span>Transactions</span>
                                </div>
                            </div>
                           <div style="width:100%;display:flex;">
                               <div class="main_con_box_s ">
                                 <i class="el-icon-s-tools icon"></i>
                                     <span>Transactions</span>
                               </div>
                                <div class="main_con_box_s">
                                  <i class="el-icon-s-tools icon"></i>
                                     <span>Transactions</span>
                                </div>
                            </div>
                             <div style="width:100%;display:flex;">
                               <div class="main_con_box_s ">
                                 <i class="el-icon-s-tools icon"></i>
                                     <span>Transactions</span>
                               </div>
                                <div class="main_con_box_s">
                                  <i class="el-icon-s-tools icon"></i>
                                     <span>Transactions</span>
                                </div>
                            </div>
                        </el-card>
                    </div>
                    <div class="main_right">
                       <el-card class="box-card" :body-style="{ display: 'flex' }" >
                          <div slot="header" class="clearfix">
                            <span>Current</span>
                            <el-button style="float: right; padding: 3px 0" type="text">View all</el-button>
                          </div>
                           <div style="flex:1;">
                              <div class="right_item ">
                                <span>15078097896</span>
                                <span>...............................................................................</span>
                                <span>$20,1234</span>
                              </div>
                              <div class="right_item ">
                                <span>15078097896</span>
                                <span>...............................................................................</span>
                                <span>$20,1234</span>
                              </div>
                              <div class="right_item ">
                                <span>15078097896</span>
                                <span>...............................................................................</span>
                                <span>$20,1234</span>
                              </div>
                           </div>
                        </el-card>
                        <el-card class="box-card" :body-style="{ display: 'flex' }" >
                          <div slot="header" class="clearfix">
                            <span>Echarts</span>
                            <el-button style="float: right; padding: 3px 0" type="text">View all</el-button>
                          </div>
                           <div>
                              <LineE/>
                           </div>
                        </el-card>
                    </div>
                 </div>
              </div>
           </div>
         </div>
        <div class="right">
          <div class="title flex">
            <div>
              <i class="el-icon-bell icon"></i>
            </div>
            <div>
              <span>张珊</span>
              <el-avatar size="large" :src="circleUrl"></el-avatar>
            </div>
          </div>
          <div class="container">
            <Echarts :echartObj="echartObj"/>
            <div class="list_title flex">
              <div>Transactions</div>
              <div>
               <span>Today</span>
              <i class=" el-icon-arrow-down icon"></i>
              </div>
            </div>
            <div class="box_list">
               <div class="item flex">
                   <div>
                     <img :src="url" alt="" style="display:inline-block;height:40px;width:40px;">
                   </div>
                  <div>Dribbble Pro Plan</div>
                  <span>-$100</span>
               </div>
                <div class="item flex">
                   <div>
                     <img :src="url" alt="" style="display:inline-block;height:40px;width:40px;">
                   </div>
                  <div>Dribbble Pro Plan</div>
                  <span>-$100</span>
               </div>
                <div class="item flex">
                   <div>
                     <img :src="url" alt="" style="display:inline-block;height:40px;width:40px;">
                   </div>
                  <div>Dribbble Pro Plan</div>
                  <span>-$100</span>
               </div>
            </div>
            <div class="btn flex_l">
              <el-button type="danger" round style="width:92%;" >Transfer Money<i class="el-icon-arrow-right el-icon--right"></i></el-button>
            </div>
            <div class="ciecle">
              <div class="ciecle_box"></div>
            </div>
          </div>
        </div>
     </div>
  </div>
</template>

<script>
import Echarts from '../../components/Echerts/Echarts'
import LineE from '../../components/Line/Line'
export default {
  name: 'Home',
  data(){
   return {
      circleUrl: "https://cube.elemecdn.com/3/7c/3ea6beec64369c2642b92c6726f1epng.png",
      url: 'https://fuss10.elemecdn.com/e/5d/4a731a90594a4af544c0c25941171jpeg.jpeg',
      input3:'',
      id:'',
      echartObj:{
          tooltip: {
                trigger: 'item',
                formatter: "{a} <br/>{b}: {c} ({d}%)"
            },
            legend: {
                selectedMode: false,
                orient: 'horizontal',
                x: 'center',
                y: 'top',
                top: '70%',
                // 图标大小,宽和高
                itemWidth: 20,
                itemHeight: 20,
                // 显示内容
                data: ['1','2','3','4'],
            },   
             grid: {
                top:'3%',
                left: "3%",
                right: "4%",
                bottom: "3%",
                containLabel: true
            },
            series: [          
                {
                name:'',
                type:'pie',
                radius: ['45%', '50%'],
                center: ['50%', '30%'],
                avoidLabelOverlap: false,
                label: {
                    normal: {
                        show: true,
                        position: 'center',
                        formatter:function(){
                            return '$5,349'
                        },
                        textStyle: {
                            fontSize: '23',
                            fontWeight: 'bold',
                            color:'#000'
                        }
                    },
                    emphasis: {
                        show: true,
                        textStyle: {
                            fontSize: '23',
                            fontWeight: 'bold'
                        }
                    }
                },
                labelLine: {
                    normal: {
                        show: false
                    }
                },
                data: ['1','2','3','4'],
                // color: ['#4B96E8','#FAB737','#EA4545', '#DDDDDD'],
                }
            ]
      },
      options:{
        title: {
                        text: '',
                        subtext: ''
                    },
                    tooltip: {
                        trigger: 'axis'
                    },
                    legend: {
                        data:['最高']
                    },
                    toolbox: {
                        show: true,
                        feature: {
                            dataZoom: {
                                yAxisIndex: 'none'
                            },
                            dataView: {readOnly: false},
                            magicType: {type: ['line']},
                            restore: {},
                            saveAsImage: {}
                        }
                    },
                    xAxis:  {
                        type: 'category',
                        boundaryGap: false,
                        data: ['2019-02-25','2019-03-04','2019-03-18','2019-03-26']
                    },
                    yAxis: {
                        type: 'value',
                        axisLabel: {
                            formatter: '{value}'
                        }
                    },
                    series: [
                        {
                            name:'最高',
                            type:'line',
                            data:[11, 11, 15, 13, 12, 13, 10],
                            markPoint: {
                                data: [
                                    {type: 'max', name: '最大值'},
                                    {type: 'min', name: '最小值'}
                                ]
                            },
                            markLine: {
                                data: [
                                    {type: 'average', name: '平均值'}
                                ]
                            }
                        },
                    ]
      }
   }
  },
  methods:{
    
  },
  components: {
    Echarts,LineE
  }
}
</script>
<style >
.el-input__inner{
     border-radius: 23px;
   }
</style>
<style  scoped>
   
   .home{
     width: 100%;
     /* height: 900px; */

   }
    .left{
      flex:4;
      height: 100%;
      background-color: aqua;
      position: relative;
  }
  .right{
    flex:1;
    height: 100%;
    background-color: beige;
    margin-left:15px;
    border-radius: 20px;
    padding: 10px;
  }
  /* 弹性盒子 */
  .flex{
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .flex_l{
    display: flex;
    justify-content: space-between;
    align-items: center;
    justify-content: center;
  }
  /* 垂直居中 */
   .Center{
     position:absolute;top:50%;left:50%;
     transform: translate(-50%,-50%);
   }
  .Box{
      width: 90%;
      height: 90%;
      border-radius: 20px;
      background-color: #FAFAFA;
      display: flex;
      position:absolute;
      top:50%;
      left:50%;
      transform: translate(-50%,-50%);

  }
  .title{
    margin-top:10px;
  }
  .title div:nth-child(2){
        display: flex;
        align-items: center;
  }
  .title div:nth-child(2) span,.list_title div:nth-child(2) span{
    margin-right: 5px;
  }
  .list_title{
    padding:5px 10px;
  }
  .box_list .item{
    padding:5px 10px;
    margin-bottom: 10px;
  }
  .box_list .item div:nth-child(2){
    font-weight: bold;
  }
  .btn,.ciecle{
    height:100px;
    width: 100%;
  }
  .ciecle{
    position: relative;
  }
  .ciecle_box{
    height:40px;
    width: 40px;
    background-color: aqua;
    border-radius: 50%;
    position:absolute;
    top:16%;
    right:3%;
  }
  /* 头部 */
  .header {
    display: flex;
    flex-direction: row;
    height: 186px;
    align-items: center;
    justify-content: center;
  }
.logo {

}

.logo > .login-img {
  width: 68px;
  height: 68px;
}

.logo > .logo-text {
  margin-top: 26px;
  font-size: 20px;
  /*font-weight: bold;*/
  color: rgba(255, 255, 255, 1);
}

.el-menu {
  display: flex;
  flex-direction: row;
  align-items: center;
  margin-top: 40px;
  height: 100px;
  width: 90%;
  background-color: #ffffff;
  padding: 10px;
}


.el-menu li:nth-child(1) {
  margin-left: 55px;
}

.el-menu > li {
  width: 120px;
}

.el-menu > li > a {
  display: block;
  width: 120px;
  height: 100px;
  line-height: 100px;
  font-size: 16px;
  text-align: center;
  color: #666;
  transition: 0.3s;
  cursor: pointer;
}

.el-menu > li > a:hover {
  color: #0095ff;
  background-color: #edf8ff;
}

a > span {
  padding-bottom: 12px;
}

a:hover span {
  border-bottom: 2px solid #0095ff;
}
/* main */
.main_box{
  display: flex;
  justify-content: center;
}
.main{
  width: 90%;
  height: 678px;
  background-color: #fff;
  border-radius: 20px;
}

/* card */
.main_con_box{
  height:150px;
  flex:1;
  background-color: brown;
  margin: 5px;
  border-radius: 10px;
}
.main_con_box_s{
  height:100px;
  flex:1;
  background-color: brown;
  margin: 5px;
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.main_con_box_s i{
  font-size: 31px;
}
.main_con_box_s span{
  font-size: 12px;
  margin-top:5px;
}
.main_left{
  flex:1;
  background-color: burlywood;
  height:406px;
}
.main_right{
  flex:3;
  background-color: chartreuse;
  height:406px;
  margin-left: 10px;

}
.right_item{
  display: flex;
  justify-content: space-around;
  align-items: center;
}
.right_item span{
  display:inline-block;
  height: 20px;
}
.right_item span:nth-child(1),.right_item span:nth-child(3){
  flex:1;
}
.right_item span:nth-child(2){
  flex:3;
  text-align: center;
}
.right_item span:nth-child(3){
  text-align: right;
}
</style>