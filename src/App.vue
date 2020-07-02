  <template>
  <div>
    <el-table style="width:100%" :data="tableData">
      <el-table-column v-if="display[1]" prop="date" label="日期" width="180"></el-table-column>
      <el-table-column v-if="display[2]" prop="name" label="AA" width="180"></el-table-column>
      <el-table-column v-if="display[3]" prop="name" label="BB" width="180"></el-table-column>
      <el-table-column v-if="display[4]" prop="name" label="CC" width="180"></el-table-column>
      <el-table-column v-if="display[5]" prop="name" label="DD" width="180"></el-table-column>
      <el-table-column v-if="display[6]" prop="name" label="EE" width="180"></el-table-column>
      <el-table-column v-if="display[7]" prop="address" label="地址"></el-table-column>
    </el-table>
    <div>
      <el-switch class="display" active-text="日期" v-model="display[1]"></el-switch>
      <el-switch class="display" active-text="AA" v-model="display[2]"></el-switch>
      <el-switch class="display" active-text="BB" v-model="display[3]"></el-switch>
      <el-switch class="display" active-text="CC" v-model="display[4]"></el-switch>
      <el-switch class="display" active-text="DD" v-model="display[5]"></el-switch>
      <el-switch class="display" active-text="EE" v-model="display[6]"></el-switch>
      <el-switch class="display" active-text="地址" v-model="display[7]"></el-switch>
    </div>
  </div>
</template>

  <script>
export default {
  data() {
    return {
      tableData: [
        {
          date: "2016-05-02",
          name: "王小虎",
          address: "上海市普陀区金沙江路 1518 弄"
        },
        {
          date: "2016-05-04",
          name: "王小虎",
          address: "上海市普陀区金沙江路 1517 弄"
        },
        {
          date: "2016-05-01",
          name: "王小虎",
          address: "上海市普陀区金沙江路 1519 弄"
        },
        {
          date: "2016-05-03",
          name: "王小虎",
          address: "上海市普陀区金沙江路 1516 弄"
        }
      ],
      display: {
        1: true,
        2: true,
        3: true,
        4: true,
        5: true,
        6: true,
        7: true
      }
    };
  }
};
</script>
<style>
.display {
  margin: 10px;
  padding: 0 40px;
}
el-table {
  width: 99.9%;
}
</style>