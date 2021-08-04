<template>
	<view>
		<view class="protect">
			<view class="box1">
				<view class="box_title">
					考试不合格
				</view>
				<view class="box_title2">
					您已答错11题
				</view>
				<view class="box_line">
					<view class="box_box">
						<view class="box_box_text">
							11
						</view>
						<view class="box_box_text2">
							错题数
						</view>
					</view>
					<view class="box_box">
						<view class="box_box_text" style="color:#2C5DFE ;">
							40
						</view>
						<view class="box_box_text2">
							未做题数
						</view>
					</view>
					<view class="box_box">
						<view class="box_box_text" style="color: #2C5DFE;">
							89
						</view>
						<view class="box_box_text2">
							考试成绩
						</view>
					</view>
				</view>
                <view class="box_bottom">
                	<view class="box_bottom_left">
                		<view style="display: flex;">
                			<image src="https://z3.ax1x.com/2021/07/29/WHp9fA.png" mode="widthFix" class="box_bottom_photo"></image>
							<view class="">
								继续答题
							</view>
                		</view>
                	</view>
					<view class="box_bottom_left">
						<view style="display: flex;">
							<image src="https://z3.ax1x.com/2021/07/29/WHppYd.png" mode="widthFix" class="box_bottom_photo"></image>
							<view style="color: #FF0000;">
								现在交卷
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
				
			}
		},
		methods: {
			
		}
	}
</script>

<style>
	.box_bottom_photo{
		width: 45rpx;
		margin-top: 5rpx;
		margin-right: 20rpx;
	}
	.box_bottom_left{
		padding: 60rpx;
		font-size: 38rpx;
	}
	.box_bottom{
		display: flex;
        justify-content: space-between;
		margin-top: 30rpx;
	}
	.box_box_text{
		text-align: center;
		color:#FF0000 ;
		font-size: 50rpx;
		margin-top: 30rpx;
		margin-bottom: 20rpx;
	}
	.box_line{
		display: flex;
		justify-content: space-around;
	}
	.box_title2{
		text-align: center;
		padding: 30rpx;
	}
	.box_title{
		text-align: center;
		color: #FF0000;
		font-size: 40rpx;
		padding-top: 25rpx;
	}
	.box1{
		width: 90%;
		height: 500rpx;
		background-color: white;
		border-radius: 30rpx;
		margin-top: 300rpx;
		margin-left: 5%;
	}
	.protect{
			width:100% ;
			height: 1250rpx;
			background:rgba(0, 0, 0, 0.4);
			position:absolute;
			z-index: 10;
			/* margin-top: -1500rpx; */
			overflow: hidden;
	}
</style>
