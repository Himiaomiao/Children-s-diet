<template>
  <div class="student" style="height:490px ; font-size:13px">
    <el-table
      :data="tableData.filter(data => !search ||( data.name.toLowerCase().includes(search.toLowerCase())) ||
      ( data.time.toLowerCase().includes(search.toLowerCase()))) "
      :size="medium"
      :height="490"
      style="width:100%"
      :highlight-current-row="true"
      :min-width="1100"
    >
      <el-table-column :min-width="100" label="套餐名称" prop="name"></el-table-column>
      <el-table-column :min-width="90" label="周期" prop="time"></el-table-column>
      <el-table-column :min-width="80" label="重量" prop="wight"></el-table-column>
      <el-table-column :min-width="100" label="能量" prop="quality"></el-table-column>
      <el-table-column :min-width="90" label="蛋白质" prop="protein"></el-table-column>
      <el-table-column :min-width="100" label="脂质" prop="lipid"></el-table-column>
      <el-table-column :min-width="100" label="配餐日期" prop="date"></el-table-column>
      <el-table-column :min-width="100" label="菜名" prop="mealname"></el-table-column>
      <el-table-column align="right" :min-width="250">
        <!-- eslint-disable-next-line -->
        <template slot="header" slot-scope="scope">
          <el-input v-model="search" size="mini" placeholder="输入关键字搜索" :width="100" />
        </template>
        <template slot-scope="scope">
          <el-button size="mini" @click="handleEdit(scope.$index, scope.row)">套餐详情</el-button>
          <el-button size="mini" type="danger" @click="handleDelete(scope.$index, scope.row)">删除</el-button>
        </template>
      </el-table-column>
    </el-table>
  </div>
</template>

<script>
export default {
  name: "NutritionalAssessment",
  data() {
    return {
      tableData: [
        {
          name: "营养套餐",
          time: "2",
          wight: "100kg",
          quality: "90",
          protein: "0.5",
          lipid: "10",
          date: "2020-03-26",
          mealname: "糖醋排骨"
        },
        {
          name: "营养套餐",
          time: "2",
          wight: "100kg",
          quality: "90",
          protein: "0.5",
          lipid: "10",
          date: "2020-03-26",
          mealname: "糖醋排骨"
        },
        {
          name: "营养套餐",
          time: "2",
          wight: "100kg",
          quality: "90",
          protein: "0.5",
          lipid: "10",
          date: "2020-03-26",
          mealname: "糖醋排骨"
        },
        {
          name: "营养套餐",
          time: "2",
          wight: "100kg",
          quality: "90",
          protein: "0.5",
          lipid: "10",
          date: "2020-03-26",
          mealname: "糖醋排骨"
        },
        {
          name: "营养套餐",
          time: "2",
          wight: "100kg",
          quality: "90",
          protein: "0.5",
          lipid: "10",
          date: "2020-03-26",
          mealname: "糖醋排骨"
        },
        {
          name: "营养套餐",
          time: "2",
          wight: "100kg",
          quality: "90",
          protein: "0.5",
          lipid: "10",
          date: "2020-03-26",
          mealname: "糖醋排骨"
        },
        {
          name: "营养套餐",
          time: "2",
          wight: "100kg",
          quality: "90",
          protein: "0.5",
          lipid: "10",
          date: "2020-03-26",
          mealname: "糖醋排骨"
        },
        {
          name: "营养套餐",
          time: "2",
          wight: "100kg",
          quality: "90",
          protein: "0.5",
          lipid: "10",
          date: "2020-03-26",
          mealname: "糖醋排骨"
        },
        {
          name: "营养套餐",
          time: "2",
          wight: "100kg",
          quality: "90",
          protein: "0.5",
          lipid: "10",
          date: "2020-03-26",
          mealname: "糖醋排骨"
        }
      ],
      search: ""
    };
  },
  methods: {
    handleEdit(index, row) {
      console.log(index, row);
    },
    handleDelete(index, row) {
      console.log(index, row);
      this.tableData.splice(index, 1);
    }
  }
};
</script>

<style  scoped>
</style>
