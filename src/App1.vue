 <template>
  <div>
    <div>
      <button @click="clickbutton(index)" v-for="(item,index) in tabledata[0]" :key="item">{{item}}</button>
    </div>
    <div style="height:36px">

    </div>
    <table>
      <table border="1">
        <tr v-for="item in tabledata" :key="item.key">
          <td v-show="!flag[index]" v-for="(data,index) in item" :key="data.key">{{data}}</td>
        </tr>
      </table>
    </table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      tabledata: [
        [
          "ID",
          "AA",
          "BB",
          "CC",
          "DD",
          "EE",
          "FF",
          "GG",
          "ZZ",
          "XX",
          "CC",
          "VV"
        ],
        [
          "9527",
          "AA",
          "BB",
          "CC",
          "DD",
          "EE",
          "FF",
          "GG",
          "ZZ",
          "XX",
          "CC",
          "VV"
        ],
        [
          "9528",
          "AA",
          "BB",
          "CC",
          "DD",
          "EE",
          "FF",
          "GG",
          "ZZ",
          "XX",
          "CC",
          "VV"
        ],
        [
          "9529",
          "AA",
          "BB",
          "CC",
          "DD",
          "EE",
          "FF",
          "GG",
          "ZZ",
          "XX",
          "CC",
          "VV"
        ]
      ],
      flag: {}
    };
  },
  created() {
    this.tabledata[0].forEach((item, index) => {
      this.flag[index] = false;
    });
    console.log(this.flag);
  },
  methods: {
    clickbutton(index) {
      this.flag[index] = !this.flag[index];
      this.$forceUpdate();
    }
  }
};
</script>

<style scoped>
table {
  font-size: 0.6vw;
  color: #686868;
  border-collapse: collapse;
}
td {
  padding: 0.5vw;
  border: solid 1px #686868;
  width: 50px;
}
button {
  width: 61.5px;
}
</style>