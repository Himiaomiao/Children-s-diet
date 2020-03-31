<template>
  <div class="student" style="height:490px ; font-size:13px">
    <el-table
      :data="tableData.filter(data => !search ||( data.idnumber.toLowerCase().includes(search.toLowerCase())) ||
      ( data.name.toLowerCase().includes(search.toLowerCase()))) "
      :size="medium"
      :height="490"
      style="width:100%"
      :highlight-current-row="true"
      :min-width="1100"
    >
      <el-table-column :min-width="100" label="学号" prop="idnumber"></el-table-column>
      <el-table-column :min-width="90" label="班级" prop="classnumber"></el-table-column>
      <el-table-column :min-width="80" label="姓名" prop="name"></el-table-column>
      <el-table-column :min-width="50" label="性别" prop="sex"></el-table-column>
      <el-table-column :min-width="50" label="年龄" prop="age"></el-table-column>
      <el-table-column :min-width="60" label="身高" prop="height"></el-table-column>
      <el-table-column :min-width="60" label="体重" prop="weight"></el-table-column>
      <el-table-column :min-width="80" label="入学时间" prop="studenttime"></el-table-column>
      <el-table-column :min-width="70" label="监护人" prop="guartian"></el-table-column>
      <el-table-column :min-width="110" label="与监护人关系" prop="guartianR"></el-table-column>
      <el-table-column :min-width="100" label="监护人电话" prop="guartianphone"></el-table-column>
      <el-table-column align="right" :min-width="250">
        <!-- eslint-disable-next-line -->
        <template slot="header" slot-scope="scope">
          <el-input v-model="search" size="mini" placeholder="输入关键字搜索" :width="100" />
        </template>
        <template slot-scope="scope">
          <el-button size="mini" @click="handleEdit(scope.$index, scope.row)">编辑</el-button>
          <el-button size="mini" type="danger" @click="handleDelete(scope.$index, scope.row)">删除</el-button>
        </template>
      </el-table-column>
    </el-table>
  </div>
</template>

<script>
export default {
  name: "StudentCenter",
  data() {
    return {
      tableData: [
        {
          idnumber: "1900300101",
          classnumber: "19003001",
          name: "莫喵喵",
          sex: "女",
          age: "2",
          height: "1.90",
          weight: "5",
          studenttime: "2020-02-25",
          guartian: "马云",
          guartianR: "父女",
          guartianphone: "123456789"
        },
        {
          idnumber: "1900300102",
          classnumber: "19003001",
          name: "莫喵喵",
          sex: "女",
          age: "1",
          height: "1.90",
          weight: "5",
          studenttime: "2020-02-25",
          guartian: "马云",
          guartianR: "父女",
          guartianphone: "123456789"
        },
        {
          idnumber: "1900300103",
          classnumber: "19003001",
          name: "莫喵喵",
          sex: "女",
          age: "3",
          height: "1.90",
          weight: "5",
          studenttime: "2020-02-25",
          guartian: "马云",
          guartianR: "父女",
          guartianphone: "123456789"
        },
        {
          idnumber: "1900300104",
          classnumber: "19003001",
          name: "莫喵喵",
          sex: "女",
          age: "1",
          height: "1.90",
          weight: "5",
          studenttime: "2020-02-25",
          guartian: "马云",
          guartianR: "父女",
          guartianphone: "123456789"
        },
        {
          idnumber: "1900300104",
          classnumber: "19003001",
          name: "莫喵喵",
          sex: "女",
          age: "1",
          height: "1.90",
          weight: "5",
          studenttime: "2020-02-25",
          guartian: "马云",
          guartianR: "父女",
          guartianphone: "123456789"
        },
        {
          idnumber: "1900300104",
          classnumber: "19003001",
          name: "莫喵喵",
          sex: "女",
          age: "1",
          height: "1.90",
          weight: "5",
          studenttime: "2020-02-25",
          guartian: "马云",
          guartianR: "父女",
          guartianphone: "123456789"
        },
        {
          idnumber: "1900300104",
          classnumber: "19003001",
          name: "莫喵喵",
          sex: "女",
          age: "1",
          height: "1.90",
          weight: "5",
          studenttime: "2020-02-25",
          guartian: "马云",
          guartianR: "父女",
          guartianphone: "123456789"
        },
        {
          idnumber: "1900300104",
          classnumber: "19003001",
          name: "莫喵喵",
          sex: "女",
          age: "1",
          height: "1.90",
          weight: "5",
          studenttime: "2020-02-25",
          guartian: "马云",
          guartianR: "父女",
          guartianphone: "123456789"
        },
        {
          idnumber: "1900300104",
          classnumber: "19003001",
          name: "莫喵喵",
          sex: "女",
          age: "1",
          height: "1.90",
          weight: "5",
          studenttime: "2020-02-25",
          guartian: "马云",
          guartianR: "父女",
          guartianphone: "123456789"
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
