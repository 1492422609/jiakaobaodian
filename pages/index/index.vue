<template>
	<view>
		<view>
			<image src="https://z3.ax1x.com/2021/07/23/Wrk5g1.png" mode="widthFix" class="Carousel_chart"></image>
			<view class="">
				<u-tabs-swiper ref="tabs" :list="list" :is-scroll="false" bar-height="6" :current="current" @change="change"> </u-tabs-swiper>
			</view>
			<view class="line"></view>
			<swiper class="swiper-box" :current="swiperCurrent" @transition="transition" @animationfinish="animationfinish">
				<swiper-item class="swiper-item">
					<scroll-view scroll-y style="height: 100%;width: 100%;">
						<view class="second">
							<view class="second_left">
								<view class="second_left_1">
									<navigator url="../question_bank/question_bank">
										<image src="https://z3.ax1x.com/2021/07/23/WrtZRI.png" mode="" class="second_left_photo">
										</image>
										<view class="second_left_text">
											题库学习
										</view>
									</navigator>
								</view>
								<view class="second_left_1">
									<navigator url="../collection/collection">
										<image src="https://z3.ax1x.com/2021/07/23/WrLCd0.png" mode="" class="second_left_photo">
										</image>
										<view class="second_left_text">
											错题收藏
										</view>
									</navigator>
								</view>
								<view class="second_left_1">
									<navigator url="../instructions/instructions">
										<image src="https://z3.ax1x.com/2021/07/23/WrL9Zq.png" mode="" class="second_left_photo">
										</image>
										<view class="second_left_text">
											学前须知
										</view>
									</navigator>
								</view>
							</view>
							<view class="second_middle">
								<navigator url="../mock/mock">
									<view>
										<image src="https://z3.ax1x.com/2021/07/23/WrwKUO.gif" mode="" class="round">
										<view class="test">
											考试模拟
										</view>
										</image>
										<image src="https://z3.ax1x.com/2021/07/23/WrwuVK.png" mode="widthFix" class="paper"></image>	
									</view>
								</navigator>			
							</view>
							<view class="second_right">
								<view class="second_left_1">
									<navigator url="../library/library">
									<image src="https://z3.ax1x.com/2021/07/23/WrLPoV.png" mode="" class="second_left_photo">
									</image>
									<view class="second_left_text2">
										<image src="https://z3.ax1x.com/2021/07/23/WsPFx0.png" mode="widthFix" class="vip"></image>
										技巧学习
									</view>
									</navigator>
								</view>
								<view class="second_left_1">
									<navigator url="../classify/classify">
										<image src="https://z3.ax1x.com/2021/07/23/WrLSLn.png" mode="" class="second_left_photo">
										</image>
										<view class="second_left_text2">
											<image src="https://z3.ax1x.com/2021/07/23/WsPFx0.png" mode="widthFix" class="vip"></image>
											专项练习
										</view>
									</navigator>						
								</view>
								<view class="second_left_1">
									<navigator url="../wrong_question/wrong_question">
									<image src="https://z3.ax1x.com/2021/07/23/WrLFiT.png" mode="" class="second_left_photo">
									</image>
									<view class="second_left_text2">
										<image src="https://z3.ax1x.com/2021/07/23/WsPFx0.png" mode="widthFix" class="vip"></image>
										高频题库
									</view>
									</navigator>
								</view>
							</view>
						</view>
								  
					</scroll-view>
				</swiper-item>
				<swiper-item class="swiper-item">
					<scroll-view scroll-y style="height: 100%;width: 100%;">
						<view class="video_head">
							<view class="video_head_left">
								<image src="https://z3.ax1x.com/2021/07/28/WoQijg.png" mode="widthFix" style="width: 30rpx;margin-right: 15rpx;margin-bottom: -5rpx;"></image>
								视频教程
							</view>
							<view class="video_head_right">
								换车型
							</view>
						</view>
						<view class="video_middle">
							<view class="video_middle_1" v-for="sk in skill">
								<image src="https://z3.ax1x.com/2021/07/28/Wo3zqg.png" mode="widthFix"style="width: 320rpx;border-radius: 20rpx"></image>
							    <view style="margin-top: 5rpx;">
							    	{{sk.name}}
							    </view>
							</view>
						</view>
					</scroll-view>
				</swiper-item>
				<swiper-item class="swiper-item">
					<scroll-view scroll-y style="height: 100%;width: 100%;">
						<view class="video_head">
							<view class="video_head_left">
								<image src="https://z3.ax1x.com/2021/07/28/WoQijg.png" mode="widthFix" style="width: 30rpx;margin-right: 15rpx;margin-bottom: -5rpx;"></image>
								视频教程
							</view>
							<view class="video_head_right">
								换车型
							</view>
						</view>
						<view class="video_middle">
							<view class="video_middle_1" v-for="sk in skill">
								<image src="https://z3.ax1x.com/2021/07/28/Wo3zqg.png" mode="widthFix"style="width: 320rpx;border-radius: 20rpx"></image>
							    <view style="margin-top: 5rpx;">
							    	{{sk.name}}
							    </view>
							</view>
						</view>
					</scroll-view>
				</swiper-item>
				<swiper-item class="swiper-item">
					<scroll-view scroll-y style="height: 100%;width: 100%;">
						<view class="second">
							<view class="second_left">
								<view class="second_left_1">
									<navigator url="../question_bank/question_bank">
										<image src="https://z3.ax1x.com/2021/07/23/WrtZRI.png" mode="" class="second_left_photo">
										</image>
										<view class="second_left_text">
											题库学习
										</view>
									</navigator>
								</view>
								<view class="second_left_1">
									<navigator url="../collection/collection">
										<image src="https://z3.ax1x.com/2021/07/23/WrLCd0.png" mode="" class="second_left_photo">
										</image>
										<view class="second_left_text">
											错题收藏
										</view>
									</navigator>
								</view>
								<view class="second_left_1">
									<navigator url="../instructions/instructions">
										<image src="https://z3.ax1x.com/2021/07/23/WrL9Zq.png" mode="" class="second_left_photo">
										</image>
										<view class="second_left_text">
											学前须知
										</view>
									</navigator>
								</view>
							</view>
							<view class="second_middle">
								<navigator url="../mock/mock">
									<view>
										<image src="https://z3.ax1x.com/2021/07/23/WrwKUO.gif" mode="" class="round">
										<view class="test">
											考试模拟
										</view>
										</image>
										<image src="https://z3.ax1x.com/2021/07/23/WrwuVK.png" mode="widthFix" class="paper"></image>	
									</view>
								</navigator>			
							</view>
							<view class="second_right">
								<view class="second_left_1">
									<navigator url="../library/library">
									<image src="https://z3.ax1x.com/2021/07/23/WrLPoV.png" mode="" class="second_left_photo">
									</image>
									<view class="second_left_text2">
										<image src="https://z3.ax1x.com/2021/07/23/WsPFx0.png" mode="widthFix" class="vip"></image>
										技巧学习
									</view>
									</navigator>
								</view>
								<view class="second_left_1">
									<navigator url="../classify/classify">
										<image src="https://z3.ax1x.com/2021/07/23/WrLSLn.png" mode="" class="second_left_photo">
										</image>
										<view class="second_left_text2">
											<image src="https://z3.ax1x.com/2021/07/23/WsPFx0.png" mode="widthFix" class="vip"></image>
											专项练习
										</view>
									</navigator>						
								</view>
								<view class="second_left_1">
									<navigator url="../library/library">
									<image src="https://z3.ax1x.com/2021/07/23/WrLFiT.png" mode="" class="second_left_photo">
									</image>
									<view class="second_left_text2">
										<image src="https://z3.ax1x.com/2021/07/23/WsPFx0.png" mode="widthFix" class="vip"></image>
										高频题库
									</view>
									</navigator>
								</view>
							</view>
						</view>
					</scroll-view>
				</swiper-item>
			</swiper>
		
			
			<view class="line"></view>
			<view class="footer">
				<view class="footer_1">
					<view class="">
						<image src="https://z3.ax1x.com/2021/07/23/WrIP3R.png" mode="widthFix" class="footer_photo"></image>
						<view class="footer_text">
							专业讲解
						</view>
						<view class="footer_text2">
							讲师进行讲解
						</view>
					</view>
				</view>
				<view class="footer_1">
					<view class="">
						<image src="https://z3.ax1x.com/2021/07/23/WrxsqH.png" mode="widthFix" class="footer_photo"></image>
						<view class="footer_text">
							手机作答
						</view>
						<view class="footer_text2">
							方便、快捷
						</view>
					</view>
				</view>
				<view class="footer_1">
					<view class="">
						<image src="https://z3.ax1x.com/2021/07/23/WrxDMD.png" mode="widthFix" class="footer_photo"></image>
						<view class="footer_text">
							做题进度
						</view>
						<view class="footer_text2">
							查看做题进度
						</view>
					</view>
				</view>
				<view class="footer_1">
					<view class="">
						<image src="https://z3.ax1x.com/2021/07/23/Wrxrse.png" mode="widthFix" class="footer_photo"></image>
						<view class="footer_text">
							技巧介绍
						</view>
						<view class="footer_text2">
							快速记忆试题
						</view>
					</view>
				</view>
			</view>
		    <view class="pop" v-show="pop">
		    	<view class="protect">
		    		<view class="bg_pop">
		    			<image src="https://z3.ax1x.com/2021/07/26/WRtBxe.png" mode="widthFix" class="bg_pop_iamge"></image>
						<view class="pop_top">
								请选择车型
						</view>
						<view class="pop_bottom">
							<view class="pop_bottom_1">
								<image src="https://z3.ax1x.com/2021/07/22/W0QU58.png" mode="widthFix" class="pop_bottom_photo"></image>
								<view class="pop_bottom_text">
									小车C1/C1/C3
								</view>
								<label class="radio" :checked="bianhao==1" @click="radio('1')">
									<radio value="1" /><text></text>
								</label>
							</view>
							<view class="pop_bottom_2">
								<image src="https://z3.ax1x.com/2021/07/31/WXvUoT.png" mode="widthFix" class="pop_bottom_photo"></image>
								<view class="pop_bottom_text">
									货车/A1/B2
								</view>
								<label class="radio" :checked="bianhao==1" @click="radio('2')">
									<radio value="1" /><text></text>
								</label>
							</view>
							<view class="pop_bottom_2">
								<image src="https://z3.ax1x.com/2021/07/31/WXvNwV.png" mode="widthFix" class="pop_bottom_photo"></image>
								<view class="pop_bottom_text">
								    客车A1/A3/B1
								</view>
								<label class="radio" :checked="bianhao==1" @click="radio('3')">
									<radio value="1" /><text></text>
								</label>
							</view>
							<view class="pop_bottom_2">
								<image src="https://z3.ax1x.com/2021/07/31/WXvte0.png" mode="widthFix" class="pop_bottom_photo"></image>
								<view class="pop_bottom_text">
								    摩托车
								</view>
								<label class="radio" :checked="bianhao==1" @click="radio('4')">
									<radio value="1" /><text></text>
								</label>
							</view>
							<view class="pop_line"></view>
							<view class="button" @click="pop1">
								确认选择
							</view>
						</view>
		    		</view>
		    	</view>
		    </view>  
		    <view class="prompt" v-show="prom" @click="prompt">
				<view class="protect">
					<view class="prom_photo">
						<view class="prom_text">
							<view class="prom_text2">
								由于各教练员教学方式不尽相
							</view>
							<view class="prom_text2">
								同请根据本地教练员指导学习
							</view>
						</view>
						<view class="prom_text3">
							我知道了
						</view>
					</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				list: [{
					name: '科目一'
				}, {
					name: '科目二'
				}, {
					name: '科目三',
				}, {
					name: '科目四',
				}],
				skill:[{
					name:'侧方位停车'
				},{
					name:'倒车入库'
				},{
					name:'曲线行驶'
				},{
					name:'直角转弯'
				}],
				pop:true,
				prom:false,
				bianhao:'1',
				// 内容
				current: 0,
				// 下标
				swiperCurrent: 0,
				// 偏移量
				dx: 0,
				timer:null,
			}
		},
		onLoad() {
			uni.request({
				url: 'http://jiakao.maiwd.cn/addons/third/api/getAuthUrl',
				method: "POST",
				header: {
					'content-type': 'application/json' ,//自定义请求头信息
					// "token": getApp().globalData.token1,
				},
				data: {
					url:'http://jiakao.maiwd.cn/api/user/third?platform=wechat',
					platform:'wechat',
				},
				success: (res) => {
					
					var http1=res.data.data
					console.log(JSON.stringify(res.data.data))
					// plus.runtime.openURL(http1)
				   // window.location.href="https://cn.bing.com/"
				}
			})
			
		},
		methods: {
			radio(e){
				this.bianhao=e;
				console.log(this.bianhao)
				getApp().globalData.car_type = this.bianhao
				console.log(getApp().globalData.car_type)
				this.timer = setTimeout( () => {
				    this.pop=false		
				}, 300)
			},
			pop1(){
				this.pop=false;
			},
			// tab栏下标切换
			change(index) {
				this.swiperCurrent = index;
			},
			// tab栏偏移量切换
			transition({ detail: { dx } }) {
				this.$refs.tabs.setDx(dx);
			},
			// tab栏内容切换
			animationfinish({ detail: { current } }) {
				// console.log(current)
				this.swiperCurrent = current;
				this.current = current;
			},
			prompt(){
				if(this.prom===false){
					this.prom=true
				}else this.prom=false	
			}
		}
	}
</script>

<style>
	.prom_text3{
		width: 80%;
		height: 70rpx;
		line-height: 70rpx;
		margin-top: 100rpx;
		margin-left: 10%;
		border-radius: 10rpx;
		color: white;
		background-color: #2C5DFE
	}
	.prom_text2{
		margin-top: 20rpx;
		/* letter-spacing: inherit; */
	}
	.prom_text{
		width: 75%;
		margin-left: 12.5%;
		padding-top: 300rpx;
	}
	.prom_photo{
		width: 70%;
		height: 600rpx;
		/* text-align: center; */
		margin-top: 300rpx;
		margin-left: 15%;
		background-image: url("https://z3.ax1x.com/2021/07/28/Wo29jU.png");
		background-size: cover;
		background-repeat: no-repeat;
		text-align: center;
	}
	.video_middle_1{
		margin-top: 40rpx;
		margin-left: 40rpx;
	}
	.video_middle{
		/* margin-top: 50rpx; */
		display: flex;
		flex-wrap: wrap;
	}
	.video_head{
		display: flex;
		justify-content: space-between;
	}
	.video_head_right{
		margin-top: 30rpx;
		margin-right: 30rpx;
		width: 140rpx;
		height: 45rpx;
		line-height: 50rpx;
		border-radius: 30rpx;
		background-color: #0000FF;
		color: white;
		text-align: center;
	}
	.video_head_left{
		margin-top: 10rpx;
		height: 80rpx;
		line-height: 80rpx;
		margin-left: 30rpx;
	}
	.swiper-box{
		height: 650rpx;
	}
	.button{
		font-size: 35rpx;
		justify-content: center;
		margin-left: 230rpx;
		margin-top: 20rpx;
		color: #2C5DFE;
		font-weight: 600;
	}
	.pop_line{
		width: 147%;
		margin-top: 30rpx;
		/* margin-left:10% ; */
		height: 10rpx;
		border-radius: 20rpx;
		background-color: #F1F1F1
	}
	.radio{
		margin-left: 520rpx;
		position: absolute;
	}
	.pop_bottom_text{
		font-size: 35rpx;
		margin-left: 50rpx;
	}
	.pop_bottom_photo{
		width: 80rpx;
		margin-left: 50rpx;
	}
	.pop_bottom_2{
		margin-top: 30rpx;
		display: flex;
		/* justify-content: center; */
		align-items: center;
	}
	.pop_bottom_1{
		/* margin-top: 20rpx; */
		display: flex;
		/* justify-content: center; */
		align-items: center;
	}
	.pop_bottom{
		margin-top: -550rpx;
		/* z-index: 15; */
		position: absolute;
	}
	.pop_top{
		color: white;
		font-size: 35rpx;
		position: absolute;
		margin-top: -650rpx;
		margin-left: 215rpx;
	}
	.bg_pop_iamge{
		width: 89%
	}
	
	.bg_pop{
		margin-top: 20%;
		margin-left: 10%;
	}
	.protect{
			width:100% ;
			height: 1700rpx;
			background:rgba(0, 0, 0, 0.4);
			position:absolute;
			z-index: 10;
			margin-top: -1500rpx;
			overflow: hidden;
	}
	.vip{
		width: 30rpx;
	}
	.footer{
		display:flex;
		flex-wrap: wrap;
	}
	.footer_text{
		position: absolute;
		margin-top: -130rpx;
		margin-left: 35rpx;
		
	}
	.footer_text2{
		position: absolute;
		margin-top: -85rpx;
		margin-left: 35rpx;
		font-size: 25rpx
	}
	.footer_photo{
		margin-left: 16rpx;
		margin-top: 20rpx;
		width: 350rpx;
		border-radius: 20rpx;
	}
	.line{
		width: 100%;
		height: 30rpx;
		background-color: #F1F1F1;
	}
	.test{
		color: white;
		position: absolute;
		margin-top: -135rpx;
		margin-left: 66rpx;
	}
	.paper{
		position: absolute;
		width: 90rpx;
		margin-top: -235rpx;
		margin-left: 80rpx;
	}
	.round {
		margin-top: 50%;
		margin-left: -17%;
		width: 325rpx;
		height: 325rpx;
		/* background-color: #509AFC; */
		border-radius: 50%;
	}

	.second_left_photo {
		width: 100rpx;
		height: 100rpx;
	}

	.second_left_text {
		/* margin-left:8rpx ; */
		/* text-align: center; */
		margin-left: -8rpx;
	}
	.second_left_text2 {
		/* margin-left:8rpx ; */
		/* text-align: center; */
		margin-left: -18rpx;
	}

	.second_left_1 {
		margin-left: 30%;
		margin-top: 20%;
		margin-bottom: 30rpx;
		justify-content: center;
		align-items: center;
		flex-direction: column;
		/* display: flex; */
	}

	.second_right {
		width: 33%;
	}

	.second_middle {
		justify-content: center;
		width: 33%;
	}

	.second_left {
		width: 33%;
	}

	.second {
		display: flex;
		/* background-color: #0000FF; */
	}

	.subjects {
		display: flex;
	}

	.Carousel_chart {
		width: 90%;
		margin-left: 5%;
		border-radius: 20rpx;
	}
</style>
