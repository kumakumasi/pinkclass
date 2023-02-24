<script>
// import { MyHeader } from "../components/MyHeader.vue";
// import { MyAside } from "../components/MyAside.vue";

// export default{
//   name: 'MyHome',
//   components:{
//     MyHeader,
//     MyAside,
//   },
// }
</script>

<template>
  <div class="home-container">
    <my-header>
      <h1>sss</h1>
    </my-header>
    <div class="home-main-box">
      <my-aside>
        <h1>sss</h1>
      </my-aside>
      <div class="home-main-body">
        <h1>sss</h1>
      </div>
    </div>
  </div>
</template>

<style lang="less" scoped>
  my-header{
    font-size: 12px;
    height:200px;
    width:100px;
    text-align: right;
    margin-top: 2rem;
    background-color:black;

  }
.home-contrainer {
  height: 100%;
  display: flex;
  flex-direction: column;

  .home-main-box {
    height: 100%;
    display: flex;
    .home-main-body {
      padding: 15px;
      flex: 1;
    }
  }
}
</style>
