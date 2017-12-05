<template>
  <div id="app">
    <vHeader :siteInfo="siteInfo"></vHeader>
    <div class="content">
      <div class="content-wrap">
        <ul>
          <li v-for="i in 10">
            <div class="item">
              <div><img class="img" src="./assets/logo.png"/></div>
              <div><span class="title">小米智能马桶盖</span></div>
              <div><button class="btn">查看明细</button></div>
            </div>
          </li>
        </ul>
      </div>
    </div>
    <vFooter :siteInfo="siteInfo"></vFooter>
  </div>
</template>

<script>
import vHeader from "./components/header";
import vFooter from "./components/footer";

export default {
  name: "app",
  components: {
    vHeader,
    vFooter
  },
  data() {
    return {
      siteInfo: {
        title: "小米",
        desc: "为发骚而生",
        name: "小米科技",
        url: "http://www.xiaomi.com"
      }
    };
  }
};
</script>

<style>
#app {
  text-align: center;
  color: #2c3e50;
  background-color: #f1f1f1;
  height: 100%;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.header,
.footer{
  flex-grow: 0;
  flex-shrink: 0;
}
.content{
  height: auto;
  flex-grow: 1;
  flex-shrink: 0;
  background-color: #eee;
}
.content-wrap{
  max-width: 1200px;
  margin: 20px auto;
  padding: 20px;
  box-sizing: border-box;
}
.content-wrap li{
  display: inline-block;
  margin: 19px;
}
.item{
  display: inline-block;
  padding: 20px;
  box-sizing: border-box;
  box-shadow: 0 0 10px 2px #eee;
  background-color: #f7f7f7;
}
.item:hover{
  box-shadow: 0 0 20px 2px #ccc;
  cursor: default;
}
.item .img{
  height: 150px;
}
.item .title{
  display: inline-block;
  margin: 10px;
}
.item .btn{
  padding: 10px 50px;
  border: none;
  background-color: #f91;
  color: #fff;
}
.item .btn:hover{
  cursor: pointer;
  background-color: #f61;
}
html,
body {
  height: 100%;
}
* {
  padding: 0;
  margin: 0;
}
ul{
  list-style: none;
}
</style>
