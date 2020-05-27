<template>
    <div class="echarts">
        <div :id="id" style="width:300px;height:200px;"></div>
    </div>
</template>
 
<script>
import Echarts from 'echarts'
// 引入基本模板
let echarts = require('echarts/lib/echarts')
// 引入柱状图组件
require('echarts/lib/chart/bar')
// 引入折线图组件
require('echarts/lib/chart/line')
// 引入提示框和title组件
require('echarts/lib/component/tooltip')
require('echarts/lib/component/title')

export default {
    data() {
        return{
            myChart: {},
            heightpx2:'200'
        }
    },
    props: {
        echartObj: {
            type: Object,
            default: {}
        },
        id:{
            type:String,
            default:{}
        }
    },
    created() {
        this.$nextTick(()=> {
            this.loadEchart()
        })
    },
    mounted(){
        let _this = this;
        window.addEventListener("resize", () => {
        _this.myChart.resize();
})
    },
    methods: {
        loadEchart() {
            this.myChart = Echarts.init(document.getElementById(this.id));
            this.myChart.setOption(this.echartObj)
        }
    }
}
</script>
 
<style>
#echart {
    width: 50%;
    height: 300px;
}
</style>
