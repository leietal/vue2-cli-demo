<template>
  <div class="content">
      <div class="content-wrap">
        <ul>
          <li v-for="it in content">
            <div class="item">
              <div><img class="img" src="../assets/logo.png"/></div>
              <div><span class="title">{{it.title}}</span></div>
              <div><button class="btn" v-on:click="look(it.msg)">{{it.btnName}}</button></div>
            </div>
          </li>
        </ul>
      </div>
    </div>
</template>

<script>
export default {
  name: "vContent",
  data() {
    return {};
  },
  props: ["content"],
  methods: {
      look: (value) => {
          window.open(value);
      }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

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

</style>
