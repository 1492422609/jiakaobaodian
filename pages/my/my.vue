<template>
	<view class="bg_total">
		<view class="header">
			<image src="https://z3.ax1x.com/2021/07/22/WwxQ58.png" mode="widthFix" class="bg" />
			<!-- 个人信息 -->
			<view class="my">
				<view style="display: flex;">
					<image src="" mode="" class="avater"></image>
					<view class="text">
						<view class="name">芜湖</view>
						<view class="huiyuanshuxing">会员属性</view>
						<view class="huiyuanshuxing">会员有效期：2021-01-01</view>
					</view>
				</view>
			</view>
			<view class="mingpian">
				<view class="jihuohuiyuan">激活会员</view>
				<view class="lijikaitong_wai">
					<view class="lijikaitong" @click="lijikaitong">立即开通></view>
				</view>
			</view>
		</view>

		<view class="diyilan">
			<view class="diyilan_1">
				<view class="diyilan_1_yincang" :style="{backgroundImage:'url('+ima1+')'}">
					<!-- <image src="https://z3.ax1x.com/2021/07/22/W0QU58.png" mode="" class="diyilan_1_1"></image> -->
				</view>
				<view class="diyilan_1_2">{{titile_1}}</view>
				<view class="diyilan_1_3" @click="zhankai" >点击选择></view>
			</view>
		</view>
		<view @click="isShow=false" >
			<view class="diyilan_yincang" v-show="isShow">
				<view class="diyilan_1">
					<view class="diyilan_1_yincang" :style="{backgroundImage:'url('+ima2+')'}">
						<!-- <image src="https://z3.ax1x.com/2021/07/22/W0QU58.png" mode="" class="diyilan_1_1"></image> -->
					</view>  
					<view class="diyilan_1_2" @click="choose1">{{titile_2}}</view>
				</view>
			</view>
			<view class="diyilan_yincang" v-show="isShow">
				<view class="diyilan_1">
					<view class="diyilan_1_yincang" :style="{backgroundImage:'url('+ima3+')'}">
						<!-- <image src="https://z3.ax1x.com/2021/07/22/W0QU58.png" mode="" class="diyilan_1_1"></image> -->
					</view>
					<view class="diyilan_1_2" @click="choose2">{{titile_3}}</view>
				</view>
			</view>
			<view class="diyilan_yincang" v-show="isShow">
				<view class="diyilan_1">
					<view class="diyilan_1_yincang" :style="{backgroundImage:'url('+ima4+')'}">
						<!-- <image src="https://z3.ax1x.com/2021/07/22/W0QU58.png" mode="" class="diyilan_1_1"></image> -->
					</view>
					<view class="diyilan_1_2" @click="choose3">{{titile_4}}</view>
				</view>
			</view>
		</view>
		
		<view class="dierlan">
			<view class="photos">
				<view class="block">
					<navigator url="../agreement/agreement">
						<image src="https://z3.ax1x.com/2021/07/22/W06hKs.png" mode="" class="photos_1"></image>
						<view class="photos_2">
							用户协议
						</view>
					</navigator>
				</view>
			</view>
			<view class="photos">
				<view class="block">
					<navigator url="../agreement/agreement">
						<image src="https://z3.ax1x.com/2021/07/22/W06L24.png" mode="" class="photos_1"></image>
						<view class="photos_2">
							用户隐私
						</view>
					</navigator>
				</view>
			</view>
			<view class="photos" @click="customer">
				<view class="block">
					<image src="https://z3.ax1x.com/2021/07/22/W0cVsA.png" mode="" class="photos_1"></image>
					<view class="photos_2">
						联系客服
					</view>
				</view>
			</view>
			<view class="photos">
				<view class="block">
					<navigator url="../history/history">
					<image src="https://z3.ax1x.com/2021/07/22/W0cZqI.png" mode="" class="photos_1"></image>
					<view class="photos_2">
						历史成绩
					</view>
					</navigator>
				</view>
			</view>
			<view class="photos">
				<view class="block" @click="remind">
					<image src="https://z3.ax1x.com/2021/07/22/W0gM01.png" mode="" class="photos_1"></image>
					<view class="photos_2" >
						服务商特权
					</view>
				</view>
			</view>
		</view>
		<view style="height: 125rpx;"></view>
		<view v-show="activation" >
			<view class="protect" @click="lijikaitong">
				<view class="Activation_code" @click.stop="stop">
					<view class="top_1">
						请输入激活码
					</view>
					<view class="top_2">
						激活码请联系客服获取
					</view>
					<input type="text" value=""  class="top_3"/>
					<button type="default" class="top_4" >激活会员</button>
				</view>
			</view>
		</view>
		
	    <view class="protect" v-show="tixing" @click="remind()">
	    	<view class="remind">
	    	   <image src="https://z3.ax1x.com/2021/07/26/WW3r34.png" mode="widthFix" class="remind_photo"></image>
			   <view class="">
			   	  <view class="remind_topic">
			   	  				   小霖锦囊提示您
			   	  </view>
			   	  <view class="remind_text">
			   	  				   请联系系统管理员
			   	  </view>
			   	  <view class="remind_text2">
			   	  		开通服务商特权
			   	  </view>
			   </view>
	    	</view>
	    </view>
		<view class="customer" v-show="customer1" @click="customer">
			<view class="protect">
				<view class="QR">
					<image src="https://z3.ax1x.com/2021/07/26/WWt2t0.png" mode="widthFix" style="width: 500rpx;"></image>
					<view style="font-size: 40rpx;font-weight: 600;margin-top: 20rpx;">
						客服二维码
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
				ima:'',
				ima1:'https://z3.ax1x.com/2021/07/22/W0QU58.png',
				ima2:'https://z3.ax1x.com/2021/07/31/WXvUoT.png',
				ima3:'https://z3.ax1x.com/2021/07/31/WXvNwV.png',
				ima4:'https://z3.ax1x.com/2021/07/31/WXvte0.png',
				titile:'',
				titile_1:'小车C1/C2/C3',
				titile_2:'货车A1/B2',
				titile_3:'客车A1/A3/B1',
				titile_4:'摩托车',
				activation:false,
				isShow:false,
				tixing:false,
				customer1:false,
			}
		},
		methods: {
			customer(){
				if(this.customer1===false){
						this.customer1=true
					}else this.customer1=false
			},
			lijikaitong(){
				if(this.activation===false){
						this.activation=true
					}else this.activation=false
			},
			zhankai(){
				if(this.isShow===false){
					this.isShow=true
				}else this.isShow=false	
			},
			choose1(){
				this.titile=this.titile_2;
				this.titile_2=this.titile_1;
				this.titile_1=this.titile;
				this.ima=this.ima2;
				this.ima2=this.ima1;
				this.ima1=this.ima;
			},
			choose2(){
				this.titile=this.titile_3;
				this.titile_3=this.titile_1;
				this.titile_1=this.titile;
				this.ima=this.ima3;
				this.ima3=this.ima1;
				this.ima1=this.ima;
			},
			choose3(){
				this.titile=this.titile_4;
				this.titile_4=this.titile_1;
				this.titile_1=this.titile;
				this.ima=this.ima4;
				this.ima4=this.ima1;
				this.ima1=this.ima;
			},
			remind(){
				if(this.tixing===false){
					this.tixing=true
				}else this.tixing=false	
				console.log(this.tixing)
			},
			stop(){
				
			}
		}
	}
</script>

<style>
	.QR{
		text-align: center;
		margin-top: 300rpx;
		margin-left: 12.5%;
		width: 75%;
		height: 625rpx;
		background-color: white
	}
	.remind_text2{
		position: relative;
		margin-top: 20rpx;
		font-size: 40rpx;
		color: #2C5DFE;
	}
	.remind_text{
		position: relative;
		margin-top: 80rpx;
		color: #2C5DFE;
		font-size: 40rpx;
	}
	.remind_topic{
		/* position: absolute; */
		position: relative;
		margin-top: -380rpx;
		font-size: 35rpx;
	}
	.remind_photo{
		width: 500rpx;
	}
	.remind{
		text-align: center;
		margin-top: 300rpx;
	}
	.top_4{
		width: 60%;
		background-color: #2C5DFE;
		color: white;
		margin-top: 5%;
	}
	.top_3{
		border:#555555 0.5rpx solid;
		border-radius:10rpx ;
		width: 80%;
		height: 15%;
		margin-left: 10%;
	}
	.top_2{
		text-align: center;
		height: 100rpx;
		line-height: 115rpx;
	}
	.top_1{
		font-size: 40rpx;
		font-weight: bold;
		text-align: center;
		width: 100%;
		height: 100rpx;
		line-height: 150rpx;
	}
	.Activation_code{
		height: 500rpx;
		width: 80%;
		background-color: white;
		border-radius: 20rpx;
		margin-left:10%;
		margin-top: 300rpx;
		z-index: 12;
	}
	.protect{
		width:100% ;
		height: 1500rpx;
		background:rgba(0, 0, 0, 0.4);
		position:absolute;
		z-index: 10;
		margin-top: -1100rpx;
		overflow: hidden;
	}
	.photos_2 {
		/* margin-left: 60rpx; */
		padding: 10rpx;
	}

	.photos_1 {
		width: 130rpx;
		height: 130rpx;
		
	}

	.photos {
		margin-left: 70rpx;
	}
	.block{
		text-align: center;
	}
	.diyilan_yincang{
		background-color: white;
		height: auto;
		width: 660rpx;
		border-radius: 20rpx;
		margin-left: auto;
		margin-right: auto;
	}
	.dierlan {
		background-color: white;
		height: auto;
		width: 660rpx;
		border-radius: 20rpx;
		margin-top: 50rpx;
		margin-left: auto;
		margin-right: auto;
		display: flex;
		flex-wrap: wrap;
	}

	.diyilan_1_1 {
		margin-left: -20rpx;
		width: 72rpx;
		height: 72rpx;
	}

	.diyilan_1_2 {
		margin-left: 50rpx;
	}

	.diyilan_1_3 {
		margin-left: 430rpx;
		position: absolute;
	}
	.diyilan_1_yincang{
		margin-left: 40rpx;
		background-image:url("https://z3.ax1x.com/2021/07/22/W0QU58.png");
		width: 72rpx;
		height: 72rpx;
		/* background-color: #000000 */
		background-repeat: no-repeat;
		background-size: cover;
	}
	.diyilan_1 {
		margin-top: 10rpx;
		display: flex;
		margin: 0 auto;
		/* justify-content: center; */
		align-items: center;
		padding: 25rpx;
		font-size:35rpx ;

	}
	.diyilan {
		background-color: white;
		height: auto;
		width: 660rpx;
		border-radius: 20rpx;
		margin-top: 50rpx;
		margin-left: auto;
		margin-right: auto;
		position: relative;
		z-index: 1;
	}

	.bg_total {
		background-color: #F3F3F3;
		/* height: 1300rpx; */
		width: 100%;
	}

	.mingpian {
		display: flex;
		position: absolute;
		margin-top: 320rpx;
		margin-left: 80rpx;
	}

	.jihuohuiyuan {
		color: #FFBC00;
		font-size: 35rpx;
	}

	.lijikaitong_wai {
		height: 50rpx;
		width: 140rpx;
		border-radius: 30rpx;
		background-color: #FFBC00;
		margin-left: 280rpx;
		text-align: center;
		line-height: 50rpx;
	}

	.text {
		color: white;
		margin-left: 20rpx;
		font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif
	}

	.name {
		font-size: 30rpx;
	}

	.huiyuanshuxing {
		font-size: 24rpx;
	}

	.my {
		top: 129rpx;
		left: 40.74rpx;
		position: absolute;
	}

	.avater {
		width: 120rpx;
		height: 120rpx;
		background-color: #0000FF;
		border-radius: 50%;
	}

	.bg {
		width: 100%;
	}

	.header {
		display: flex;
	}
</style>
