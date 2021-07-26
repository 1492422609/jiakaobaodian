<template>
	<view>
		<view class="">
			<view class="row">
				<view class="grads">
					{{grads}}分
				</view>
				<view class="time">
					30分56秒
				</view>
				<view class="time2">
					06月09号
				</view>
				<view style="font-size: 35rpx;margin-left: 25rpx;">
					>
				</view>
			</view>
			<view class="line"></view>
		</view>
	    <view class="">
	    	<view class="row">
	    		<view class="grads">
	    			{{grads}}分
	    		</view>
	    		<view class="time">
	    			30分56秒
	    		</view>
	    		<view class="time2">
	    			06月09号
	    		</view>
	    		<view style="font-size: 35rpx;margin-left: 25rpx;">
	    			>
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
				grads:95,
			}
		},
		methods: {
			
		}
	}
</script>

<style>
	.line{
		width: 100%;
		height: 5rpx;
		background-color: #F1F1F1;
		margin-top: 30rpx;
	}
	.time2{
		font-size: 35rpx;
		margin-left: 130rpx;
		color:#888888 ;
	}
	.time{
		font-size: 35rpx;
		margin-left: 160rpx;
		color:#888888 ;
	}
	.grads{
		color:#0CAF00 ;
		font-size: 35rpx;
		margin-left: 30rpx;
	}
	.row{
		display: flex;
		margin-top: 30rpx;
	}
</style>
