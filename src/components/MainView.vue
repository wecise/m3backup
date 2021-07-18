<template>

  <div class="box">
    <el-card shadow="hover" v-for="item in list" :key="item.name" class="box-item">
        <span class="el-icon-coin"></span> 
        <h4>{{item.title}}</h4>
    </el-card>
  </div>
  
</template>

<script>

export default {
  name: 'MainView',
  props: {
    global: Object
  },
  data(){
    return {
      list: [
        {name: "etcd", title: "备份备份", icon:"el-icon-"},
        {name: "omdb-ddl", title: "数据结构备份"},
        {name: "omdb-data", title: "数据备份"},
        {name: "dfs", title: "文件系统备份"}
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .box{
    display: flex;
    flex-wrap: wrap;
    align-content: center;
  }
  .box-item{
    width: 20%;
    height: 10em;
    text-align: center;
    margin: 15px;
    padding: 20px;
  }
  .box-item span{
    font-size: 44px;
  }

</style>
