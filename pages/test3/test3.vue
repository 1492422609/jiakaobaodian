<template>
	<view>
		<u-circle-progress active-color="#2979ff" :percent="part">
				<view class="u-progress-content">
					<text class='u-progress-info'>查找中</text>
				</view>
			</u-circle-progress>
	</view>
</template>

<script>
    export default {
       data() {
       	return {
			part:50
       	}
       },
       methods: {
       	   
       }
    }
</script>

<style lang="scss" scoped>
	.u-progress-content {
			display: flex;
			align-items: center;
			justify-content: center;
		}
		
		.u-progress-dot {
			width: 16rpx;
			height: 16rpx;
			border-radius: 50%;
			background-color: #fb9126;
		}
		
		.u-progress-info {
			font-size: 28rpx;
			padding-left: 16rpx;
			letter-spacing: 2rpx
		}
</style>
