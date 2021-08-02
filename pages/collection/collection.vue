<template>
	<view>
	   <view class="header_header" >
	    	<view style="display: flex;">
					<view class="" style="color: black;padding-top: 70rpx;margin-left: 30rpx;font-size: 40rpx;" @click="con">
					    返回
					</view>
					<view class="header_middle">
						<view class="header_middle_left" :style="{color:ccc,'background-color':bgc,}" @click="change">
							错题
						</view>
						<view class="header_middle_right" :style="{'background-color':ccc,color:bgc,}" @click="change">
							收藏
						</view>
					</view>
	    	</view>
	    </view>	
		<view class="header">
			<view class="avater">
				<image src="https://z3.ax1x.com/2021/07/26/WWcPET.png" mode="widthFix" style="width: 150rpx;"></image>
				<view class="name">
					芜湖起飞
				</view>
			</view>
		</view>
	    <view class="middle">
	    	<view class="middle_1">
	    		<view v-show="chan">
	    			<image :src="bg_1" mode="widthFix" class="middle_photo"></image>
	    		</view>
				<view class="middle_text" >
	    	    	{{text1}}
	    	    </view>
				<view class="middle_text2">
					50
				</view>
				<view class="middle_text3">
					道
				</view>
			</view>
	    </view> 
		<view class="bottom">
			<navigator url="../library/library">
				<view class="test1">
					全部错题
				</view>
			</navigator>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				indexSearchBar:'padding-top: '+uni.getSystemInfoSync().statusBarHeight+'px',
				// 状态栏高度
				statusBarHeight: 'padding-top: '+uni.getSystemInfoSync().statusBarHeight+'px',
				// 导航栏高度
				navBarHeight: 82,
				bgc:'white',
				ccc:'#2C5DFE',
				none:'',
				chan:true,
				bg_1:'https://z3.ax1x.com/2021/07/26/WflSld.png',
				text1:'全部错题',
				text2:'收藏题目',
				text:''
			}
		},
		methods: {
			con(){
				uni.switchTab({
				url: '/pages/index/index'
				});
			},
			change(){
				this.none=this.bgc;
				this.bgc=this.ccc;
				this.ccc=this.none;
				
				this.text=this.text1;
				this.text1=this.text2;
				this.text2=this.text;
			},
			
		}
	}
</script>

<style scoped>
	.header_middle_right{
		width: 100rpx;
		height: 58rpx;
		text-align: center;
		border-radius:0 10rpx 10rpx 0;
		/* border:  1rpx #000000 solid; */
	}
	.header_middle_left{
		/* background-color: white; */
		width: 50%;
		/* height: 80rpx; */
		text-align: center;
		border-radius: 10rpx  0 0 10rpx;
		/* border:  1rpx #000000 solid; */
	}
	.header_middle{
		position: absolute;
		width: 200rpx;
		height: 60rpx;
		line-height: 60rpx;
		border-radius: 10rpx;
		margin-left: 35%;
		margin-top: 50rpx;
		background-color: white;
		display: flex;
		justify-content: space-between;
		/* padding: 0 50rpx; */
		/* border:  2rpx solid black; */
		/* box-sizing: border-box; */
		/* z-index: 10; */
		/* overflow: hidden; */
	}
	.header_header{
		width: 100%;
		height: 133rpx;
		background-color: #F8F8F8;

	}

	.middle_text3{
		margin-left: 10rpx;
		font-size: 35rpx;
		font-weight: 600;
	}
	.middle_text2{
		margin-left: 170rpx;
		font-size: 45rpx;
		font-weight: 600;
		color:#2C5DFE ;
	}
	.middle_text{
		margin-left: 50rpx;
		font-size: 35rpx;
		font-weight: 600;
	}
	.middle_photo{
		width: 120rpx;
		margin-top: 40rpx;
		margin-left: 50rpx;
	}
	.middle_1{
		display: flex;
		width: 90%;
		height: 200rpx;
		line-height:200rpx ;
		/* background-color: #0000FF; */
		margin-left: 5%;
		margin-top: 60rpx;
		border-radius: 30rpx;
		box-shadow: 1px 1px 2px 2px rgba(0, 0, 0, 0.1);
	}
	.test1{
		width: 60%;
		height: 85rpx;
		line-height: 80rpx;
		background-color: #2C5DFE;
		border-radius: 20rpx;
		color: white;
		font-size: 35rpx;
		text-align: center;
		margin-left: 20%;
		margin-top: 80rpx;
	}
	
	.name{
		font-size: 38rpx;
		margin-top: 10rpx;
	}
	.avater{
		text-align: center;
	    margin-top: 40rpx; 
	}
	
	/* 收藏 */
	.box_vip{
		width: 250rpx;
		height: 50rpx;
		line-height: 50rpx;
		background-image: linear-gradient(to right, #FFBC00 , #FFE6A2);
		text-align: center;
		border-radius: 30rpx;
	}
	.jinnang{
		width: 90%;
		margin-top: 30rpx;
		margin-left: 5%;
		
	}
	.answer_text{
		height: 50rpx;
		line-height: 50rpx;
	}
	
	.answer_num{
		width: 50rpx;
		height: 50rpx;
		line-height: 50rpx;
		text-align: center;
		border-radius: 50%;
		/* background-color: black; */
	}
	.parse {
		width: 90%;
		/* height: 100rpx; */
		margin-top: 30rpx;
		margin-left: 5%;
		padding: 30rpx;
		background-color: #F0F7FF;
		border-radius: 10rpx;
		/* display: flex; */
		/* vertical-align: middle; */
	}
	
	.verticl {
		height: 70rpx;
		width: 5rpx;
		background-color: #EBEBEB;
		margin: 0 30rpx;
	}
	
	.yes_text2 {
		text-align: center;
		color: #0CAF00;
		font-size: 45rpx;
	}
	
	.yes_text {
		font-size: 20rpx;
	}
	
	.yes {
		/* width: 15%; */
		/* display: flex; */
	}
	
	.green_line {
		width: 90%;
		margin-top: 30rpx;
		margin-left: 5%;
		padding: 15rpx 15rpx 5rpx 40rpx;
		background-color: #DCFFDA;
		border-radius: 10rpx;
		display: flex;
		/* vertical-align: middle; */
	}
	
</style>
