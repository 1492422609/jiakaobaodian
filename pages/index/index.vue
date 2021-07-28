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
				<swiper-item class="swiper-item">
					<scroll-view scroll-y style="height: 100%;width: 100%;">
						<view class="page-box">
							<view>
								我是内容二
							</view>
							<view>
								我是内容二
							</view>
							<view>
								我是内容二
							</view>
							<view>
								我是内容二
							</view>
							<view>
								我是内容二
							</view>
							<view>
								我是内容二
							</view>
							<view>
								我是内容二
							</view>
							<view>
								我是内容二
							</view>
							<view>
								我是内容二
							</view>
							<view>
								我是内容二
							</view>
							<view>
								我是内容二
							</view>
							<view>
								我是内容二
							</view>
							<view>
								我是内容二
							</view>
							<view>
								我是内容二
							</view>
							<view>
								我是内容二
							</view>
							<view>
								我是内容二
							</view>
							<view>
								我是内容二
							</view>
							<view>
								我是内容二
							</view>
							<view>
								我是内容二
							</view>
							<view>
								我是内容二
							</view>
							<view>
								我是内容二
							</view>
							<view>
								我是内容二
							</view>
							<view>
								我是内容二
							</view>
							<view>
								我是内容二
							</view>
							<view>
								我是内容二
							</view>
							<view>
								我是内容二
							</view>
							<view>
								我是内容二
							</view>
							<view>
								我是内容二
							</view>
							<view>
								我是内容二
							</view>
							<view>
								我是内容二
							</view>
							<view>
								我是内容二
							</view>
							<view>
								我是内容二
							</view>
							<view>
								我是内容二
							</view>
							<view>
								我是内容二
							</view>
						</view>
					</scroll-view>
				</swiper-item>
				<swiper-item class="swiper-item">
					<scroll-view scroll-y style="height: 100%;width: 100%;">
						<view class="page-box">
							我是内容三
						</view>
					</scroll-view>
				</swiper-item>
				<swiper-item class="swiper-item">
					<scroll-view scroll-y style="height: 100%;width: 100%;">
						<view class="page-box">
							我是内容四
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
								<label class="radio" :checked="bianhao===1" @click="radio('1')">
									<radio value="1" /><text></text>
								</label>
							</view>
							<view class="pop_bottom_2">
								<image src="https://z3.ax1x.com/2021/07/22/W0QU58.png" mode="widthFix" class="pop_bottom_photo"></image>
								<view class="pop_bottom_text">
									小车C1/C1/C3
								</view>
								<label class="radio" :checked="bianhao===1" @click="radio('1')">
									<radio value="1" /><text></text>
								</label>
							</view>
							<view class="pop_bottom_2">
								<image src="https://z3.ax1x.com/2021/07/22/W0QU58.png" mode="widthFix" class="pop_bottom_photo"></image>
								<view class="pop_bottom_text">
									小车C1/C1/C3
								</view>
								<label class="radio" :checked="bianhao===1" @click="radio('1')">
									<radio value="1" /><text></text>
								</label>
							</view>
							<view class="pop_bottom_2">
								<image src="https://z3.ax1x.com/2021/07/22/W0QU58.png" mode="widthFix" class="pop_bottom_photo"></image>
								<view class="pop_bottom_text">
									小车C1/C1/C3
								</view>
								<label class="radio" :checked="bianhao===1" @click="radio('1')">
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
				pop:false,
				bianhao:'1',
				// 内容
				current: 0,
				// 下标
				swiperCurrent: 0,
				// 偏移量
				dx: 0,
			}
		},
		onLoad() {

		},
		methods: {
			radio(e){
				this.bianhao=e;
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
				console.log(current)
				this.swiperCurrent = current;
				this.current = current;
			}
		}
	}
</script>

<style>
	.swiper-box{
		height: 600rpx;
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
		width: 107%;
		margin-top: 30rpx;
		/* margin-left:10% ; */
		height: 10rpx;
		border-radius: 20rpx;
		background-color: #F1F1F1
	}
	.radio{
		margin-left: 100rpx;
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
		justify-content: center;
		align-items: center;
	}
	.pop_bottom_1{
		/* margin-top: 20rpx; */
		display: flex;
		justify-content: center;
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
		font-size: 5rpx
	}
	.footer_photo{
		margin-left: 16rpx;
		margin-top: 20rpx;
		width: 350rpx;
		border-radius: 20rpx;
	}
	.line{
		width: 100%;
		height: 50rpx;
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
