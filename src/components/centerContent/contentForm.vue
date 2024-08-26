<template>
  <div class="content_table">
    <div class="inp">
      <el-input
        placeholder="サービス番号、カスタマー、伝票番号を入力してください"
        v-model="input3"
        class="input-with-select"
      >
        <el-button slot="append" icon="el-icon-search" class="inp_icon"></el-button>
      </el-input>
    </div>
    <div class="content_center">
      <div>合計85件</div>
      <el-pagination layout="prev, pager, next" :total="50"> </el-pagination>
      <div class="dowm">
        <span>作成時間</span>
        <i class="el-icon-arrow-down"></i>
      </div>
    </div>
    <div class="table">
      <el-table :data="tableData" style="width: calc(100% - 20px)">
        <el-table-column prop="name" label="サービス名称" width="140">
        </el-table-column>
        <el-table-column prop="address" label="ロッカー" width="180">
        </el-table-column>
        <el-table-column prop="thing" label="物件" width="160">
        </el-table-column>
        <el-table-column prop="number" label="カスタマー" width="200">
        </el-table-column>
        <el-table-column prop="date" label="作成時間" width="234">
        </el-table-column>
        <el-table-column prop="status" label="ステータス" width="160">
          <template slot-scope="scope">
            <el-tag
              :type="
                scope.row.status === 1
                  ? 'success'
                  : scope.row.status === 2
                  ? 'danger'
                  : 'primary'
              "
              >{{ getStatus(scope.row.status) }}</el-tag
            >
          </template>
        </el-table-column>
        <el-table-column fixed="right" label="操作" width="100">
          <template slot-scope="scope">
            <el-button @click="handleClick(scope.row)" type="text" size="small"
              >詳細</el-button
            >
          </template>
        </el-table-column>
      </el-table>
    </div>
    <div class="footer">
      <el-pagination
        @size-change="handleSizeChange"
        @current-change="handleCurrentChange"
        :current-page="currentPage4"
        :page-sizes="[10, 20, 30, 40]"
        :page-size="10"
        layout="total, sizes, prev, pager, next, jumper"
        :total="400"
      >
      </el-pagination>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      tableData: [
        {
          name: "宅配配送",
          address: "11F-10号",
          thing: "Pabbitマンション",
          number: 555,
          date: "2024/08/07 21:10:01",
          status: 2,
        },
        {
          name: "宅配配送",
          address: "11F-10号",
          thing: "Pabbitマンション",
          number: 555,
          date: "2024/08/07 21:10:01",
          status: 1,
        },
        {
          name: "宅配配送",
          address: "11F-55555",
          thing: "Pabbitマンション",
          number: 6666,
          date: "2024/08/07 21:10:01",
          status: 3,
        },
      ],
      currentPage4: 4,
      input3:''
    };
  },
  methods: {
    getStatus(status) {
      if (status === 1) {
        return "進行中";
      }
      if (status === 2) {
        return "滞留中";
      }
      return "完了";
    },
    handleSizeChange(val) {
      console.log(`每页 ${val} 条`);
    },
    handleCurrentChange(val) {
      console.log(`当前页: ${val}`);
    },
  },
};
</script>

<style>
.content_table {
  padding: 20px 24px 12px 24px;
}
.inp {
  width: 504px;
  .el-input-group__append{
    background:#1677ff !important;
  }
  .inp_icon{
    color: #fff !important;
  }
}
.content_center {
  height: 24px !important;
  padding: 20px 0px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  .dowm {
    color: #1677ff;
    cursor: pointer;
  }
}
.footer {
  margin-top: 20px;
}
</style>