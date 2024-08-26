<template>
  <div>
    <el-row>
      <el-col :span="24"
        ><div class="grid-content bg-purple-dark">
          <div class="left">
            <div class="title">
              <i class="el-icon-edit"></i>
              <div class="name">{{ name }}</div>
            </div>
            <div class="center">
              <i class="el-icon-s-fold icon"></i>
              <i class="el-icon-refresh icon"></i>
            </div>
          </div>
          <div class="right">
            <div class="right_name">{{ personalName }}</div>
            <i class="el-icon-caret-bottom icon"></i>
          </div></div
      ></el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "Pabbit Admin",
      personalName: "许江敏",
    };
  },
};
</script>

<style>
.el-row {
}
.el-col {
  border-radius: 4px;
}
.bg-purple-dark {
  background: #1677ff;
  color: #fff;
}
.bg-purple {
  background: #d3dce6;
}
.bg-purple-light {
  background: #e5e9f2;
}
.grid-content {
  min-height: 48px;
  display: flex;
  align-items: center;
  padding: 0px 16px;
  justify-content: space-between;
}
.row-bg {
  padding: 10px 0;
  background-color: #f9fafc;
}
.left {
  display: flex;
}
.title {
  display: flex;
  align-items: center;
  width: 180px;
  .name {
    margin-left: 8px;
  }
}
.icon {
  font-size: 22px;
  margin-right: 30px;
}
.right {
  font-size: 14px;
  display: flex;
  align-items: center;
  .icon {
    margin-left: 5px;
    font-size: 14px;
    margin-right: 0px !important;
  }
}
</style>