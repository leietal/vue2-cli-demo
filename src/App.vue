<template>
  <div id="app">
    <vHeader :siteInfo="siteInfo"></vHeader>
    <vContent :content="content"></vContent>
    <vFooter :siteInfo="siteInfo"></vFooter>
  </div>
</template>

<script>
import vHeader from "./components/header";
import vFooter from "./components/footer";
import vContent from "./components/content";

export default {
  name: "app",
  components: {
    vHeader,
    vFooter,
    vContent
  },
  data() {
    return {
      siteInfo: {
        title: "小米",
        desc: "为发骚而生",
        name: "小米科技",
        url: "http://www.xiaomi.com"
      },
      content: 
        [{
        title: "小米智能马桶盖",
        btnName: "官网查看",
        msg: "http://www.xiaomi.com"
        },{
        title: "小米智能马桶盖",
        btnName: "天猫网店查看",
        msg: "https://xiaomi.tmall.com/shop/view_shop.htm"
        }]
      
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
