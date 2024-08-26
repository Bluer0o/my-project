<template>
  <div>
    <el-form
      ref="form"
      label-position="left"
      label-width="100px"
      :model="formLabelAlign"
      class="form"
    >
      <el-form-item label="サービス:">
        <el-radio-group v-model="radio1" class="item">
          <div class="radio_item" :label="1">全部</div>
          <div class="radio_item" :label="2">宅配配送</div>
          <div class="radio_item" :label="3">発送</div>
          <div class="radio_item" :label="4">預かり</div>
        </el-radio-group>
      </el-form-item>
      <el-form-item label="ステータス:">
        <el-radio-group v-model="radio2" class="item">
          <div class="radio_item" :label="1">全部</div>
          <div class="radio_item" :label="2">宅配配送</div>
          <div class="radio_item" :label="3">発送</div>
          <div class="radio_item" :label="4">預かり</div>
        </el-radio-group>
      </el-form-item>
      <el-form-item label="日付:">
        <el-date-picker
          v-model="value1"
          type="daterange"
          range-separator="至"
          start-placeholder="開始日付"
          end-placeholder="終了日付"
        >
        </el-date-picker>
      </el-form-item>
    </el-form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      formLabelAlign: {
        name: "",
        region: "",
        date1: "",
        date2: "",
        delivery: false,
        type: [],
        resource: "",
        desc: "",
      },
      radio1: 1,
      radio2: 1,
      value1:''
    };
  },
};
</script>

<style>
.form {
  padding: 12px 0px 12px 24px;
  .el-form-item {
    margin-bottom: 0px !important;
    display: flex;
    align-items: center;
  }
  .item {
    display: flex;
    gap: 16px;
    .radio_item {
      display: flex;
      gap: 10px;
      color: #000;
      font-size: 14px;
      cursor: pointer;
      line-height: 21px;
      padding: 2px 8px 2px 8px;
      &:active {
        border-radius: 4px;
        background: #1677ff;
        color: #fff;
      }
    }
  }
}
</style>