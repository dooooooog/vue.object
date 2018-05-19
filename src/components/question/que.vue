<template>
<div class="wenda">
  <div class="left">
    <div class="left-top">
      <span class="tit">程序员自己的问答社区</span>
      <a class="button">我要提问</a>
    </div>
    <div class="nav">
      <a v-for="item in navs">{{item}}</a>
      <div class="switch-box">
        <span>只显示关注内容</span>
        <div class="switch js-switch">
          <div class="fill">
            <div class="outer"></div>
          </div>
          <div class="inner"></div>
        </div>
      </div>
    </div>
    <div class="topic"></div>
    <div class="que-list"></div>
    <div class="lq">
    	<list-question></list-question>
    </div>    
  </div>
  <div class="right">
    <div class="userinfo"></div>
    <div class="guanzhu"></div>
    <div>这里是广告</div>
    <div class="hotque"></div>
    <div class="answer">
      <h3>
        <span>回答雷锋榜</span>
        <span>今日</span>
        <span>一周</span>
      </h3>
    </div>
  </div>
</div>
</template>

<script>
import listQuestion from './listQuestion.vue'
    export default {
    	 components: {
           listQuestion
         },
        name: "que",
      data(){
          return{
            navs:['推荐','最新','等待回答','话题']
         }
      }
    }
</script>

<style scoped>
.wenda{
  display: flex;
  margin: 3% 7% 0;
}
  .left{
    display: flex;
    flex-direction: column;
    flex: 2.5;
    margin-right: 5%;
  }
  .left-top{
    background: url("../../../static/image/wenda_title_bg.png");
    padding: 5% 4%;
    display: flex;
    justify-content: space-between;
    margin-bottom: 1%;
    align-items: center;
  }
  .tit{
    color: #07111B;
    letter-spacing: 3px;
    font-size: 1.5em;
  }
  .button{
    padding: 1.3% 4%;
    /*不加这个width会导致刷新后这个元素的padding依据父盒子的宽高*/
    width: 12%;
    background: #F01414;
    border-radius:4px;
    color: #fff;
    cursor: pointer;
  }
  .nav{
    padding: 2%;
    color: #93999F;
    border-bottom: 1px solid #D9DDE1;
    display: flex;
    justify-content: space-between;
  }
  .nav a:hover{
    color: #303133;
    cursor: pointer;
  }
  .switch-box{
    margin-left: 20%;
    width: 30%;
    font-size: 0.75rem;
    display: flex;
    justify-content: center;
  }
  .switch{
    cursor: pointer;
    margin-left:5%;
    position: relative;
    width: 18%;
    -webkit-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none;
    overflow: hidden;
  }
  .fill{
    background: rgba(147,153,159,.4);
    border-radius: 3px;
    margin-top: 7px;
    height: 6px;
    overflow: hidden;
  }
  .fill .outer{
    margin-left: -20px;
    width: 40px;
    height: 6px;
    border-radius: 3px;
    background: #fcd0d0;
  }
  .switch-box .switch .inner {
  position: absolute;
  box-sizing: border-box;
  top: 0;
  left: 0;
  height: 20px;
  border: 2px solid #93999F;
  width: 20px;
  background: #fff;
  border-radius: 100%;
}
.right{
  display: flex;
  flex-direction: column;
  flex: 1;
}
</style>
