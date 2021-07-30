<template>
	<view>
		<view class="header">
			<view class="header_bg">
				<image src="https://z3.ax1x.com/2021/07/27/WhqKdU.png" mode="widthFix" class="header_photo"></image>
			</view>
			<view class="header_grades">
				95
			</view>
			<view class="header_qualified">
				成绩合格
			</view>
		</view>
		<view class="middle">
			<view class="middle_1" v-for="item in list">
				<view  style="display: flex;justify-content: space-between;padding: 0 60rpx;">
					<view class="middle_left">
						<view class="num">
							{{item.id}}
						</view>
						<view style="margin-left: 15rpx;">
							<view style="font-size: 35rpx;">
								{{item.name}}
							</view>
							<view style="color:#888888 ;margin-top: 10rpx;">
								错误率{{item.percent}}%
							</view>
						</view>
					</view>
					<view class="middle_right">
						<view style="color: #888888;font-size: 40rpx;">
							{{item.percent}}
							<image src="https://z3.ax1x.com/2021/07/27/W4crcQ.png" mode="widthFix" style="width: 18rpx;margin-left: 30rpx;"></image>
						</view>
					</view>
				</view>
				<view class="line"></view>
			</view>
			
		</view>
	
	</view>
</template>

<script>
	export default {
		data() {
			return {
				list:[{
					id:'1',
					name:'全部试题',
					percent:'5'
				},{
					id:'2',
					name:'单选题',
					percent:'0'
				}]
			}
		},
		methods: {
			
		}
	}
</script>

<style>
	.line{
		margin-top:20rpx ;
		width: 95%;
		margin-left: 2.5%;
		height: 3rpx;
		background-color:#F2F5FF
	}
	.num{
		font-size: 35rpx;
		width: 50rpx;
		height: 50rpx;
		border-radius: 50%;
		background-color: #2C5DFE;
		text-align: center;
		color: white;
		/* margin-left: 30rpx; */
	}
	.middle_left{
		display: flex;
	}
	.middle_1{
		margin-top: 30rpx;
	}
	.middle{
		margin-top:100rpx
	}
	.header_qualified{
		position: relative;
		/* margin-left: 40%; */
		margin-top: 35rpx;
		font-size: 30rpx;
		color: white;
		text-align: center;
	}
	.header_grades{
		position: relative;
		/* margin-left: 43%; */
		margin-top: -250rpx;
		font-size: 90rpx;
		color: #2CC020;
		text-align: center;
	}
	.header_photo{
		width: 350rpx;
		margin-top: 40rpx;
	}
	.header_bg{
		text-align: center;
		position: relative;
		background-image: url('https://z3.ax1x.com/2021/07/27/W4CLiq.png');
		width: 100%;
		height: 400rpx;
		background-repeat: no-repeat;
		background-size: cover;
	}
</style>
<!-- <image src="https://z3.ax1x.com/2021/07/27/W4CLiq.png" mode="widthFix" style="width: 100%;"></image> -->