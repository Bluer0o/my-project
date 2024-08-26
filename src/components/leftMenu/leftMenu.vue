<template>
  <div>
    <el-col>
      <el-menu default-active="2" class="el-menu-vertical-demo">
        <el-menu-item v-for="item in menuName" :key="item" class="item">
          <span slot="title">{{ item }}</span>
        </el-menu-item>
      </el-menu>
    </el-col>
  </div>
</template>

<script>
export default {
  data() {
    return {
      menuName: [
        "Dashboard",
        "物件リスト",
        "デバイスリスト",
        "IMEI リスト",
        "解錠記録",
        "ロッカー記録",
        "ロッカーサービス",
        "アカウント管理",
        "運営ツール",
      ],
    };
  },
  methods: {},
};
</script>

<style>
.el-menu-vertical-demo {
  width: 180px;
  background-color: #fff;
  height: calc(100vh - 48px);
}
.item {
  padding-left: 16px !important;
  text-align: left;
  height: 40px !important;
  display: flex;
  align-items: center;
  margin: 10px 0px;
}
</style>