<template>
	<div class="list1">
	<div class="img">
		<img src="../../../static/image/jstop.png"/>
	</div>
	<div class="right">
		<div class="sign">
			<p>来自</p>
			<div class="sign_list" v-for="item in items.index">
			<el-button size="mini" plain>{{item}}</el-button>
			</div>
		</div>
		<h3>{{items.question}}</h3>
		<div class="done" v-if="items.isDone">
			<div class="row">
			<el-button size="mini" v-if="items.isAdopt"   style="background-color: #67c23a;color:white;" plain>已采纳</el-button> 
			<div class="user_name" ><h4>{{items.userName}}</h4></div>
			<p style="font-size:12px;">回答:</p>
			</div>
			<div class="row">
			<p class="answerfor">{{items.answertext}}</p>
			</div>
			<div class="row ju"> 
			<el-button size="mini" plain>已帮助用户<span>{{items.helpnumber}}</span></el-button>
			<a><span>{{items.disagree}}人反对</span></a>
			<a>分享</a>
			</div>
		</div>
		<div class="nodone" v-if="!items.isDone">
			<el-button size="mini" plain>撰写答案</el-button> 
			<a>回答问题最高可获得<span>{{items.point}}</span>积分哦！</a>
			<a><span>{{items.answernumber}}</span>个回答</a>
			<a>关注</a>
		</div>
	</div>
	</div>
</template>
<script>
export default {
        name: "list_question",
    data(){
          return{
          	items:{
     	img:"../../../static/image/jstop.png",
     	  index:[
     	  	"javascript",
     	  	"javascript",
     	  	"javascript",
     	  ],
     	  question:"fuck you",
     	  isDone:true,
     	  isAdopt:true,
     	  userName:"sbsbsbsbsb",
     	  answertext:"ojbkojbkojbkojbk",
     	  helpnumber:0,
     	  point:2,
     	  answernumber:2,
     	  disagree:2,
     	 }
        }
    }
}
</script>
<style >
.img img{
  width: 48px;
}
.list1{
   display: flex;
   flex-flow: row nowrap;
  
   width: 100%;
   padding:20px;

}
.right{
	padding-left: 20px;
}
.right h3{
	display: flex;
	justify-content: flex-start;
	padding: 0px 5px 20px 0px;
}
.sign{
	display: flex;
    flex-flow: row nowrap; 
    align-items: center;
}
.sign p{
	font-size: 12px;
}
.sign_list{
padding: 0 10px;
}
.done{
		display: flex;
    flex-flow: column nowrap; 
}
.row{
	display: flex;
    flex-flow: row nowrap;
    align-items: center;

}
.user_name{
	padding:0 10px;
}
.answerfor{
	padding-bottom: 25px;
	padding-left: 5px;
}
.ju{
width: 80%;
justify-content: space-between;
}
</style>