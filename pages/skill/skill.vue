<template>
	<view>
		<view class="header">
			技巧学习包含18个技巧，共656道题目，帮助学员快速记忆
		</view>
		<view class="middle">
			<view class="" v-for="skil in skill">
				<view>
					<view class="middle_bg">
						<view class="middle_bulb">
							
						</view>
					{{skil.name}}
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
				skill:[{
					name:'图片题技巧'
				},{
					name:'交通信号技巧'
				},{
					name:'判断技巧'
				},{
					name:'单选题技巧'
				}]
			}
		},
		methods: {
			
		}
	}
</script>

<style>
	.middle_bulb{
		
	}
	.middle_bg{
		margin-top: 30rpx;
		margin-left: 30rpx;
		height: 100rpx;
		/* line-height: 100rpx; */
		width: 200rpx;
		background-image: url(../../static/技巧背景2.png);
		background-size: cover;
		background-repeat: no-repeat;
		text-align: center;
	}
	.middle{
		display:flex;
		flex-wrap: wrap;
	}
	.header{
		font-size: 25rpx;
		text-align: center;
		color:#888888 ;
		margin-top: 40rpx;
	}
</style>
<!-- text-align: center;
		position: relative;
		background-image: url(../../static/grades.png);
		width: 100%;
		height: 400rpx;
		background-repeat: no-repeat;
		background-size: cover; -->