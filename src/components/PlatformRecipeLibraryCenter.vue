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
      <el-table-column :min-width="100" label="食物名称" prop="name"></el-table-column>
      <el-table-column :min-width="90" label="重量" prop="wight"></el-table-column>
      <el-table-column :min-width="80" label="适宜餐次" prop="fittime"></el-table-column>
      <el-table-column :min-width="100" label="营养评价" prop="evaluate"></el-table-column>
      <el-table-column :min-width="90" label="制作方法" prop="make"></el-table-column>
      <el-table-column :min-width="100" label="饮食禁忌" prop="taboo"></el-table-column>
      <el-table-column :min-width="100" label="原料组成" prop="makefor"></el-table-column>
      <el-table-column :min-width="100" label="营养组成" prop="composition"></el-table-column>
      <el-table-column align="right" :min-width="250">
        <!-- eslint-disable-next-line -->
        <template slot="header" slot-scope="scope">
          <el-input v-model="search" size="mini" placeholder="输入关键字搜索" :width="100" />
        </template>
        <template slot-scope="scope">
          <el-button size="mini" @click="handleEdit(scope.$index, scope.row)">食物详情</el-button>
          <el-button size="mini" type="danger" @click="handleDelete(scope.$index, scope.row)">删除</el-button>
        </template>
      </el-table-column>
    </el-table>
  </div>
</template>

<script>
export default {
  name: "PlatformRecipeLibrarryCenter",
  data() {
    return {
      tableData: [
        {
          name: "鸡肉",
          wight: "100kg",
          fittime: "中午",
          evaluate: "美味",
          make: "爆炒",
          taboo: "辣",
          makefor: "鸡肉，姜蒜",
          composition: "蛋白质，脂质"
        },
        {
          name: "鸡肉",
          wight: "100kg",
          fittime: "中午",
          evaluate: "美味",
          make: "爆炒",
          taboo: "辣",
          makefor: "鸡肉，姜蒜",
          composition: "蛋白质，脂质"
        },
        {
          name: "鸡肉",
          wight: "100kg",
          fittime: "中午",
          evaluate: "美味",
          make: "爆炒",
          taboo: "辣",
          makefor: "鸡肉，姜蒜",
          composition: "蛋白质，脂质"
        },
        {
          name: "鸡肉",
          wight: "100kg",
          fittime: "中午",
          evaluate: "美味",
          make: "爆炒",
          taboo: "辣",
          makefor: "鸡肉，姜蒜",
          composition: "蛋白质，脂质"
        },
        {
          name: "鸡肉",
          wight: "100kg",
          fittime: "中午",
          evaluate: "美味",
          make: "爆炒",
          taboo: "辣",
          makefor: "鸡肉，姜蒜",
          composition: "蛋白质，脂质"
        },
        {
          name: "鸡肉",
          wight: "100kg",
          fittime: "中午",
          evaluate: "美味",
          make: "爆炒",
          taboo: "辣",
          makefor: "鸡肉，姜蒜",
          composition: "蛋白质，脂质"
        },
        {
          name: "鸡肉",
          wight: "100kg",
          fittime: "中午",
          evaluate: "美味",
          make: "爆炒",
          taboo: "辣",
          makefor: "鸡肉，姜蒜",
          composition: "蛋白质，脂质"
        },
        {
          name: "鸡肉",
          wight: "100kg",
          fittime: "中午",
          evaluate: "美味",
          make: "爆炒",
          taboo: "辣",
          makefor: "鸡肉，姜蒜",
          composition: "蛋白质，脂质"
        },
        {
          name: "鸡肉",
          wight: "100kg",
          fittime: "中午",
          evaluate: "美味",
          make: "爆炒",
          taboo: "辣",
          makefor: "鸡肉，姜蒜",
          composition: "蛋白质，脂质"
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
