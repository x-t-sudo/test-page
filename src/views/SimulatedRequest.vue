<template>
  <div id="SimulatedRequest">
    <el-row type="flex">
      <el-col :span="4">
        <el-select v-model="value" placeholder="请选择服务器">
          <el-option
            v-for="item in services"
            :key="item.value"
            :label="item.name"
            :value="item.value"
          >
          </el-option>
        </el-select>
      </el-col>
      <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
      <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
      <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
    </el-row>
  </div>
</template>
<script>
export default {
    data(){
        return{
            services:[{value:"https://a.xrview.ga",name:"服务器1"}]
        }
    }
}
</script>
<style scoped>
#SimulatedRequest {
  margin-top: 0.6rem;
  /* border: 1px solid red; */
}
el-col{
    border: 1px solid slategrey;
}
</style>