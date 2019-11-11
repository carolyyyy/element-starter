<template>
  <div id="app">
    <el-container>
      <el-aside width="360px">
        <el-container>
          <el-header>Fast Initializr</el-header>
          <p class="subTitle">Framework for Automated Software Testing</p>
          <el-main>
            Fast.common Version<br>
            Project Name<br>
            Dependencies<br><br><br><br>
          </el-main>
          <el-footer>©2017-2019 Fast Framework. All rights reserved.</el-footer>
        </el-container>
      </el-aside>
      <el-main>
        <el-container>
          <el-header>
            <el-link type="primary">help</el-link>
            
            <el-link type="primary">email</el-link>
          </el-header>
          <el-main>
            <br><br><br>
            <el-tabs v-model="activeName" @tab-click="handleClick">
              <el-tab-pane label="v 1.0" name="first"></el-tab-pane>
              <el-tab-pane label="v 2.0" name="second"></el-tab-pane>
            </el-tabs><br>
            <el-input v-model="input"></el-input><br><br><br>
            <myCard></myCard>
            <!--<my></my>-->
          </el-main>
          <el-footer>
             <el-button type="primary">Generate</el-button>
          </el-footer>
        </el-container>
      </el-main>
    </el-container>
  </div>
</template>

<script>
import myCard from './components/myCard';
import my from './components/my';
export default {
  data() {
    return {
      activeName: 'second',
      input: 'com.example.fast'
    };
  },
  components:{
    myCard,
    my
  },
  methods: {
    handleClick(tab, event) {
      console.log(tab, event);
    }
  }
}
</script>

<style lang='less' scoped>
#app {
  font-family: Helvetica, sans-serif;
  text-align: center;
}

.subTitle {
  color: gray;
}

.el-header{
  background-color: #EDEDED;
  color: #333;
  text-align: center;
  line-height: 60px;
  font-family:Arial, Helvetica, sans-serif;
  font-size:xx-large;
  font-weight: bold
}

.el-footer {
  background-color: #EDEDED;
  color: #333;
  text-align: center;
  line-height: 60px;
  font-family: 'Times New Roman', Times, serif;
  font-size: small;
  font-weight: bold
}

.el-main .el-header{
  background-color: #ffffff;
  color: #333;
  line-height: 60px;
  text-align: right;
}

.el-main .el-footer{
  background-color: #ffffff;
  color: #333;
  line-height: 60px;
}

.el-aside {
  background-color: #EDEDED;
  color: #333;
  text-align: center;
  
}

.el-aside .el-main{
  background-color: #EDEDED;
  color: 	#000000	;
  text-align: right;
  line-height: 100px;
}

.el-input{
  line-height: 100px;
}

.el-main {
  background-color: #ffffff;
  color: #333;
  text-align: center;
  
}

body > .el-container {
  margin-bottom: 40px;
}

.el-container:nth-child(5) .el-aside,
.el-container:nth-child(6) .el-aside {
  line-height: 260px;
}

.el-row {
  margin-bottom: 20px;
  line-height: 100px;
  &:last-child {
    margin-bottom: 0;
  }
}
.el-col {
  border-radius: 4px;
  line-height: 100px;
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
.row-bg {
  padding: 10px 0;
  background-color: #f9fafc;
}
</style>
