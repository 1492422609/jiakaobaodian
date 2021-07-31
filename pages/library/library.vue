<template>
	<view>
		<!-- :class="size=true?'protect':''" @click="fons" -->
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
	    <view class="topic">
	    	{{topic}}
	    </view>
		<view class="answer_total">
			<view class="answer" v-for="(qut,index) in question" :ikey="index" :style="{'font-size':font_size+'rpx'}" @click="questio(index)">
				<view class="answer_pad">
					<!-- <view class="answer_num">
					    {{qut.id}}
					</view>
					<view class="answer_text">
				        {{qut.que}}
					</view> -->
					<view class="">
						{{qut.ques}}
					</view>
				</view>
			</view>				
		</view>
		<view class="jinnang" v-show="jinnang">
			<view class="jinnang_1">
				<image src="https://z3.ax1x.com/2021/07/26/WRqnXT.png" mode="widthFix" style="width: 100rpx;margin-top: 10rpx;"></image>
			    <view style="margin-top: 10rpx;">
			    	小霖锦囊
			    </view>
			</view>
		</view>
	    <view class="footer">
	    	<view class="line"></view>
			<view  style="display: flex; padding-bottom: 20rpx;">
				<view class="collection">
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
						1
					</view>
					<image src="https://z3.ax1x.com/2021/07/26/WWpCnI.png" mode="widthFix" class="footer_photo"  style="margin-left:15rpx;"></image>
					<view style="color: #FF0000;margin-left: 3rpx;">
						0
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
	        	<view class="circulal">
	        		1
	        	</view>
				<view class="circulal">
					1
				</view>
				<view class="circulal">
					1
				</view>
				<view class="circulal">
					1
				</view><view class="circulal">
					1
				</view><view class="circulal">
					1
				</view><view class="circulal">
					1
				</view><view class="circulal">
					1
				</view><view class="circulal">
					1
				</view><view class="circulal">
					1
				</view><view class="circulal">
					1
				</view><view class="circulal">
					1
				</view><view class="circulal">
					1
				</view><view class="circulal">
					1
				</view><view class="circulal">
					1
				</view><view class="circulal">
					1
				</view><view class="circulal">
					1
				</view>
				
	        </view>
		</view>
	    <view class="size" v-show="size">
	    	<view @click="fons" >
	    		<view class="size_bottom" @click.stop="stop">
	    			<view>
	    				<view class="bottom_topic">
	    					字体大小设置
	    				</view>
	    				<view class="line_5"></view>
	    			</view>
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
</template>

<script>
	export default {
		methods: {
			questio(index){
				this.quesiton_now=this.quesiton_now+1
				var that=this
				console.log(index);
				this.pages=this.pages+1;
				// console.log(this.pages)
				uni.request({
					url:'http://jiakao.maiwd.cn/api/question/index',
					method:"POST",
					data:{
						page:this.pages,
						limit:10,
						token:'5rew5',
						eq_car_type:1,
						eq_subject:1,
					},
					success:(res)=>{
						// zzconsole.log(res.data.data.data[5].question_type)
						that.topic=(res.data.data.data[3].question_content)
						 that.question[0].ques=res.data.data.data[3].option1
						 that.question[1].ques=res.data.data.data[3].option2
						 that.question[2].ques=res.data.data.data[3].option3
						 that.question[3].ques=res.data.data.data[3].option4
						 if(res.data.data.data[5].question_type==1){
							 that.type='单选'			
						 }else if(res.data.data.data[5].question_type==1){
							 that.type='多选'	
						 }else{
							 that.type='判断'
						 }
					}
				})
			
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
				}else {
					this.box=false;
					this.jinnang=true;
				}
			},
			fons(){
				if(this.size==false){
					this.size=true;
					this.jinnang=false;
				}else {
					this.size=false;
					this.jinnang=true;
				}
			},
			stop(){
				
			}
		},
		onLoad(){
			var that=this;
			// console.log(that.question[0].id);
			uni.request({
				url:'http://jiakao.maiwd.cn/api/question/index',
				method:"POST",
				data:{
					page:this.pages,
					limit:10,
					token:'5rew5',
					eq_car_type:1,
					eq_subject:1,
				},
				success:(res)=>{
					// zzconsole.log(res.data.data.data[5].question_type)
					that.topic=(res.data.data.data[3].question_content)
					 that.question[0].ques=res.data.data.data[3].option1
					 that.question[1].ques=res.data.data.data[3].option2
					 that.question[2].ques=res.data.data.data[3].option3
					 that.question[3].ques=res.data.data.data[3].option4
					 if(res.data.data.data[5].question_type==1){
						 that.type='单选'			
					 }else if(res.data.data.data[5].question_type==1){
						 that.type='多选'	
					 }else{
						 that.type='判断'
					 }
				}
			})
		},
		data() {
			return {
				pages:5,
				font_size1:30,
				font_size:40,
				size:false,
				topic:'',
				type:'',
				jinnang:true,
				box:false,
				quesiton_now:1,
				quesiton_total:'/10',
				question:[{
					ques:''
				},{
					ques:''
				},{
					ques:''
				},{
					ques:''
				}]
			}
		},
		
	}
</script>

<style scoped>
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
	}
	.protect{
			width:100% ;
			/* height: 1700rpx; */
			background:rgba(0, 0, 0, 0.4);
			position:absolute;
			z-index: 10;
			/* margin-top: -800rpx; */
			overflow: hidden;
			z-index: 500;
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
		margin-left: 75rpx;
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
		background-color: white
	}
	.jinnang{
		position: absolute;
		background-color: #2C5DFE;
		width: 150rpx;
		height: 180rpx;
		margin-left: 550rpx;
		margin-top: 200rpx;
		border-radius: 30rpx;
		color: white;
		text-align: center;
	}
	.answer_text{
		margin-left: 30rpx;
	}
	.answer_pad{
		margin-left: 30rpx;
		display: flex;
		/* position: absolute; */
		padding: 20rpx;
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
</style>
