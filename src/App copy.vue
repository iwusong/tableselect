<template>
  <div>
    <el-table style="width: 50vw" :data="tableData" border>
      <div v-for="item in Object.keys(tableData[0])" :key="item" :v-if="flag(item)">
        <el-table-column :prop="item" :label="item" width="200"></el-table-column>
      </div>
    </el-table>
    <div></div>
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
          address: "上海市普陀区金沙江路 1518 弄",
          AA: "AAA",
          BB: "bbb",
          CC: "CCC",
          DD: "DDD",
          EE: "EEE",
          FF: "FFF",
          GG: "GGG"
        },
        {
          date: "2017-05-02",
          name: "王大虎",
          address: "上海市普陀区金沙江路 1517 弄",
          AA: "AAA",
          BB: "bbb",
          CC: "CCC",
          DD: "DDD",
          EE: "EEE",
          FF: "FFF",
          GG: "GGG"
        },
        {
          date: "2018-05-02",
          name: "王老虎",
          address: "上海市普陀区金沙江路 1516 弄",
          AA: "AAA",
          BB: "bbb",
          CC: "CCC",
          DD: "DDD",
          EE: "EEE",
          FF: "FFF",
          GG: "GGG"
        },
        {
          date: "2019-05-02",
          name: "王1虎",
          address: "上海市普陀区金沙江路 1511 弄",
          AA: "AAA",
          BB: "bbb",
          CC: "CCC",
          DD: "DDD",
          EE: "EEE",
          FF: "FFF",
          GG: "GGG"
        },
        {
          date: "2010-05-02",
          name: "王2虎",
          address: "上海市普陀区金沙江路 1512 弄",
          AA: "AAA",
          BB: "bbb",
          CC: "CCC",
          DD: "DDD",
          EE: "EEE",
          FF: "FFF",
          GG: "GGG"
        }
      ],
      namelist: ['AA']
    };
  },

  methods: {
    flag(item) {
      if (this.namelist.indexOf(item) !== -1) {
        console.log(item);
        return false;
      }
    }
  }
};
</script>