<template>
    <div>
       <div id="myChart1" :style="{width: '400px', height: '175px'}"></div>
    </div>
</template>
<script>
    // 引入基本模板
    let echarts = require('echarts/lib/echarts');
    // 引入柱状图组件
    require('echarts/lib/chart/bar');
    // 引入提示框和title组件
    require('echarts/lib/component/tooltip');
    require('echarts/lib/component/title');
    export default {
        name: "DataCount",
        data: () => ({
            msg: 'Welcome to Your Vue.js App'
        }),
        mounted(){
            this.drawLine();
        },
        methods:{
            drawLine(){
                // 基于准备好的dom，初始化echarts实例
                let myChart = this.$echarts.init(document.getElementById('myChart1'));
                // 绘制图表
                myChart.setOption({
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
                });
            }
        }
    }
</script>