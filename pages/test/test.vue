<template>
	<view>
			<view class="wrap">
				<view class="u-tabs-box">
					<u-tabs-swiper activeColor="#f29100" ref="tabs" :list="list" :current="current" @change="change" :is-scroll="false" swiperWidth="750"></u-tabs-swiper>
				</view>
				<swiper class="swiper-box" :current="swiperCurrent" @transition="transition" @animationfinish="animationfinish">
					<swiper-item class="swiper-item">
						<scroll-view scroll-y style="height: 100%;width: 100%;">
							<view class=""></view>
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
			</view>
		</view>
	
</template>
<script>
	export default {
		data() {
			return {
				list: [
					{
						name: '内容一'
					},
					{
						name: '内容二'
					},
					{
						name: '内容三'
					},
					{
						name: '内容四',
					}
				],
				// 内容
				current: 0,
				// 下标
				swiperCurrent: 0,
				// 偏移量
				dx: 0,
			};
		},
		methods: {
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
	};

</script>
<style>
	.wrap {
		width: 100%;
		height: calc(100vh - var(--window-top));
		display: flex;
		flex-direction: column;
		
		.page-box{
			text-align: center;
		}
	}
	.swiper-box {
		flex: 1;
	}
	.swiper-item {
		height: 100%;
	}

</style>