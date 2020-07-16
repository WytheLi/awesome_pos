<template>
    <div class="pos">
        <!-- Hello Pos! -->
        <!-- icon图标演示 -->
        <!-- <i class="icon iconfont icon-jinrudianpu" style="font-size: 2em"></i> -->
        <el-row id="order-list">
            <!-- 栅栏布局 共24分栏 -->
            <el-col :span="7">
                订单栏目
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
    .pos {
        background-color: orange;
    }
</style>