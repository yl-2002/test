<template>
  <div>
    <div class="nav_top">
      <p>
        <span>
          <a style="    margin-left: 9px;">外卖基础设置</a>
        </span>
      </p>
    </div>
    <div class="box">
      <table class="bg" style="border-collapse:collapse;    margin-bottom: 30px;">
        <tr>
          <td style="background:rgb(250,250,250)" class="first">
            <span style="color:red">*</span>名称：
          </td>
          <td class="secend">
            <el-checkbox-group v-model="checkLists">
              <el-checkbox label="美食"></el-checkbox>
              <el-checkbox label="超市"></el-checkbox>
              <el-checkbox label="鲜果"></el-checkbox>
              <el-checkbox label="甜点饮品"></el-checkbox>
              <el-checkbox label="土豪馆"></el-checkbox>
              <el-checkbox label="鲜花蛋糕"></el-checkbox>
              <el-checkbox label="烧烤"></el-checkbox>
            </el-checkbox-group>
          </td>
        </tr>
        <tr>
          <td style="background:rgb(250,250,250)" class="first">营业时间：</td>
          <td class="secend">
            <div style="font-size:12px">
              【 + 】
              <span style="color:rgb(255,136,0)">【默认24小时营业】</span>
            </div>
            <div style="margin:30px 0">
              <el-col :span="4">
                <span>从</span>
                <el-input
                  size="mini"
                  placeholder="输入时间"
                  v-model="time.input"
                  style="width: 80%;margin-left:10px;"
                ></el-input>
              </el-col>
              <el-col class="line" :span="1" style="margin-top: 5px;
    margin-right: -16px;">至</el-col>
              <el-col :span="4">
                <el-input
                  size="mini"
                  placeholder="输入时间"
                  v-model="time.input1"
                  style="width: 80%;margin-right:1px;"
                ></el-input>
                <span>【-】</span>
              </el-col>
            </div>
            <br />
            <div style="    margin: 30px 0px;">
              <el-col :span="4">
                <span>从</span>
                <el-input
                  size="mini"
                  placeholder="输入时间"
                  v-model="time.input3"
                  style="width: 80%;margin-left:10px;"
                ></el-input>
              </el-col>
              <el-col class="line" :span="1" style="margin-top: 5px;
    margin-right: -16px;">至</el-col>
              <el-col :span="4">
                <el-input
                  size="mini"
                  placeholder="输入时间"
                  v-model="time.input4"
                  style="width: 80%;margin-right:1px;"
                ></el-input>
                <span>【-】</span>
              </el-col>
            </div>
          </td>
        </tr>
        <tr>
          <td style="background:rgb(250,250,250)" class="first">外卖配送模式：</td>
          <td class="secend">
            <el-radio-group v-model="radio">
              <el-radio style="margin:0 0 10px 0" :label="3">自动接单，并由商家配送</el-radio>
              <br />
              <el-radio :label="6">手动接单，手动指派</el-radio>
            </el-radio-group>
          </td>
        </tr>
        <tr>
          <td style="background:rgb(250,250,250)" class="first">配送信息：</td>
          <td class="secend">
            <div style="font-size:12px">
              【 + 】
              <span style="color:rgb(255,136,0)">【默认不收配送费】</span>
            </div>
            <div style="    margin: 30px 0px;">
              <el-col :span="4">
                <el-input
                  size="mini"
                  placeholder="输入时间"
                  v-model="time.input5"
                  style="width: 90%;margin-left:10px;"
                ></el-input>
              </el-col>
              <el-col
                class="line"
                :span="4"
                style="margin-top: 5px;
    margin-right: -66px;"
              >公里之内&nbsp;&nbsp;起送费</el-col>
              <el-col :span="3">
                <el-input
                  size="mini"
                  placeholder="输入时间"
                  v-model="time.input6"
                  style="width: 90%;margin-right:1px;"
                ></el-input>
              </el-col>
              <el-col
                class="line"
                :span="3"
                style="margin-top: 5px;
    margin-right: -66px;"
              >元&nbsp;&nbsp;配送费</el-col>
              <el-col :span="5">
                <el-input
                  size="mini"
                  placeholder="输入时间"
                  v-model="time.input7"
                  style="width: 80%;margin-left:10px;"
                ></el-input>
                <span>【-】</span>
              </el-col>
            </div>
            <br />
            <div style="    margin: 30px 0px;">
              <el-col :span="4">
                <el-input
                  size="mini"
                  placeholder="输入时间"
                  v-model="time.input8"
                  style="width: 90%;margin-left:10px;"
                ></el-input>
              </el-col>
              <el-col
                class="line"
                :span="4"
                style="margin-top: 5px;
    margin-right: -66px;"
              >公里之内&nbsp;&nbsp;起送费</el-col>
              <el-col :span="3">
                <el-input
                  size="mini"
                  placeholder="输入时间"
                  v-model="time.input9"
                  style="width: 90%;margin-right:1px;"
                ></el-input>
              </el-col>
              <el-col
                class="line"
                :span="3"
                style="margin-top: 5px;
    margin-right: -66px;"
              >元&nbsp;&nbsp;配送费</el-col>
              <el-col :span="5">
                <el-input
                  size="mini"
                  placeholder="输入时间"
                  v-model="time.input0"
                  style="width: 80%;margin-left:10px;"
                ></el-input>
                <span>【-】</span>
              </el-col>
            </div>
          </td>
        </tr>

     
       

        <tr>
          <td style="background:rgb(250,250,250)" class="first">
            <span style="color:red">*</span>打包费信息：
          </td>
          <td class="secend">
            <el-col :span="2" style="padding-top: 9px;margin-right:-20px"><div>基础价：</div></el-col><el-col :span="5"><el-input style="width:100%" v-model="input4" size="small" placeholder="请输入内容"></el-input></el-col><el-col :span="14" style="padding-top: 9px;margin-left:20px"><div>元 <span style="color:rgb(255,136,0)">【0：为不收打包费，-1：全收打包费，大于0:小于该值，收取打包费;大于该值，不收打包费】</span></div></el-col>
          </td>
        </tr>
        <tr>
          <td style="background:rgb(250,250,250)" class="first">
            <span style="color:red">*</span>商家公告：
          </td>
          <td class="secend">
              <el-input
  type="textarea"
  :rows="10"
  style="width:500px"
  v-model="textarea">
</el-input>
          </td>
        </tr>
      </table>
      <el-button type="warning" size="small" @click.native="bj">确认提交</el-button>
      <el-button type="success" size="small" @click.native="bj1">取消</el-button>
    </div>
  </div>
</template>
<script>
export default {
  name: "shouye",
  data() {
    return {
      editorOption: {
        modules: {
          toolbar: [
            [
              "bold",
              "italic",
              "clean",
              "strike",
              "blockquote",
              "code-block",
              "formula",
              "image",
              "video",
              "clean",
              "align",
            ],
          ],
        },
      },
      checkList: ["外卖"],
      checkLists: ["选中且禁用", "复选框 A"],
      gb: true,
      input: "",
      input4: "0",
      time: {
        input: "10:00",
        input1: "13:00",
        input3: "17:00",
        input4: "20:00",
        input5:'1',
        input6:'15',
        input7:'2',
        input8:'5',
        input9:'30',
        input0:'5'
      },
      w1: "",
      bk: true,
      radio: 3,
      gb1: false,
      bk1: false,
        textarea:'',
      url:
        "https://fuss10.elemecdn.com/e/5d/4a731a90594a4af544c0c25941171jpeg.jpeg",
    };
  },
  methods: {
    cy() {
      this.msg = "餐饮美食";
    },
    cy1() {
      this.msg = "休闲娱乐";
    },
    cy2() {
      this.msg = "美容美发";
    },

    bj() {
      this.$alert("确认提交吗？", "提示", {
        confirmButtonText: "确定",
        callback: (action) => {
          this.$alert("成功", "提示", {
        confirmButtonText: "确定",
        callback: (action) => {
          this.$router.push({
            path: "/waimaiy",
          });
        },
      });
       
        },
      });
    },
    bj1() {
      this.$router.push({
            path: "/waimaiy",
          });
    },
    cy11() {
      this.msg1 = "广东";
    },
    cy12() {
      this.msg1 = "湖南";
    },
    cy23() {
      this.msg1 = "四川";
    },
    cy111() {
      this.msg2 = "广州";
    },
    cy121() {
      this.msg2 = "深圳";
    },
    cy222() {
      this.msg2 = "佛山";
    },
    cy1111() {
      this.msg3 = "天秀";
    },
    cy122() {
      this.msg3 = "天河";
    },
    cy223() {
      this.msg3 = "黄埔";
    },
  },
};
</script>
<style scoped>
.el-button {
  margin-bottom: 20px;
  margin-right: 57px;
  margin-left: 74px;
}
.first {
  width: 180px;
  text-align: right;
}
.secend {
  width: 1000px;
}
.box >>> .el-radio__label {
  font-size: 12px;
}
.box >>> .el-radio__input.is-checked + .el-radio__label {
  color: rgb(255, 136, 0);
}
.box >>> .el-radio__input.is-checked .el-radio__inner {
  border-color: rgb(255, 136, 0);
  background: rgb(255, 136, 0);
}
.box >>> .el-checkbox__input.is-checked + .el-checkbox__label {
  color: rgb(255, 136, 0);
}
.box >>> .el-checkbox__input.is-checked .el-checkbox__inner,
.el-checkbox__input.is-indeterminate .el-checkbox__inner {
  background-color: rgb(255, 136, 0);
  border-color: rgb(255, 136, 0);
}
.box >>> .el-checkbox__inner:hover {
  border-color: rgb(255, 136, 0);
}
.bg tr td {
  border: 1px solid rgb(215, 215, 215);
  padding: 20px 10px;
  font-size: 12px;
  display: table-cell;
  vertical-align: middle;
}

.tt {
  line-height: 1.7;
  font-size: 14px;
}
.el-main {
  padding: 0 !important;
  min-height: 1000px;
  margin: 60px 0 0 -61px;
  background: rgb(242, 242, 242);
}
.el-image {
  padding: 4px;
  margin: 0 3px;
  border: 1px solid gray;
}
.el-main p {
  padding: 7px 0 7px 165px;
  height: 36px;
  text-indent: 17px;
  background: white;
  line-height: 36px;
}
.el-main p span {
  line-height: 1.7;
  border-left: 3px solid rgb(255, 136, 0);
}
.box {
  padding: 29px 60px 0 60px;
  background: white;
  min-height: 500px;
  width: 1185px;
  margin: 34px auto;
}
.box h2 {
  margin: 0 0 0 327px;
}
.Newpwd .el-input {
  margin: 0 0 0 146px;
}
.Imgbig {
  background: url(/img/u370.80a172f4.png) no-repeat;
  background-size: 92% 90%;
  width: 1282px;
  height: 1201px;
  margin: 43px 0 0 -50px;
}
.Newpwd {
  width: 505px;

  margin: 45px 0;
}
.Newpwd div {
  margin: 17px 0 -29px 17px;
}
.Newpwd i {
  color: red;
}
.Newpwd .el-link :hover {
  cursor: auto;
  color: rgb(28, 23, 29);
}
.el-link {
  margin-left: 4px;
}
.el-button--success {
  margin-right: 57px;
  margin-left: 74px;
}
.box >>> .ql-editor {
  height: 200px;
}
</style>