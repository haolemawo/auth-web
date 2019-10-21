<template>
  <el-container>
    
      <div class="header-class">
        <div class="header-left">
          <div><i class="i-class">|</i><span style="font-size: 22px;">WORD格式</span></div>
          <div><span>无封面</span>
            <el-checkbox v-model="isCover" />
          </div>
          <div style="display：inline"><span>版本</span>
            <el-checkbox-group
              v-model="wordEditions"
              @change="handleCheckedWordEditionsChange"
            >
              <el-checkbox>03版</el-checkbox>
              <el-checkbox>07版</el-checkbox>
            </el-checkbox-group>
          </div>
          <div><span>编辑WORD</span></div>
        </div>
        <div class="header-right">
          <div><i class="i-class">|</i><span style="font-size: 22px;">落款控制</span></div>
          <div><span>输出文件落款控制</span></div>
          <div><span>落款内容</span></div>
          <div><span>落款日期</span></div>
        </div>
      </div>
  </el-container>
</template>
<script>
export default {
  name: "Format",
  data() {
    return {
      isCover: false,
      wordEditions: ''
    };
  },
  methods :{
      handleCheckedWordEditionsChange(value){
          this.isIndeterminate = false;
      }
  }
};
</script>
<style lang="scss" scoped>
.el-header {
  padding-top: 10px;
  margin: 0px 0px 0px 0px;
}
.el-main {
  padding: 10px 0px 0px 0px;
}
.el-footer {
  margin: 10px 0 0 0;
  background-color: #ffffff;
}
.header-class {
  margin-top: 10px;
  height: 100%;
}
.header-left {
  margin: 0px 0px 0px 0px;
  float: left;
  text-align: left;
  width: 49.5%;
  height: 100%;
  background-color: #ffffff;
}
.header-right {
  margin: 0px 0px 0px 0px;
  float: right;
  text-align: left;
  width: 49.5%;
  height: 100%;
  background-color: #ffffff;
}
.main-class {
  height: 100%;
  background-color: #ffffff;
}
.el-button--danger {
  color: #fff;
  background-color: #b60000;
  border-color: #b60000;
}
.i-class {
  color: #a40000;
  letter-spacing: 7px;
  font-size: 25px;
  font-weight: 800;
}
.el-row {
  margin-top: 15px;
  margin-left: 25px;
  font-size: 14px;
}
/deep/ .el-checkbox__input.is-checked .el-checkbox__inner {
  background-color: #ac1420;
  border-color: #ac1420;
}
/deep/ .el-checkbox__input.is-indeterminate .el-checkbox__inner {
  background-color: #ac1420;
  border-color: #ac1420;
}
/deep/ .el-checkbox__inner {
  width: 20px;
  height: 20px;
}
</style>

