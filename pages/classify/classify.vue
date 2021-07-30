<template>
	<view class="total" >
		<view class="row" >
			<view class="row_header">
				<view class="row_1">
					按内容类型
				</view>
				<view class="row_2">
					1200题
				</view>
			</view>
			<view class="row_3" >
				
				<view class="row_text" >
					文字题
				</view>
				<view class="row_text">
					正确题
				</view>
				<view class="row_text">
					正确题
				</view>
			
			</view>
			<view class="line"></view>
		</view>
		<view class="row" >
			<view class="row_header">
				<view class="row_1">
					按内容类型
				</view>
				<view class="row_2">
					1200题
				</view>
			</view>
			<view class="row_3">
				<view class="row_text" >
					文字题
				</view>
				<view class="row_text">
					正确题
				</view>
				<view class="row_text">
					正确题
				</view>
				<view class="row_text">
					正确题
				</view>
			</view>
			<view class="line"></view>
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
	.total{
		width: 750rpx;
		height: 1250rpx;
		background-color: #F2F5FF;
	}
	.line{
		margin-top: 30rpx;
		height: 3rpx;
		width: 90%;
		margin-left: 5%;
		background-color: #CECECE;
	}
	.row_text{
		width: 180rpx;
		height: 80rpx;
		line-height: 80rpx;
		border-radius: 20rpx;
		background-color: white;
		text-align: center;
		font-size: 30rpx;
		font-weight: bold;
		
		margin-top: 40rpx;
		/* argin-left: 50rpx; */
	}
	.row_3{
		padding: 0 50rpx;
		display:grid;
		grid-template-columns: 225rpx 225rpx 225rpx;
	}
	.row_2{
		margin-left:380rpx ;
		font-size: 35rpx;
	}
	.row_1{
		font-size:35rpx ;
		font-weight: 600;
	}
	.row_header{
		display: flex;
		padding-top: 30rpx;
		margin-left: 50rpx;
	}
	
</style>
