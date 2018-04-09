<template>
  <div class="index">
   <el-row :gutter="9">
  <el-col align :xs="8" :sm="6" :md="4" :lg="3" :xl="1"><div class="grid-content bg-purple"></div></el-col>
  <el-col align :xs="4" :sm="6" :md="8" :lg="9" :xl="11"><div class="grid-content bg-purple-light"></div></el-col>
  <el-col align :xs="4" :sm="6" :md="8" :lg="9" :xl="11"><div class="grid-content bg-purple"></div></el-col>
  <el-col align :xs="8" :sm="6" :md="4" :lg="3" :xl="1"><div class="grid-content bg-purple-light"></div></el-col>
</el-row>
<el-button type="primary" icon="el-icon-search">搜索</el-button>
  <el-button type="primary" round>主要按钮</el-button>
  <el-button type="primary" >上传<i class="el-icon-upload el-icon--right"></i></el-button>
   <el-radio-group v-model="radio2">
    <el-radio :label="3">备选项</el-radio>
    <el-radio :label="6">备选项</el-radio>
    <el-radio :label="9">备选项</el-radio>
  </el-radio-group>
 

    <!-- 按钮样式 -->
     <div style="margin-top: 20px">
    <el-radio-group v-model="radio4" size="medium">
      <el-radio-button label="上海" ></el-radio-button>
      <el-radio-button label="北京"></el-radio-button>
      <el-radio-button label="广州"></el-radio-button>
      <el-radio-button label="深圳"></el-radio-button>
    </el-radio-group>
  </div>
    <!-- 按钮样式 -->

    <!-- input输入框 -->
    <div>
  <el-input placeholder="请输入内容" v-model="input3">
    <template slot="prepend">Http://</template>
  </el-input>
    </div>
    <!-- input输入框 -->

    <!-- inputNumber计数器 -->

     <el-input-number debounce="2000" v-model="num8" controls-position="right" @change="handleChange" :min="1" :max="10"></el-input-number>
   
    <!-- inputNumber计数器 -->
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data () {
    return {
        radio2: '3',
        radio4: '上海',
        num8:1
    }
  },
  methods:{
       handleChange(value) {
        console.log(value);
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    .el-col {
    border-radius: 4px;
  }
  .bg-purple-dark {
    background: #99a9bf;
  }
  .bg-purple {
    background: #d3dce6;
  }
  .bg-purple-light {
    background: #e5e9f2;
  }
  .grid-content {
    border-radius: 4px;
    min-height: 36px;
  }
 
</style>
