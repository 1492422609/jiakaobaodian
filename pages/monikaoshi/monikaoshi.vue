<template>
	<view @touchstart="start" @touchend="end">
      
       	<view class="header_header" >
       		<view style="display: flex;">
       				<view  style="color: black;padding-top: 70rpx;margin-left: 30rpx;font-size: 40rpx;" @click="con">
       				    返回
       				</view>
       				<view style="margin-top: 70rpx;font-size: 40rpx;margin-left: 110rpx;">
       					{{countdown_time}}
       				</view>
       		</view>
       	</view>	
       					
       	<view class="top"  >
       		<view class="top_1" >
       			<view class="quesiton_now">
       				{{quesiton_now}}
       			</view>
       			<view class="quesiton_total">
       				{{quesiton_total}}
       			</view>
       		</view>
       		<view class="top_2_wai">
       			{{type}}
       		</view>
       		<view class="top_3_wai">
       			<image src="https://z3.ax1x.com/2021/07/26/WRI4AI.png" mode="widthFix" class="top_photo"></image>
       			<view class="top_text">
       				读题
       			</view>
       		</view>
       		<view class="top_4_wai" @click="fons">
       			<image src="https://z3.ax1x.com/2021/07/26/WRI5Nt.png" mode="widthFix" class="top_photo"></image>
       			<view class="top_text">
       				设置
       			</view>
       		</view>
       	</view>
       	<view class="topic" :style="{'font-size':font_size+'rpx'}">
       		{{topic}}
       	</view>
       	<view>
       		<image v-show="ima" :src=imag mode="widthFix" style="width: 90%;margin-left: 5%;margin-top: 10rpx;"></image>
       	</view>
		<view class="answer_total">
       		<view class="answer" v-for="(qut,index) in question" :ikey="index" :style="{'font-size':font_size+'rpx'}" @click="questio(qut.id)">
       			<view class="answer_pad">
       				<view :style="{margin: qut.ques=== '' ? '0rpx' : '20rpx'}">
       					{{qut.ques}}
       				</view>
       			</view>
       		</view>				
       	</view>
	    <view style="height: 200rpx;"></view>
       	
		<view class="size" v-show="size">
			<!-- <view class="line"></view> -->
	    	<view @click="fons">
	    		<view class="size_bottom" >
					<view class="line"></view>
	    			<view>
	    				<view class="bottom_topic">
	    					字体大小设置
	    				</view>
	    				<view class="line_5"></view>
	    			</view>
					<view @click.stop="stop">
						<view class="size_bottom_text">
							<view class="">
								小号
							</view>
							<view class="">
								标准
							</view>
							<view class="">
								特大
							</view>
						</view>
						<view style="display:flex ;margin-left:100rpx  ;">
							<view class="">
								A
							</view>
							<view :class="font_size==30 ? 'size_cir1':'size_cir'" @click="font_size0" ></view>
							<view class="size-line" ></view>
							<view :class="font_size==35 ? 'size_cir1':'size_cir'" @click="font_size2"></view>
							<view class="size-line"></view>
							<view :class="font_size==40 ? 'size_cir1':'size_cir'" @click="font_size3"></view>
							<view class="size-line"></view>
							<view :class="font_size==45 ? 'size_cir1':'size_cir'" @click="font_size4"></view>
							<view class="size-line"></view>
							<view :class="font_size==50 ? 'size_cir1':'size_cir'" @click="font_size5"></view>
							<view style="font-size: 50rpx;">
								A
							</view>
						</view>
							    		
					</view>
				</view>				
	    	</view>
	    </view>

	    <view class="footer">
	    	<view class="line"></view>
			<view  style="display: flex; padding-bottom: 20rpx;">
				<view class="collection" @click="shoucang">
					<image src="https://z3.ax1x.com/2021/07/26/WWSz1H.png" mode="widthFix" class="footer_photo"></image>
					<view class="footer_text">
						收藏
					</view>
				</view>
				<view class="share">
					<image src="https://z3.ax1x.com/2021/07/26/WWpScd.png" mode="widthFix" class="footer_photo"></image>
					<view class="footer_text">
						分享
					</view>
				</view>
				<view class="yon">
					<image src="https://z3.ax1x.com/2021/07/26/WWppjA.png" mode="widthFix" class="footer_photo"></image>
					<view style="color: #0CAF00;margin-left: 3rpx;">
						{{duiques}}
					</view>
					<image src="https://z3.ax1x.com/2021/07/26/WWpCnI.png" mode="widthFix" class="footer_photo"  style="margin-left:15rpx;"></image>
					<view style="color: #FF0000;margin-left: 3rpx;">
						{{cuoques}}
					</view>
				</view>
				<view class="footer_question" @click="pop">
					<image src="https://z3.ax1x.com/2021/07/26/WWpPBt.png" mode="widthFix" class="footer_photo"></image>
					<view class="">
						{{quesiton_now}}
					</view>
					<view class="">
						{{quesiton_total}}
					</view>
				</view>
			</view>
	        <view class="footer_pop" v-show="box" >
	        	<view   :class="[item.answer==''?'circulal_kong' :item.answer==item.answer1?'circulal':'circulal_cuo']"  v-for="(item,i) in a" :key="i" @click="returnque(i)">
	        		{{i+1}}
	        	</view>
						
	        </view>
		</view>
	    <view v-show="protect" class="protect" @click="quanguan"></view>
	
	</view>
</template>

<script>
	var that
	export default {
		methods: {
			questio(e){
				
				let i = that.qus;
				if(that.a[i].answer==''){
					that.a[i].answer=e
					if(that.a[i].answer==that.a[i].answer1){
						that.duiques=that.duiques+1
					}else{
						that.cuoques=that.cuoques+1
					}
				}
				
				console.log(JSON.stringify(that.a[i].answer))
				console.log(JSON.stringify(that.a[i].answer1))
				this.zuohua()
				this.cunchu()	
			},
		    
			quanguan(){
				if(that.size==true){
					that.size=false;
					that.protect=false
				}
				if(that.box==true){
					that.box=false;
					that.protect=false
				}
			},
			
			start(e){
			  this.startData.clientX=e.changedTouches[0].clientX;      
			  this.startData.clientY=e.changedTouches[0].clientY;
			},
			end(e){
			  // console.log(e)
			  const subX=e.changedTouches[0].clientX-this.startData.clientX;
			  const subY=e.changedTouches[0].clientY - this.startData.clientY;
			  if(subY>50 || subY<-50){
			     console.log('上下滑')
			  }else{
			     if(subX>100){
			       console.log('右滑')
				   if(that.qus>0){
				   	  this.youhua()		   
				   }
			     }else if(subX<-100){
			       console.log('左滑')
				   this.zuohua()
			     }else{
			       // console.log('无效')
			     }
			  }
			},
	
			zuohua(){
				that.qus=that.qus+1;
				let i = that.qus;
				this.quesiton_now=i+1
				that.topic=that.quesiton_tot[i].question_content
				that.question[0].ques=that.quesiton_tot[i].option1
				that.question[0].id='A'
				that.question[1].ques=that.quesiton_tot[i].option2
				that.question[1].id='B'
				that.question[2].ques=that.quesiton_tot[i].option3
				that.question[2].id='C'
				that.question[3].ques=that.quesiton_tot[i].option4
				that.question[3].id='D'
				that.a[i].answer1=that.quesiton_tot[i].answer
				if(that.question[3].ques===null){
					 that.question[0].ques='对'
					 that.question[0].id='对'
					 that.question[1].ques='错'
					 that.question[1].id='错'
					 that.question[2].ques=''
					 that.question[3].ques=''
					 that.type='判断'
					 // console.log(that.question[0].id)
				}
				if(that.quesiton_tot[i].pic_image===null){
					that.ima=false
				}else{
					 that.imag=that.quesiton_tot[i].pic_image
					 that.ima=true
				}

			},
			youhua(){
				that.qus=that.qus-1;
				let i = that.qus;
				this.quesiton_now=i+1
				that.topic=that.quesiton_tot[i].question_content
				that.question[0].ques=that.quesiton_tot[i].option1
				that.question[0].id='A'
				that.question[1].ques=that.quesiton_tot[i].option2
				that.question[1].id='B'
				that.question[2].ques=that.quesiton_tot[i].option3
				that.question[2].id='C'
				that.question[3].ques=that.quesiton_tot[i].option4
				that.question[3].id='D'
				that.a[i].answer1=that.quesiton_tot[i].answer
				if(that.question[3].ques===null){
					 that.question[0].ques='对'
					 that.question[0].id='对'
					 that.question[1].ques='错'
					 that.question[1].id='错'
					 that.question[2].ques=''
					 that.question[3].ques=''
					 that.type='判断'
					 // console.log(that.question[0].id)
				}
				if(that.quesiton_tot[i].pic_image===null){
					that.ima=false
				}else{
					 that.imag=that.quesiton_tot[i].pic_image
					 that.ima=true
				}
			},
			
			font_size5(){
				this.font_size=50
				
			},
			font_size4(){
				this.font_size=45
			},
			font_size3(){
				this.font_size=40
			},
			font_size2(){
				this.font_size=35
			},
			font_size0(){
				this.font_size=30
			},
			pop(){
				if(this.box===false){
					this.box=true;
					this.jinnang=false;
					this.protect=true
				}else {
					this.box=false;
					this.jinnang=true;
					this.protect=false
				}
			},
			fons(){
				if(this.size==false){
					this.size=true;
					this.jinnang=false;
					this.protect=true
				}else {
					this.size=false;
					this.jinnang=true;
					this.protect=false
				}
			
			},
			stop(){
				
			},
			cunchu(){
				uni.request({
					url: 'http://jiakao.maiwd.cn/api/mock_record/add',
					method: "POST",
					header: {
						'content-type': 'application/json' ,//自定义请求头信息
						"token": '58d7014b-16d0-48c4-b959-e71e0ae17c7d',
					},
					data: {
						mock_id:1,
						user_answer:that.answer_1,
						question_id:211
					},
					success: (res) => {
						// console.log(JSON.stringify(res.data))
					
					}
				})
			},
			shoucang(){
				let i=this.qus
				if(this.shoucang1==true){
					this.shoucang1=false
				}else this.shoucang1=true
				if(this.shoucang1==true){
					uni.request({
						url:'http://jiakao.maiwd.cn/api/user_question_collect/collect',
						method:"POST",
						data:{
							token:getApp().globalData.token1,
							question_id:this.quesiton_tot[i].id
						},
						success:(res)=>{
							// console.log('4')
							}
					})
				}else{
					uni.request({
						url:'http://jiakao.maiwd.cn/api/user_question_collect/cancel_collect',
						method:"POST",
						data:{
							token:getApp().globalData.token1,
							question_id:this.quesiton_tot[i].id
						},
						success:(res)=>{
							// console.log('5')
							}
					})
				}
			},
			change(){
				this.none=this.bgc;
				this.bgc=this.ccc;
				this.ccc=this.none;
				
				this.text=this.text1;
				this.text1=this.text2;
				this.text2=this.text;
				
				if(this.jinnang==true){
					this.jinnang=false
				}else this.jinnang=true
				
				if(this.jiyi==false){
					this.jiyi=true
				}else this.jiyi=false
			
			},
			con(){
				uni.switchTab({
				url: '/pages/index/index'
				});
			},
			countTime() {
				//获取当前时间  
				var date = new Date();
				var now = date.getTime();
				var leftTime = this.time - now;
				if (leftTime <= 0) {
					this.countdown_time = "已结束"
					return
				}
				var d, h, m, s;
				if (leftTime >= 0) {
					  // d = Math.floor(leftTime/1000/60/60/24); 
					h = Math.floor(leftTime / 1000 / 60 / 60 % 24);
					m = Math.floor(leftTime / 1000 / 60 % 60);
					s = Math.floor(leftTime / 1000 % 60);
				}
				//将倒计时赋值到view中  
				this.countdown_time = `倒计时${m}分${s}秒`
				//递归每秒调用countTime方法，显示动态时间效果  
				var timers = setTimeout(this.countTime, 1000);
			},
			
			danxuan_1(){
			
				uni.request({
					url:'http://jiakao.maiwd.cn/api/question/random_ten',
					method:"POST",
					header: {
						'content-type': 'application/json' ,//自定义请求头信息
						"token": '58d7014b-16d0-48c4-b959-e71e0ae17c7d',
					},
					data:{
						eq_car_type:1,
						eq_subject:1,
						eq_question_type:1,
						limit:5
					},
					success:(res)=>{
						// console.log(JSON.stringify(res.data))
						let i = that.qus
						that.quesiton_tot=res.data.data
						that.topic=that.quesiton_tot[i].question_content
						// console.log(JSON.stringify(that.quesiton_tot[i]))
						 that.question[0].ques=that.quesiton_tot[i].option1
						 that.question[0].id='A'
						 that.question[1].ques=that.quesiton_tot[i].option2
						 that.question[1].id='B'
						 that.question[2].ques=that.quesiton_tot[i].option3
						 that.question[2].id='C'
						 that.question[3].ques=that.quesiton_tot[i].option4
						 that.question[3].id='D'
						 that.type='单选'			
						 if(that.quesiton_tot[i].pic_image===null){
							 that.ima=false
						 }else{
							 that.imag=that.quesiton_tot[i].pic_image
							 that.ima=true
						 }
						that.fangfa()
						that.a[i].answer1=that.quesiton_tot[i].answer
						 // console.log('eqwewq'+JSON.stringify(that.a))
						 // console.log(JSON.stringify(that.quesiton_tot[i]))
						 // console.log(JSON.stringify(that.question_tot[i]))
						 // console.log(that.quesiton_tot[i].pic_image)
					}
				})
				
			},
		    duoxuan_1(){
		    	uni.request({
		    		url:'http://jiakao.maiwd.cn/api/question/random_ten',
		    		method:"POST",
		    				header: {
		    							'content-type': 'application/json' ,//自定义请求头信息
		    							"token": '58d7014b-16d0-48c4-b959-e71e0ae17c7d',
		    						},			
		    		data:{
		    			// token:getApp().globalData.token1,
		    			eq_car_type:getApp().globalData.car_type,
		    			eq_subject:getApp().globalData.subject,
		    			eq_question_type:3,
		    			limit:40
		    		},
		    		success:(res)=>{
		    			var ddd=res.data.data
		    			that.quesiton_tot=that.quesiton_tot.concat(ddd)
		    			// console.log(JSON.stringify(that.quesiton_tot))
		    			// console.log(JSON.stringify(res.data.data))
		    			// console.log(that.quesiton_tot)
		    		}
		    	})
		    			   
		    },
				
		    returnque(i){
				// console.log()
				that.quesiton_now=i+1
				that.qus=i
				that.topic=that.quesiton_tot[i].question_content
				that.question[0].ques=that.quesiton_tot[i].option1
				that.question[0].id='A'
				that.question[1].ques=that.quesiton_tot[i].option2
				that.question[1].id='B'
				that.question[2].ques=that.quesiton_tot[i].option3
				that.question[2].id='C'
				that.question[3].ques=that.quesiton_tot[i].option4
				that.question[3].id='D'
				that.a[i].answer1=that.quesiton_tot[i].answer
				if(that.question[3].ques===null){
					 that.question[0].ques='对'
					 that.question[0].id='对'
					 that.question[1].ques='错'
					 that.question[1].id='错'
					 that.question[2].ques=''
					 that.question[3].ques=''
					 that.type='判断'
					 // console.log(that.question[0].id)
				}
				if(that.quesiton_tot[i].pic_image===null){
					that.ima=false
				}else{
					 that.imag=that.quesiton_tot[i].pic_image
					 that.ima=true
				}
			},
		    fangfa(){
				for(var i=0;i<100;i++){
						that.a.push({
							id:i,
							answer:'',
							answer1:'',
						})
				}
			}
		},
		mounted(){
			this.countTime()
		},
		onLoad(){
			that=this
			// console.log(getApp().globalData.token1)
			// console.log(that.question[0].id);
			var date = new Date();
			var now = date.getTime();
			that.time=now+2700000
			
			this.danxuan_1()
			this.duoxuan_1()
		},
		data() {
			return {
				startData: {
				  clientX: 0,
				  clientY: 0
				},
				a:[],
				duiques:0,
				cuoques:0,
				num:[],
				answer_1:'',
				qus:0,
				ima:false,
				imag:'',
				protect:false,
				shoucang1:false,
				danxuan:1,
				countdown_time: '倒计时00分00秒',
				time:'',
				eq_question_type:1,
				quesion_1:'',
				quesiton_tot:[],
				bgc:'white',
				ccc:'#2C5DFE',
				none:'',
				chan:true,
				pages:17,
				font_size:35,
				size:false,
				topic:'',
				type:'',
				jinnang:true,
				box:false,
				quesiton_now:1,
				quesiton_total:'/100',
				question:[{
					ques:'',
					id:'',
				},{
					ques:'',
					id:'',
				},{
					ques:'',
					id:'',
				},{
					ques:'',
					id:'',
				}]
			}
		},
		
	}
</script>

<style scoped>
	.size{
		z-index: 200;
	}
	.size-line{
		width: 120rpx;
		height: 5rpx;
		background-color: #C8C7CC;
		margin: 8rpx -10rpx;
	}
	.size_cir1{
		height: 30rpx;
		width: 30rpx;
		border-radius: 50%;
		background-color: #2C5DFE;
		z-index: 10;
		margin-top: -5rpx;
	}
	.size_cir{
		height: 20rpx;
		width: 20rpx;
		border-radius: 50%;
		background-color: #000000;
		z-index: 10;
	}
	.size_bottom_text{
		display: flex;
		justify-content: space-around;
		margin: 30rpx;
	}
	.line_5{
		width: 15%;
		height: 5rpx;
		margin-left: 42.5%;
		background-color: #0000FF;
	}
	.bottom_topic{
		text-align: center;
		font-size: 35rpx;
		padding: 30rpx 0 20rpx;
	}
	.size_bottom{
		position: fixed;
		bottom: 0;
		width: 100%;
		height: 350rpx;
		background-color: white;
		z-index: 200;
	}
	.protect{
			width:100% ;
			height: 1700rpx;
			background:rgba(0, 0, 0, 0.4);
			position:fixed;
			top: 0rpx;
			/* margin-top: -800rpx; */
			overflow: hidden;
			z-index: 10;
	}
	.circulal{
		width: 50rpx;
		height: 50rpx;
		line-height: 50rpx;
		border-radius: 50%;
		background-color: #DCFFDA;
		color: #0CAF00;
		text-align: center;
        margin: 30rpx 20rpx 1px;
		display: inline-block;
	}
	.circulal_cuo{
		width: 50rpx;
		height: 50rpx;
		line-height: 50rpx;
		border-radius: 50%;
		background-color: #FFDCDC;
		color: #FF0000;
		text-align: center;
	    margin: 30rpx 20rpx 1px;
		display: inline-block;
	}
	.circulal_kong{
		width: 50rpx;
		height: 50rpx;
		line-height: 50rpx;
		border-radius: 50%;
		background-color: #ECECEC;
		color: #888888;
		text-align: center;
	    margin: 30rpx 20rpx 1px;
		display: inline-block;
	}
	.footer_pop{
		height: 500rpx;
		width: 100%;
		background-color:white;
		background-color: white;
		/* display:flex; */
		/* flex-wrap: wrap; */
	}
	.footer_question{
		display: flex;
		margin-top:20rpx ;
		margin-left: 65rpx;
		font-size: 33rpx;
	}
	.yon{
		margin-top: 20rpx;
		display: flex;
		margin-left: 75rpx;
		font-size: 35rpx;
	}
	.share{
		margin-top: 20rpx;
		display: flex;
		margin-left:75rpx;
	}
	.footer_text{
		margin-top: 6rpx;
		margin-left: 10rpx;
		font-size: 30rpx;
	}
	.collection{
		padding-top: 20rpx;
		display: flex;
		margin-left: 30rpx;
	}
	.footer_photo{
		width: 40rpx;
		margin-top: 5rpx;
	}
	.line{
		width: 100%;
		height: 7rpx;
		background-color: #00000029
	}
	.footer{
		position: fixed;
		bottom: 0;
		/* height: 100rpx; */
		width: 100%;
		background-color: white;
		z-index:100;
		overflow:scroll
	}
	
	.answer_text{
		margin-left: 30rpx;
	}
	.answer_pad{
		margin-left: 30rpx;
		display: flex;
		/* position: absolute; */
		
	}
	.answer{
		width: 90%;
		margin-top: 30rpx;
		margin-left: 5%;
		/* height: 90rpx; */
		background-color: #EBEBEB;
		border-radius: 10rpx;
		/* padding: 10rpx 0; */
		/* vertical-align: middle; */
		/* z-index: 10; */
	}
	.topic{
		margin-top: 30rpx;
		margin-left: 5%;
		font-size: 33rpx;
		font-weight: 600;
	}
	.top_4_wai{
		height: 55rpx;
		line-height: 55rpx;
		width: 150rpx;
		border-radius: 30rpx;
		background-color: #2C5DFE;
		margin-left: 20rpx;
		text-align: center;
		line-height: 50rpx;
		color: white;
		font-size: 30rpx;
		font-weight: 500;
		margin-top: 7rpx;
		display: flex;
		text-align: center;
	}
	.top_text{
		/* margin-top: 5rpx; */
		margin-left: 10rpx;
	}
	.top_3_wai{
		height: 55rpx;
		line-height: 55rpx;
		width: 150rpx;
		border-radius: 30rpx;
		background-color: #2C5DFE;
		margin-left: 140rpx;
		text-align: center;
		line-height: 50rpx;
		color: white;
		font-size: 30rpx;
		font-weight: 500;
		margin-top: 7rpx;
		display: flex;
		text-align: center;
	}
	.top_photo{
		margin-top: 13rpx;
		margin-left: 20rpx;
		width: 30rpx;
	}
	.top_2_wai{
		height: 55rpx;
		line-height: 55rpx;
		width: 120rpx;
		border-radius: 30rpx;
		background-color: #2C5DFE;
		margin-left: 20rpx;
		text-align: center;
		line-height: 50rpx;
		color: white;
		font-size: 35rpx;
		font-weight: 500;
		margin-top: 7rpx;
		text-align: center;
	}
	.quesiton_total{
		color:#AAAAAA ;
	}
	.quesiton_now{

	}
	.top_1{
		margin-left: 20rpx;
		display: flex;
		font-size: 45rpx;
	}
	.top{
		margin-top: 20rpx;
		display: flex;
	}
	
	.header_header{
		width: 100%;
		height: 133rpx;
		background-color: #F8F8F8;
	
	}
	/* 收藏 */
	
	.answer_text{
		height: 50rpx;
		line-height: 50rpx;
	}
	
	.answer_num{
		width: 50rpx;
		height: 50rpx;
		line-height: 50rpx;
		text-align: center;
		border-radius: 50%;
		/* background-color: black; */
	}
	
	

	
	
	
</style>
