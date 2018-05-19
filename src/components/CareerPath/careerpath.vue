<template>
<div class="bg">
  <div class="topbg">
    <div class="top">
      <div class="title">
        <div class="nav-item">
          <h2 class="tit">成长  因陪伴不再孤单</h2>
          <div class="top-desc-box">
            <p class="desc-item">课程体系化</p>
            <em class="desc-line">/</em>
            <p class="desc-item">问答作业1V1</p>
            <em class="desc-line">/</em>
            <p class="desc-item">学练测一体</p>
            <em class="desc-line">/</em>
            <p class="desc-item">视频不限期</p>
            <em class="desc-line">/</em>
            <p class="desc-item">服务随开随用</p>
          </div>
        </div>
      </div>
      <div class="tab-nav">
        <router-link to="/CareerPath/careerpath" class="navitem">
          <span class="navtext">全部</span>
        </router-link>
        <router-link to="/CareerPath/careerpath/web" class="navitem">
          <span class="navtext">Web前端攻城狮</span>
        </router-link>
        <router-link to="/CareerPath/careerpath/java" class="navitem">
          <span class="navtext">Java攻城狮</span>
        </router-link>
        <router-link to="/CareerPath/careerpath/android" class="navitem">
          <span class="navtext">Android攻城狮</span>
        </router-link>
        <router-link to="/CareerPath/careerpath/php"  class="navitem">
          <span class="navtext">PHP攻城狮</span>
        </router-link>
        <router-link to="/CareerPath/careerpath/ios" class="navitem">
          <span class="navtext">iOS / C++攻城狮</span>
        </router-link>
      </div>
    </div>
  </div>
  <div class="top">
    <router-view></router-view>
  </div>
</div>
</template>

<script>
    export default {
      name: "careerpath",
      data(){
        return{

        }
      },
      methods:{
        }
    }
</script>

<style scoped>
  a{
    text-decoration:none;
  }
  .router-link-active{
    text-decoration:none;
  }
  .bg{
    background: #F3F5F7;
  }
  .topbg{
    background-color:#379FDE;
  }
  .top{
    margin: 0 7%;
    padding-top: 3%;
  }
  .tit{
    color: #fff;
    margin-bottom: 1%;
    font-size:30px;
  }
  .desc-item{
    margin: 0 0.8%;
    text-shadow: 0 4px 8px rgba(7, 17, 27, 0.4);
    color: rgba(255, 255, 255, 0.6);
  }
  .title{
    margin-bottom: 3%;
  }
.top-desc-box{
  display: flex;
  justify-content: center;
}
  .tab-nav{
    display: flex;
    justify-content: space-between;
  }
  .navitem{
    padding: 2% 4%;
    color:#fff;
  }
  .navitemall:hover{
    background: rgba(243, 245, 247, 0.2);
    border-radius: 12px 12px 0 0;
  }
  .navtext{
    text-shadow: 0 2px 4px rgba(7, 17, 27, 0.4);
    transition: .3s all linear;
    font-size: 16px;
    cursor: pointer;
  }
  .active{
    color: #07111b;
    background: #F3F5F7;
    border-radius: 12px 12px 0 0;
  }
</style>
