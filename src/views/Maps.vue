<template>
<div>
<header class="header">
        <div class="header_bg header_pose"></div>
        <div class="header_center header_pose">
            <h2><strong>停车场数据监控中心</strong></h2>
        </div>
        <div id="pay_btn">
            <div class="header_bg2 header_pose">
                <img id="down_img" src="../assets/images/down_push.png">
                <img id="up_img" src="../assets/images/up_push.png">
            </div>
            <div class="header_center2 header_pose">
                <h5><strong>今日收款总额</strong></h5>
            </div>
        </div>
        <div id="pay_dialog">
            <div class="header_dialog_bg header_pose"></div>
            <div class="header_dialog header_pose">
                <div class="header_number"><span>000.000.000.000.00</span></div>
                <div class="header_flex">
                    <div>
                        <span>昨日收款总额：</span>
                        <span>0000.00</span>
                    </div>
                    <div>
                        <span>单笔临停平均收费：</span>
                        <span>0000.00</span>
                    </div>
                    <div>
                        <span>环比增长：</span>
                        <span>00.00%</span>
                    </div>
                </div>
            </div>
        </div>

    </header>
    <!--内容部分-->
    <div class="container left">
        <!--统计分析图-->
        <div class="div_center">
            <div class="div_any_child div_height">
                <div id="mapChart" style="width:100%;height:100%;display: inline-block;"></div>
            </div>
        </div>
        <div class="div_left div_any00"></div>
        <div class="div_left div_any01">
            <div class="div_any_child" style="height: 160px;">
                <div class="div_any_title"><img src="../assets/images/title_1.png">营收趋势（最近15天）</div>
                <p id="lineChart1" class="p_chart" style="height: 144px;"></p>
            </div>
            <div class="div_any_child" style="border-bottom: none; height: 260px; z-index: 2;">
                <div class="div_any_title"><img src="../assets/images/title_16.png">实际收费情况</div>
                <div class="table_p">
                    <table>
                        <thead>
                            <tr>
                                <th>车场</th>
                                <th>车牌</th>
                                <th>收费</th>
                            </tr>
                        </thead>
                        <tbody id="tbody_pay">
                            <tr>
                                <td>1</td>
                                <td>浙F 222333</td>
                                <td>￥30.00</td>
                            </tr>
                            <tr>
                                <td>2</td>
                                <td>浙F 222333</td>
                                <td>￥300.00</td>
                            </tr>
                            <tr>
                                <td>3</td>
                                <td>浙F 222333%</td>
                                <td>￥30.00</td>
                            </tr>
                            <tr>
                                <td>4</td>
                                <td>浙F 222333</td>
                                <td>￥30.00</td>
                            </tr>
                            <tr>
                                <td>5</td>
                                <td>浙F 222333</td>
                                <td>￥30.00</td>
                            </tr>
                            <tr>
                                <td>6</td>
                                <td>浙F 222333</td>
                                <td>￥30.00</td>
                            </tr>
                            <tr>
                                <td>7</td>
                                <td>浙F 222333</td>
                                <td>￥30.00</td>
                            </tr>
                            <tr>
                                <td>8</td>
                                <td>浙F 222333</td>
                                <td>￥30.00</td>
                            </tr>
                            <tr>
                                <td>9</td>
                                <td>浙F 222333</td>
                                <td>￥30.00</td>
                            </tr>
                        </tbody>
                    </table>
                    <table>
                        <thead>
                            <tr>
                                <th>车场</th>
                                <th>排行</th>
                            </tr>
                        </thead>
                        <tbody id="tbody_rank">
                            <tr>
                                <td>浙F 222333</td>
                                <td>1</td>
                            </tr>
                            <tr>
                                <td>浙F 222333</td>
                                <td>2</td>
                            </tr>
                            <tr>
                                <td>浙F 222333%</td>
                                <td>3</td>
                            </tr>
                            <tr>
                                <td>浙F 222333</td>
                                <td>4</td>
                            </tr>
                            <tr>
                                <td>浙F 222333</td>
                                <td>5</td>
                            </tr>
                            <tr>
                                <td>浙F 222333</td>
                                <td>6</td>
                            </tr>
                            <tr>
                                <td>浙F 222333</td>
                                <td>7</td>
                            </tr>
                            <tr>
                                <td>浙F 222333</td>
                                <td>8</td>
                            </tr>
                            <tr>
                                <td>浙F 222333</td>
                                <td>9</td>
                            </tr>
                        </tbody>
                    </table>
                </div>
            </div>
            <div class="div_any_child" style="height: 200px; margin-top: -20px; border-top: none;">
                <div class="div_any_title" style="top: 25px;"><img src="../assets/images/title_1.png">支付分析</div>
                <p id="pieChart1" class="p_chart" style="height: 188px; left: 0px; width: 45%; position: absolute;"></p>
                <p id="pieChart2" class="p_chart" style="height: 188px; right: 0px; width: 45%; position: absolute;">
                </p>
            </div>

            <div class="div_any_child">
                <div class="div_any_title"><img src="../assets/images/title_2.png">各大区收费统计</div>
                <p id="histogramChart" class="p_chart"></p>
            </div>
        </div>

        <div class="div_right div_any00"></div>
        <div class="div_right div_any02">
            <div class="div_any_child">
                <div class="div_any_title"><img src="../assets/images/title_3.png">今日总车流量</div>
                <div class="div_number"><span>00.000</span><span>辆</span></div>
                <div class="div_flex">
                    <div>
                        <p>电子支付数（车数）：</p>
                        <p></p>
                        <p style="margin-top: 50px;">车流量（车数）：</p>
                        <p></p>
                    </div>
                    <div>
                        <p>月累计：</p>
                        <p>日新增：</p>
                        <p style="margin-top: 50px;">月累计：</p>
                        <p>日新增：</p>
                    </div>
                </div>
                <!-- <p id="lineChart" class="p_chart"></p> -->
            </div>
            <div class="div_any_child">
                <div class="div_any_title"><img src="../assets/images/title_3.png">车流量趋势(最近15天)</div>
                <p id="lineChart" class="p_chart"></p>
            </div>
            <div class="div_any_child">
                <div class="div_any_title"><img src="../assets/images/title_4.png">今日进出场车型分析</div>
                <p id="lineChart2" class="p_chart"></p>
            </div>
        </div>
    </div>
</div>
</template>
<script>
import 'echarts/extension/bmap/bmap'
export default {
name: 'Maps',
methods: {
    myMap() {
        const mapChart = this.$echarts.init(document.getElementById('mapChart'));
        mapChart.setOption({
        bmap: {
            center: [120.680229, 30.511541],
            zoom: 25,
            roam: true,
        },
        title: { //  标题样式
            x: "center",
            subtextStyle: {
                color: '#00F6FF',
                fontSize: 15,
                textShadowColor: "#64FAFF",
                textShadowBlur: 5,
                textShadowOffsetX: 0,
                textShadowOffsetY: 0,
            },
        },
        tooltip: {
            trigger: 'item',
            formatter: function (params) {
                return params.value[2]
            }
        },
        series: [{
            type: 'scatter',
            coordinateSystem: 'bmap',
            symbol: "pin", // 标识点的样式
            symbolSize: "25", // 标识点的大小
            color: "#F62157", // 标识点的颜色
            // data:dataAll.parking_map
            data:[
                [120.680229, 30.511520, '第一车场'],
                [120.680345, 30.511145, '第二车场'],
                [120.680427, 30.511543, '第三车场'],
                [120.680526, 30.511683, '第四车场'],
                [120.680625, 30.511356, '第五车场'],
                [120.680724, 30.511790, '第六车场'],
            ]
        }],
    });
    
    //营收趋势（最近15天）
    const lineChart1 = this.$echarts.init(document.getElementById('lineChart1'));
    lineChart1.setOption({
        // title: {
        //     text: '营收趋势（最近15天）',
        //     textStyle: {
        //         fontSize: 16,
        //         color: '#ff7f50'
        //     },
        // },
        color: ["#ff7f50"],
        grid: {
            left: '15%',
            right: '5%',
            bottom: '15%',
            top: '15%',
        },
        tooltip: {
            trigger: 'item',
            formatter: "{a}<br/>{b}<br/>{c}元"
        },

        calculable: true,
        yAxis: [{
            type: 'value',
            axisLine: {
                lineStyle: {
                    color: '#ff7f50'
                },
            },
            splitLine: {
                "show": false
            },
            axisLabel: {
                textStyle: {
                    color: '#fff'
                },
                formatter: function (value) {
                    return value + ""
                },
            },
        }],
        xAxis: [{
            type: 'category',
            data: ['1', '2', '1', '2', '1', '2', '1', '2', '1', '2'],
            boundaryGap: false,
            axisLine: {
                lineStyle: {
                    color: '#ff7f50'
                },
            },
            splitLine: {
                "show": false
            },
            axisLabel: {
                // interval:0,
                // rotate:40,
                textStyle: {
                    color: '#fff'
                },
                formatter: function (value) {
                    return value + ""
                },
            },
        }],
        series: [{
            name: '营收金额',
            type: 'line',
            smooth: true,
            itemStyle: {
                normal: {
                    areaStyle: {
                        type: 'default'
                    }
                }
            },
            data: [120, 132, 101, 134, 90, 230, 210, 120, 132, 101, 134, 90]
        }, ]

    });
    // 支付分析
    const pieChart1 = this.$echarts.init(document.getElementById('pieChart1'));
    pieChart1.setOption({

        color: ["#87cefa", "#ff7f50", "#32cd32", "#da70d6", ],

        legend: {
            y: '150',
            x: 'center',
            type: 'scroll',
            textStyle: {
                color: '#ffffff',
                fontSize: '8',
            },
            bottom: 0,
            data: ['第一车场', '第二车场', '第三车场', '第四车场', ],
        },
        tooltip: {
            trigger: 'item',
            formatter: "{a}<br/>{b}<br/>{c}元 ({d}%)"
        },
        calculable: false,
        series: [{
            name: '支付占比',
            type: 'pie',
            radius: ['40%', '70%'],
            center: ['50%', '55%'],
            avoidLabelOverlap: false,
            itemStyle: {
                normal: {
                    label: {
                        show: false,
                        position: 'center'
                    },
                    labelLine: {
                        show: false
                    }
                },
                emphasis: {
                    label: {
                        show: true,
                        position: 'center',
                        textStyle: {
                            fontSize: '10',
                            fontWeight: 'bold'
                        }
                    }
                }
            },
            data: [{
                    value: 335,
                    name: '第一车场'
                },
                {
                    value: 65,
                    name: '第二车场'
                },
                {
                    value: 100,
                    name: '第三车场'
                },
                {
                    value: 500,
                    name: '第四车场'
                }

            ]
        }]
    });
    const pieChart2 = this.$echarts.init(document.getElementById('pieChart2'));
    pieChart2.setOption({

        color: ["#87cefa", "#ff7f50", "#32cd32", "#da70d6", ],

        legend: {
            y: '150',
            x: 'center',
            type: 'scroll',
            textStyle: {
                color: '#ffffff',
                fontSize: '8',
            },

            bottom: 0,

            data: ['支付宝', '微信', '现金', '银联卡', ],
        },
        tooltip: {
            trigger: 'item',
            formatter: "{a}<br/>{b}<br/>{c}元 ({d}%)"
        },
        calculable: false,
        series: [{
            name: '支付占比',
            type: 'pie',
            radius: ['40%', '70%'],
            center: ['50%', '55%'],
            avoidLabelOverlap: false,
            itemStyle: {
                normal: {
                    label: {
                        show: false,
                        position: 'center'
                    },
                    labelLine: {
                        show: false
                    }
                },
                emphasis: {
                    label: {
                        show: true,
                        position: 'center',
                        textStyle: {
                            fontSize: '10',
                            fontWeight: 'bold'
                        }
                    }
                }
            },
            data: [{
                    value: 335,
                    name: '支付宝'
                },
                {
                    value: 310,
                    name: '微信'
                },
                {
                    value: 234,
                    name: '现金'
                },
                {
                    value: 135,
                    name: '银联卡'
                }

            ]
        }]
    });
    // 各大区收费统计
    const histogramChart = this.$echarts.init(document.getElementById('histogramChart'));
    histogramChart.setOption({

        color: ["#87cefa", "#ff7f50", "#32cd32", "#da70d6", ],
        legend: {
            y: '250',
            x: 'center',
            type: 'scroll',
            data: ['第一车场', '第二车场', '第三车场', '第四车场'],
            textStyle: {
                color: '#ffffff',

            }
        },

        calculable: false,


        grid: {
            left: '5%',
            right: '5%',
            top: '10%',
            bottom: '20%',
            containLabel: true
        },

        tooltip: {
            trigger: 'axis',
            axisPointer: {
                type: 'shadow'
            }
        },

        xAxis: [{
            type: 'value',
            axisLabel: {
                show: true,
                textStyle: {
                    color: '#fff'
                }
            },
            splitLine: {
                lineStyle: {
                    color: ['#f2f2f2'],
                    width: 0,
                    type: 'solid'
                }
            }

        }],

        yAxis: [{
            type: 'category',
            data: ['硖石街道', '海洲街道', '海昌街道', '马桥街道'],
            axisLabel: {
                show: true,
                textStyle: {
                    color: '#fff'
                }
            },
            splitLine: {
                lineStyle: {
                    width: 0,
                    type: 'solid'
                }
            }
        }],

        series: [{
                name: '第一车场',
                type: 'bar',
                stack: '总量',
                itemStyle: {
                    normal: {
                        label: {
                            show: true,
                            position: 'insideRight'
                        }
                    }
                },
                data: [320, 302, 301, 400]
            },
            {
                name: '第二车场',
                type: 'bar',
                stack: '总量',
                itemStyle: {
                    normal: {
                        label: {
                            show: true,
                            position: 'insideRight'
                        }
                    }
                },
                data: [120, 132, 101, 99]
            },
            {
                name: '第三车场',
                type: 'bar',
                stack: '总量',
                itemStyle: {
                    normal: {
                        label: {
                            show: true,
                            position: 'insideRight'
                        }
                    }
                },
                data: [220, 182, 191, 300]
            },
            {
                name: '第四车场',
                type: 'bar',
                stack: '总量',
                itemStyle: {
                    normal: {
                        label: {
                            show: true,
                            position: 'insideRight'
                        }
                    }
                },
                data: [150, 212, 201, 222]
            }

        ]
    });

    // 车流量趋势
    const lineChart = this.$echarts.init(document.getElementById('lineChart'));
    lineChart.setOption({

        color: ["#87cefa", "#ff7f50", "#32cd32", "#da70d6", ],
        legend: {
            y: '250',
            x: 'center',
            type: 'scroll',
            textStyle: {
                color: '#ffffff',
            },
            data: ['第一车场', '第二车场', '第三车场', '第四车场', ],
        },
        calculable: false,
        tooltip: {
            trigger: 'item',
            formatter: "{a}<br/>{b}<br/>{c}条"
        },
        yAxis: [{
            type: 'value',
            // axisLine: {
            //     onZero: false
            // },
            // axisLine: {
            //     lineStyle: {
            //         color: '#034c6a'
            //     },
            // },

            // axisLabel: {
            //     textStyle: {
            //         color: '#fff'
            //     },
            //     formatter: function (value) {
            //         return value + "k条"
            //     },
            // },
            // splitLine: {
            //     lineStyle: {
            //         width: 0,
            //         type: 'solid'
            //     }
            // }
        }],
        xAxis: [{
            type: 'category',
            data: ['8:00', '10:00', '12:00', '14:00', '16:00', '18:00', '20:00', '22:00'],
            axisLine: {
                lineStyle: {
                    color: '#034c6a'
                },
            },
            splitLine: {
                "show": false
            },
            axisLabel: {
                textStyle: {
                    color: '#fff'
                },
                formatter: function (value) {
                    return value + ""
                },
            },
            // splitLine: {
            //     lineStyle: {
            //         width: 0,
            //         type: 'solid'
            //     }
            // },
        }],
        grid: {
            left: '5%',
            right: '5%',
            bottom: '20%',
            containLabel: true
        },
        series: [{
                name: '第一车场',
                type: 'line',
                smooth: true,
                itemStyle: {
                    normal: {
                        lineStyle: {
                            shadowColor: 'rgba(0,0,0,0.4)'
                        }
                    }
                },
                data: [15, 0, 20, 45, 22.1, 25, 70, 55, 76]
            },
            {
                name: '第二车场',
                type: 'line',
                smooth: true,
                itemStyle: {
                    normal: {
                        lineStyle: {
                            shadowColor: 'rgba(0,0,0,0.4)'
                        }
                    }
                },
                data: [25, 10, 30, 55, 32.1, 35, 80, 65, 76]
            },
            {
                name: '第三车场',
                type: 'line',
                smooth: true,
                itemStyle: {
                    normal: {
                        lineStyle: {
                            shadowColor: 'rgba(0,0,0,0.4)'
                        }
                    }
                },
                data: [35, 20, 40, 65, 42.1, 45, 90, 75, 96]
            },
            {
                name: '第四车场',
                type: 'line',
                smooth: true,
                itemStyle: {
                    normal: {
                        lineStyle: {
                            shadowColor: 'rgba(0,0,0,0.4)'
                        }
                    }
                },
                data: [45, 30, 50, 75, 52.1, 55, 100, 85, 106]
            }
        ]
    });

    // 今日进出场车型分析
    const lineChart2 = this.$echarts.init(document.getElementById('lineChart2'));
    lineChart2.setOption({

        color: ["#87cefa", "#ff7f50", "#32cd32", "#da70d6", ],
        legend: {
            y: '250',
            x: 'center',
            type: 'scroll',
            textStyle: {
                color: '#ffffff',

            },
            data: ['小型', '中型', '大型', 'SUV', ],
        },
        calculable: false,
        tooltip: {
            trigger: 'item',
            formatter: "{a}<br/>{b}<br/>{c}条"
        },
        yAxis: [{
            type: 'value',
            axisLine: {
                onZero: false
            },
            // axisLine: {
            //     lineStyle: {
            //         color: '#034c6a'
            //     },
            // },

            axisLabel: {
                textStyle: {
                    color: '#fff'
                },
                formatter: function (value) {
                    return value + "k条"
                },
            },
            splitLine: {
                lineStyle: {
                    width: 0,
                    type: 'solid'
                }
            }
        }],
        xAxis: [{
            type: 'category',
            data: ['8:00', '10:00', '12:00', '14:00', '16:00', '18:00'],
            axisLine: {
                lineStyle: {
                    color: '#034c6a'
                },
            },
            splitLine: {
                "show": false
            },
            axisLabel: {
                textStyle: {
                    color: '#fff'
                },
                formatter: function (value) {
                    return value + ""
                },
            },
            // splitLine: {
            //     lineStyle: {
            //         width: 0,
            //         type: 'solid'
            //     }
            // },
        }],
        grid: {
            left: '5%',
            right: '5%',
            bottom: '20%',
            containLabel: true
        },
        series: [{
                name: '小型',
                type: 'line',
                smooth: true,
                itemStyle: {
                    normal: {
                        lineStyle: {
                            shadowColor: 'rgba(0,0,0,0.4)'
                        }
                    }
                },
                data: [15, 0, 20, 45, 22.1, 25, ].reverse()
            },
            {
                name: '中型',
                type: 'line',
                smooth: true,
                itemStyle: {
                    normal: {
                        lineStyle: {
                            shadowColor: 'rgba(0,0,0,0.4)'
                        }
                    }
                },
                data: [25, 10, 30, 55, 32.1, 35, ].reverse()
            },
            {
                name: '大型',
                type: 'line',
                smooth: true,
                itemStyle: {
                    normal: {
                        lineStyle: {
                            shadowColor: 'rgba(0,0,0,0.4)'
                        }
                    }
                },
                data: [35, 20, 40, 65, 42.1, 45, ].reverse()
            },
            {
                name: 'SUV',
                type: 'line',
                smooth: true,
                itemStyle: {
                    normal: {
                        lineStyle: {
                            shadowColor: 'rgba(0,0,0,0.4)'
                        }
                    }
                },
                data: [45, 30, 50, 75, 52.1, 55, 6].reverse()
            }
        ]
    });
    },
    init(){
        const upImg = document.getElementById('up_img');
        const downImg = document.getElementById('down_img');
        const payDialog = document.getElementById('pay_dialog');
        const payBtn = document.getElementById('pay_btn');
        upImg.classList.add("hide");
        payDialog.classList.add("hide");
        let ii = 1;
        payBtn.addEventListener("click",function(){
            if(ii == 1){
                payDialog.classList.remove("hide");
                upImg.classList.remove("hide");
                downImg.classList.add("hide");
                ii = 0;
            }else if(ii == 0){
                payDialog.classList.add("hide");
                upImg.classList.add("hide");
                downImg.classList.remove("hide");
                ii = 1;
            }
        });
    }
    },
    mounted() {
        this.myMap();
        this.init();
    }
}
</script>
<style src="../assets/styles/common.css"></style>
