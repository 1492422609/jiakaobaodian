<template>
	<view>
		<view class="header">
			<view class="header_bg">
				<image src="https://z3.ax1x.com/2021/07/27/WhqKdU.png" mode="widthFix" class="header_photo"></image>
			</view>
		</view>
		<view class="middle">
			<view class="middle_left">
				<image src="https://z3.ax1x.com/2021/07/26/WWcPET.png" mode="widthFix" class="middle_photo"></image>
				<view style="text-align: center;">
					芜湖起飞wuhu
				</view>
			</view>
			<view class="middle_right">
				<view class="middle_right_left">
					<view style="color:#FF0000 ;" class="quesiton_num">
						11
					</view>
					<view class="quesiton_text" style="margin-left: 2rpx;">
						错题数
					</view>
				</view>
				<view class="middle_right_left" style=";">
					<view style="color:#2C5DFE;" class="quesiton_num">
						0
					</view>
					<view class="quesiton_text">
						未做题数
					</view>
				</view>
			</view>
		</view>
	    <view class="wrong">
			<view style="display: flex;padding-top: 10rpx;">
				<view class="logo">
					<image src="https://z3.ax1x.com/2021/07/30/WqO0Nd.png" mode="widthFix" class="log"></image>
				</view>
				<view class="logo_text">
					本次错题
				</view>
			</view>
		</view>
	    <view class="line"></view>
	    <view class="bottom">
	    	<view class="button">
	    		返回首页
	    	</view>
	    </view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style scoped>
	.button{
		width: 60%;
		height: 100rxpx;
		line-height: 100rpx;
		border-radius: 10rpx;
		font-size: 35rpx;
		text-align: center;
		margin-top: 80rpx;
		margin-left: 20%;
		color: white;
		background-color: #0000FF;
	}
	.line{
		width: 100%;
		height: 2rpx;
		background-color:#00000010 ;
	}
	.logo_text{
		text-align: center;
		font-size: 35rpx;
		margin-top: -15rpx;
		margin-left: 20rpx;
	}
	.log{
		width: 50rpx;

	}
	.logo{
		margin-left: 35%;
	}
	.wrong{
		height: 125rpx;
		line-height: 125rpx;
		width: 100%;
		/* text-align: center; */
		/* display: flex; */
	}
	.quesiton_text{
	    margin-top: 30rpx;
		margin-left: -10rpx;
		width: 150%;
	}
	.quesiton_num{
		font-size: 50rpx;
		text-align: center;
	}
	.middle_right_left{
		margin-top: 30rpx;
		margin-left: 100rpx;
		width: 50%;
	}
	.middle_right{
		width: 50%;
		display: flex;
		margin-top: 70rpx;
		margin-left: -80rpx;
	}
	.middle_left{
		width: 50%;
	}
	.middle_photo{
		width: 150rpx;
		margin-top: 30rpx;
		margin-left: 100rpx;
	}
	.middle{
		width: 100%;
		height: 300rpx;
		background-color:#F0F7FF ;
		display: flex;
		/* justify-content: space-between; */
		
	}
	.header_photo{
		width: 350rpx;
		margin-top: 40rpx;
	}
	.header_bg{
		text-align: center;
		position: relative;
		background-image: url('https://z3.ax1x.com/2021/07/27/W4CLiq.png');
		background-color:#F0F7FF; 
		width: 100%;
		height: 400rpx;
		background-repeat: no-repeat;
		background-size: cover;
	}
</style>
