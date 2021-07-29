<template>
	<view>
		<view class="top">
			<view class="top_1">
				<view class="quesiton_now">
					{{quesiton_now}}
				</view>
				<view class="quesiton_total">
					{{quesiton_total}}
				</view>
			</view>
			<view class="top_2_wai">
				单选
			</view>
			<view class="top_3_wai">
				<image src="https://z3.ax1x.com/2021/07/26/WRI4AI.png" mode="widthFix" class="top_photo"></image>
				<view class="top_text">
					读题
				</view>
			</view>
			<view class="top_4_wai">
				<image src="https://z3.ax1x.com/2021/07/26/WRI5Nt.png" mode="widthFix" class="top_photo"></image>
				<view class="top_text">
					设置
				</view>
			</view>
		</view>
	    <view class="topic">
	    	超车前需从前车左侧超越，以下说法正确的是 ？
	    </view>
		<view class="answer_total">
			<view class="answer" v-for="qut in question">
				<view class="answer_pad">
					<view class="answer_num">
					    {{qut.id}}
					</view>
					<view class="answer_text">
				        {{qut.que}}
					</view>
				</view>
			</view>
			
				
		</view>
		<view class="jinnang">
			<view class="jinnang_1">
				<image src="https://z3.ax1x.com/2021/07/26/WRqnXT.png" mode="widthFix" style="width: 100rpx;margin-top: 10rpx;"></image>
			    <view style="margin-top: 10rpx;">
			    	小霖锦囊
			    </view>
			</view>
		</view>
	    <view class="footer">
	    	<view class="line"></view>
			<view  style="display: flex; padding-bottom: 20rpx;">
				<view class="collection">
					<image src="https://z3.ax1x.com/2021/07/26/WWSz1H.png" mode="widthFix" class="footer_photo"></image>
					<view class="footer_text">
						收藏
					</view>
				</view>
				<view class="share">
					<image src="https://z3.ax1x.com/2021/07/26/WWpScd.png" mode="widthFix" class="footer_photo"></image>
					<view class="footer_text">
						分享
					</view>
				</view>
				<view class="yon">
					<image src="https://z3.ax1x.com/2021/07/26/WWppjA.png" mode="widthFix" class="footer_photo"></image>
					<view style="color: #0CAF00;margin-left: 3rpx;">
						1
					</view>
					<image src="https://z3.ax1x.com/2021/07/26/WWpCnI.png" mode="widthFix" class="footer_photo"  style="margin-left:15rpx;"></image>
					<view style="color: #FF0000;margin-left: 3rpx;">
						0
					</view>
				</view>
				<view class="footer_question" @click="pop">
					<image src="https://z3.ax1x.com/2021/07/26/WWpPBt.png" mode="widthFix" class="footer_photo"></image>
					<view class="">
						{{quesiton_now}}
					</view>
					<view class="">
						{{quesiton_total}}
					</view>
				</view>
			</view>
	        <view class="footer_pop" v-show="box" >
	        	<view class="circulal">
	        		1
	        	</view>
				<view class="circulal">
					1
				</view>
				<view class="circulal">
					1
				</view>
				<view class="circulal">
					1
				</view><view class="circulal">
					1
				</view><view class="circulal">
					1
				</view><view class="circulal">
					1
				</view><view class="circulal">
					1
				</view><view class="circulal">
					1
				</view><view class="circulal">
					1
				</view><view class="circulal">
					1
				</view><view class="circulal">
					1
				</view><view class="circulal">
					1
				</view><view class="circulal">
					1
				</view><view class="circulal">
					1
				</view><view class="circulal">
					1
				</view><view class="circulal">
					1
				</view>
				
	        </view>
		</view>
	 
	</view>
</template>

<script>
	export default {
		data() {
			return {
				box:false,
				quesiton_now:1,
				quesiton_total:'/10',
				question:[{
					id:'A',
					que:'我国实行左侧通行原则'
				},{
					id:'B',
					que:'我国实行左侧通行原则22'
				},{
					id:'C',
					que:'我国实行左侧通行原则1'
				},{
					id:'D',
					que:'我国实行左侧通行原则35'
				}]
			}
		},
		methods: {
			pop(){
				if(this.box===false){
					this.box=true
				}else this.box=false	
			}
		}
	}
</script>

<style>
	.circulal{
		width: 50rpx;
		height: 50rpx;
		line-height: 50rpx;
		border-radius: 50%;
		background-color: #DCFFDA;
		color: #0CAF00;
		text-align: center;
        margin: 30rpx 20rpx 1px;
		display: inline-block;
	}
	.footer_pop{
		height: 500rpx;
		width: 100%;
		background-color:white;
		/* display:flex; */
		/* flex-wrap: wrap; */
	}
	.footer_question{
		display: flex;
		margin-top:20rpx ;
		margin-left: 75rpx;
		font-size: 33rpx;
	}
	.yon{
		margin-top: 20rpx;
		display: flex;
		margin-left: 75rpx;
		font-size: 35rpx;
	}
	.share{
		margin-top: 20rpx;
		display: flex;
		margin-left:75rpx;
	}
	.footer_text{
		margin-top: 6rpx;
		margin-left: 10rpx;
		font-size: 30rpx;
	}
	.collection{
		margin-top: 20rpx;
		display: flex;
		margin-left: 30rpx;
	}
	.footer_photo{
		width: 40rpx;
		margin-top: 5rpx;
		
	}
	.line{
		width: 100%;
		height: 7rpx;
		background-color: #00000029
	}
	.footer{
		position: fixed;
		bottom: 0;
		/* height: 100rpx; */
		width: 100%;
		/* background-color: #0000FF */
	}
	.jinnang{
		position: absolute;
		background-color: #2C5DFE;
		width: 150rpx;
		height: 180rpx;
		margin-left: 550rpx;
		margin-top: 200rpx;
		border-radius: 30rpx;
		color: white;
		text-align: center;
	}
	.answer_text{
		margin-left: 30rpx;
	}
	.answer_pad{
		margin-left: 30rpx;
		display: flex;
		position: absolute;
		margin-top: 20rpx;
	}
	.answer{
		width: 90%;
		margin-top: 30rpx;
		margin-left: 5%;
		height: 90rpx;
		background-color: #EBEBEB;
		border-radius: 10rpx;
		/* vertical-align: middle; */
	}
	.topic{
		margin-top: 30rpx;
		margin-left: 5%;
		font-size: 33rpx;
		font-weight: 600;
	}
	.top_4_wai{
		height: 55rpx;
		line-height: 55rpx;
		width: 150rpx;
		border-radius: 30rpx;
		background-color: #2C5DFE;
		margin-left: 20rpx;
		text-align: center;
		line-height: 50rpx;
		color: white;
		font-size: 30rpx;
		font-weight: 500;
		margin-top: 7rpx;
		display: flex;
		text-align: center;
	}
	.top_text{
		/* margin-top: 5rpx; */
		margin-left: 10rpx;
	}
	.top_3_wai{
		height: 55rpx;
		line-height: 55rpx;
		width: 150rpx;
		border-radius: 30rpx;
		background-color: #2C5DFE;
		margin-left: 140rpx;
		text-align: center;
		line-height: 50rpx;
		color: white;
		font-size: 30rpx;
		font-weight: 500;
		margin-top: 7rpx;
		display: flex;
		text-align: center;
	}
	.top_photo{
		margin-top: 13rpx;
		margin-left: 20rpx;
		width: 30rpx;
	}
	.top_2_wai{
		height: 55rpx;
		line-height: 55rpx;
		width: 120rpx;
		border-radius: 30rpx;
		background-color: #2C5DFE;
		margin-left: 20rpx;
		text-align: center;
		line-height: 50rpx;
		color: white;
		font-size: 35rpx;
		font-weight: 500;
		margin-top: 7rpx;
		text-align: center;
	}
	.quesiton_total{
		color:#AAAAAA ;
	}
	.quesiton_now{

	}
	.top_1{
		margin-left: 20rpx;
		display: flex;
		font-size: 45rpx;
	}
	.top{
		margin-top: 20rpx;
		display: flex;
	}
</style>
