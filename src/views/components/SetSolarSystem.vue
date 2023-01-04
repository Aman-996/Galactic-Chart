<template>
  <div class="set-div">
    <el-form style="padding: 0px 20px">
      <el-form-item label="公转：">
        <el-switch
          v-model="isRevolution"
          :title="[!isRevolution ? '开始公转' : '停止公转']"
          active-color="#13ce66"
          inactive-color="#ff4949"
          @change="changeRevolution"
        ></el-switch>
      </el-form-item>
      <el-form-item label="自转：">
        <el-switch
          v-model="isRotation"
          :title="[!isRotation ? '开始自转' : '停止自转']"
          active-color="#13ce66"
          inactive-color="#ff4949"
          @change="changeRotation"
        ></el-switch>
      </el-form-item>
    </el-form>
  </div>
</template>
<script>
export default {
  props: {},
  components: {},
  data() {
    return {
      isRevolution: true, //公转状态
      isRotation: true, //自转状态
    };
  },
  computed: {},
  watch: {},
  created() {},
  mounted() {},
  methods: {
    //公转
    changeRevolution(val) {
      let data = {
        key: "isRevolution",
        val: val,
      };
      this.changeSet(data);
    },
    //自转
    changeRotation(val) {
      let data = {
        key: "isRotation",
        val: val,
      };
      this.changeSet(data);
    },
    //改变设置
    changeSet(data) {
      this.$emit("changeSet", data);
    },
  },
};
</script>
<style scoped lang='scss'>
.set-div {
  user-select: none;
  color: #fff;
  background-color: rgba(0, 0, 0, 0.5);
  position: absolute;
  width: 135px;
  bottom: 0;
  left: 0;
}
::v-deep .el-form-item__label {
  color: #fff;
}
</style>