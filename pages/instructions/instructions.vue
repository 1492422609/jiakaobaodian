<template>
	<view>
		<view class="header">
			《学前须知》
		</view>
		<view class="video">
			<image src="https://z3.ax1x.com/2021/07/27/W47ihd.png" mode="widthFix" style="width: 90%;margin-left: 5%;margin-top: 30rpx;"></image>
		</view>
		<view class="text">
			line-height 与 font-size 的计算值之差（在 CSS 中成为“行间距”）分为两半，分别加到一个文本行内容的顶部和底部。可以包含这些内容的最小框就是行框。
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
	.text{
		width: 90%;
		margin-left: 5%;
		margin-top: 30rpx;
	}
	.header{
		font-size: 35rpx;
		text-align: center;
		margin-top: 20rpx;
	}
</style>
