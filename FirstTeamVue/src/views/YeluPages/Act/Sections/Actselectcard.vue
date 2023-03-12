<script>


</script>

<template>   
        <div class="">
            <el-button type="info" text-lg font-weight-bolder >
            <router-link to="/pages/Yelu-pages/act/ActHot">熱門精選</router-link>           
            </el-button>
            <el-button  type="info" text-lg font-weight-bolder>
            <router-link to="/pages/Yelu-pages/act/ActHot">北部</router-link>           
            </el-button>
            <el-button  type="info" text-lg font-weight-bolder>
            <router-link to="/pages/Yelu-pages/act/ActHot">中部</router-link>           
            </el-button>
            <el-button  type="info" text-lg font-weight-bolder>
            <router-link to="/pages/Yelu-pages/act/ActHot">南部</router-link>           
            </el-button>
            <el-button  type="info" text-lg font-weight-bolder>
            <router-link to="/pages/Yelu-pages/act/ActHot">東部</router-link>           
            </el-button>            
            <hr />
            <div>
                <router-view></router-view>
            </div>
            
        </div>
</template>

<style>
/* .tab-button {
    padding: 6px 10px;
    border-top-left-radius: 3px;
    border-top-right-radius: 3px;
    border: 1px solid #ccc;
    cursor: pointer;
    background: #f0f0f0;
    margin-bottom: -1px;
    margin-right: -1px;
}

.tab-button:hover {
    background: #e0e0e0;
}

.tab-button.active {
    background: #e0e0e0;
}

.tab {
    border: 1px solid #ccc;
    padding: 10px;
} */

</style>