<template>
	<view>
		<view class="">
			{{countdown_time}}
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				countdown_time: '倒计时00分00秒',
				time:''
			}
		},
		mounted(){
			this.countTime()
		},
		onLoad(){
			var date = new Date();
			var now = date.getTime();
			this.time=now+2700000
		},
		methods: {
		
			countTime() {
				//获取当前时间  
				var date = new Date();
				var now = date.getTime();
				var leftTime = this.time - now;
				if (leftTime <= 0) {
					this.countdown_time = "已结束"
					return
				}
				var d, h, m, s;
				if (leftTime >= 0) {
					  // d = Math.floor(leftTime/1000/60/60/24); 
					h = Math.floor(leftTime / 1000 / 60 / 60 % 24);
					m = Math.floor(leftTime / 1000 / 60 % 60);
					s = Math.floor(leftTime / 1000 % 60);
				}
				//将倒计时赋值到view中  
				this.countdown_time = `倒计时${m}分${s}秒`
				//递归每秒调用countTime方法，显示动态时间效果  
				var timers = setTimeout(this.countTime, 1000);
			},
		
		},
	}
</script>

<style lang="scss">
	/deep/ .uni-searchbar {
		background-color: rgb(79, 191, 141);
	}

	/deep/ .uni-searchbar__cancel {
		color: #fff;
	}
</style>

