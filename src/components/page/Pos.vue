<template>
    <div class="pos">
        <!-- Hello Pos! -->
        <!-- icon图标演示 -->
        <!-- <i class="icon iconfont icon-jinrudianpu" style="font-size: 2em"></i> -->
        <el-row id="order-list">
            <!-- 栅栏布局 共24分栏 -->
            <el-col :span="7">
                <el-tabs type="card">
                    <el-tab-pane label="点餐">
                        <el-table :data="tableData" stripe show-summary style="width: 100%"> 
                            <el-table-column prop="goodsName" label="商品" width="100"> </el-table-column> 
                            <el-table-column prop="count" label="数量" width="100"> </el-table-column> 
                            <el-table-column prop="price" label="金额"> </el-table-column>

                            <el-table-column
                            label="操作"
                            width="100">
                            <template slot-scope="scope">
                                <el-button type="text" size="small" @click="addCount(scope.$index, scope.row)">增加</el-button>
                                <el-button type="text" size="small" @click="deleteRow(scope.$index, scope.row)">删除</el-button>
                            </template>
                            </el-table-column>
                        </el-table>
                        <div class="tools">
                            <el-button type="warning">挂单</el-button>
                            <el-button type="danger">删除</el-button>
                            <el-button type="success">结账</el-button>
                        </div>
                    </el-tab-pane>
                    <el-tab-pane label="挂单">挂单</el-tab-pane>
                    <el-tab-pane label="外卖">外卖</el-tab-pane>
                </el-tabs>
            </el-col>
            <el-col :span="17">
                商品栏目
            </el-col>
        </el-row>
    </div>
</template>

<script>
export default {
    name: 'pos',
    data() {
        return {
            tableData: [{
                goodsName: '可口可乐',
                price: 8,
                count:1
            }, 
            {
                goodsName: '香辣鸡腿堡',
                price: 15,
                count:1
            }, 
            {
                goodsName: '爱心薯条',
                price: 8,
                count:1
            }, 
            {
                goodsName: '甜筒',
                price: 8,
                count:1
            }]
        }
    },
    methods: {
        addCount(index, row) {
            this.tableData[index].count += 1;
        },
        deleteRow(index, row) {
            this.tableData.splice(index, 1);
        }
    },
    /* 由于引入了Element组件库，DOM树Element被托管，直接在style中设置height高度100%失效
    /* > mounted是vue中的一个钩子函数,一般在初始化页面完成后,再对dom节点进行相关操作
    /* 这里用来在页面初始化完成之后给组件添加满屏高度 */
    mounted: function() {
        var clientHeight = document.body.clientHeight;
        document.getElementById('order-list').style.height = clientHeight + 'px';
    }
}
</script>

<style scoped>
    .tools {
        margin-top: 10px;
    }
</style>