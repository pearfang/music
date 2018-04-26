<template>
        <nav class="header">
            <div class="logo">
              <img src="../assets/logo.png" alt="" width="50">
            </div>
            <ul class="navigationList">
              <li v-for="(item, index) in navArr" :key="index" :class="'navli'">
               <router-link :to="{path:'/list/'+item.post_id}">{{item.content}}</router-link>
              </li>
              <div class="header-search">
                <img src="../../static/images/search.png" alt="" width="50">
              </div>
            </ul>
            
        </nav>  
</template>
<script>

export default {
  data() {
    return {
      navArr: [
        {
          content: "电影",
          title: "电影",
          post_id:1
        },
        {
          content: "图书",
          title: "图书",
          post_id:2
        },
        {
          content: "广播",
          title: "广播",
          post_id:3
        },
        {
          content: "小组",
          title: "小组",
          post_id:4
        }
      ]
    };
  }
};
</script>
<style scoped>
.header {
  border-bottom: 1px solid #f3f3f3;
    -webkit-box-pack: justify;
    justify-content: space-between;
    -webkit-box-align: center;
    align-items: center;
    padding: 0 18px;
    background: #fff;
    height: 47px;
    box-sizing: border-box;
    display: -webkit-box;
    display: flex;
}
.logo{
  width: 50px;
  height: 50px;
}
.navigationList  li.navli{

     color: #42bd56;
    font-size: 15px;
    margin-right: 19px;
}
.navigationList {
  display: flex;
  align-items: center;
}
</style>

