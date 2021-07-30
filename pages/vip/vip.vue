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
			<view class="answer" v-for="(qut,jud) in question"  :style="qut.jud=='yes' ? 'background-color:#DCFFDA;':''">
				<view class="answer_pad">
					<view class="answer_num" :style="qut.jud=='yes' ? 'background-color:#0CAF00;color:white' : '' ">
						{{qut.id}}
					</view>
					<view class="answer_text">
						{{qut.que}}
					</view>
				</view>
			</view>


		</view>
		<view class="green_line">
			<view class="yes">
				<view class="yes_text">
					正确答案
				</view>
				<view class="yes_text2">
					A
				</view>
			</view>
			<view class="verticl"></view>
			<view class="yes">
				<view class="yes_text">
					我的答案
				</view>
				<view class="yes_text2">
					A
				</view>
			</view>
		</view>
		<view class="jinnang">
			<view style="display: flex;">
				<image src="https://z3.ax1x.com/2021/07/29/WbPMxs.png" mode="widthFix" style="width: 40rpx;margin-right: 20rpx;"></image>
				<view>
					技巧锦囊
				</view>
			</view>
			<view style="display: flex;margin: 30rpx 0;justify-content: space-between;">
				<view style="">
					本体技巧本体技巧本体技巧
				</view>
				<view class="box_vip">
					开通会员后查看
				</view>
			</view>
		</view>
		<view class="parse">
			<view class="">
				<view style="color: #525252;">
					解析
				</view>
				<view>
					正确答案是A，无证驾驶可构成危险驾驶罪
				</view>
			</view>
		</view>		
		<view class="footer">
			<view class="line"></view>
			<view style="display: flex; padding-bottom: 20rpx;">
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
					<image src="https://z3.ax1x.com/2021/07/26/WWpCnI.png" mode="widthFix" class="footer_photo"
						style="margin-left:15rpx;"></image>
					<view style="color: #FF0000;margin-left: 3rpx;">
						0
					</view>
				</view>
				<view class="footer_question" @click="pop">
					<image src="https://z3.ax1x.com/2021/07/26/WWpPBt.png" mode="widthFix" class="footer_photo" style="margin-left: -10rpx;margin-right: 10rpx;"></image>
					<view >
						{{quesiton_now}}
					</view>
					<view class="">
						{{quesiton_total}}
					</view>
				</view>
			</view>
			<view class="footer_pop" v-show="box">
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
				</view>
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
				</view>
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
				</view>
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
				</view>
				<view class="circulal">
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
				jinnang: true,
				box: false,
				quesiton_now: 1,
				quesiton_total: '/10',
				 isactive:0,
				question: [{
					jud:'yes',
					id: 'A',
					que: '我说数量的开发基斯里夫结束了'
				}, {
					// jud:'no',
					id: 'B',
					que: '我说数量的开发基斯里夫结束了'
				}, {
					// jud:'no',
					id: 'C',
					que: '我说数量的开发基斯里夫结束了'
				}, {
					// jud:'',
					id: 'D',
					que: '我说数量的开发基斯里夫结束了'
				}]
			}
		},
		methods: {
			pop() {
				if (this.box === false) {
					this.box = true;
					this.jinnang = false;
				} else {
					this.box = false;
					this.jinnang = true;
				}


			}
		}
	}
</script>

<style scoped>
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

	.circulal {
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

	.footer_pop {
		height: 500rpx;
		width: 100%;
		background-color: white;
		/* display:flex; */
		/* flex-wrap: wrap; */
	}

	.footer_question {
		display: flex;
		margin-top: 20rpx;
		margin-left: 75rpx;
		font-size: 33rpx;
	}

	.yon {
		margin-top: 20rpx;
		display: flex;
		margin-left: 75rpx;
		font-size: 35rpx;
	}

	.share {
		margin-top: 20rpx;
		display: flex;
		margin-left: 75rpx;
	}

	.footer_text {
		margin-top: 6rpx;
		margin-left: 10rpx;
		font-size: 30rpx;
	}

	.collection {
		margin-top: 20rpx;
		display: flex;
		margin-left: 30rpx;
	}

	.footer_photo {
		width: 40rpx;
		margin-top: 5rpx;

	}

	.line {
		width: 100%;
		height: 7rpx;
		background-color: #00000029
	}

	.footer {
		position: fixed;
		bottom: 0;
		/* height: 100rpx; */
		width: 100%;
		background-color: white
	}


	.answer_text {
		margin-left: 30rpx;
	}

	.answer_pad {
		margin-left: 30rpx;
		display: flex;
		position: absolute;
		margin-top: 20rpx;
	}

	.answer {
		width: 90%;
		margin-top: 30rpx;
		margin-left: 5%;
		height: 90rpx;
		background-color: #EBEBEB;
		border-radius: 10rpx;
		/* vertical-align: middle; */
	}

	.topic {
		margin-top: 30rpx;
		margin-left: 5%;
		font-size: 33rpx;
		font-weight: 600;
	}

	.top_4_wai {
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

	.top_text {
		/* margin-top: 5rpx; */
		margin-left: 10rpx;
	}

	.top_3_wai {
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

	.top_photo {
		margin-top: 13rpx;
		margin-left: 20rpx;
		width: 30rpx;
	}

	.top_2_wai {
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

	.quesiton_total {
		color: #AAAAAA;
	}

	.quesiton_now {}

	.top_1 {
		margin-left: 20rpx;
		display: flex;
		font-size: 45rpx;
	}

	.top {
		margin-top: 20rpx;
		display: flex;
	}
</style>
