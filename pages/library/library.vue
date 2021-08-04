<template>
	<view>
		<view class="header_header">
			<view style="display: flex;">
				<view class="" style="color: black;padding-top: 70rpx;margin-left: 30rpx;font-size: 40rpx;"
					@click="con">
					返回
				</view>
				<view class="header_middle">
					<view class="header_middle_left" :style="{'background-color':ccc,color:bgc,}" @click="change">
						学习
					</view>
					<view class="header_middle_right" :style="{color:ccc,'background-color':bgc,}" @click="change">
						记忆
					</view>
				</view>
			</view>
		</view>

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
				{{type}}
			</view>
			<view class="top_3_wai">
				<image src="https://z3.ax1x.com/2021/07/26/WRI4AI.png" mode="widthFix" class="top_photo"></image>
				<view class="top_text">
					读题
				</view>
			</view>
			<view class="top_4_wai" @click="fons">
				<image src="https://z3.ax1x.com/2021/07/26/WRI5Nt.png" mode="widthFix" class="top_photo"></image>
				<view class="top_text">
					设置
				</view>
			</view>
		</view>
		<view class="topic" :style="{'font-size':font_size+'rpx'}">
			{{topic}}
		</view>
		<view class="answer_total">
			<!-- :style="qut.answer===index_1 ? 'background-color:#DCFFDA':''" @click="cli(index)" -->
				<view class="answer" v-for="(qut,index) in question" :ikey="index" :style="{'font-size':font_size+'rpx'}">
					<!-- <view :style="qut.answer===index_1 ? 'background-color:#DCFFDA':'background-color:red'" @click="cli(index)"> -->
						<view class="answer_pad">
							<view :style="{margin: qut.ques=== '' ? '0rpx' : '20rpx'}">
								{{qut.ques}}
							</view>
						</view>
					<!-- </view> -->
				</view>
		</view>
			<!-- </view> -->

		<view v-show="jiyi" style="margin-bottom: 100rpx;">
			<view class="green_line">
				<view class="yes">
					<view class="yes_text">
						正确答案
					</view>
					<view class="yes_text2">
						{{answer}}
					</view>
				</view>
				<view class="verticl"></view>
				<view class="yes">
					<view class="yes_text">
						我的答案
					</view>
					<view class="yes_text2">
						{{answer}}
					</view>
				</view>
			</view>
			<view class="jinnang2">
				<view style="display: flex;">
					<image src="https://z3.ax1x.com/2021/07/29/WbPMxs.png" mode="widthFix"
						style="width: 40rpx;margin-right: 20rpx;"></image>
					<view>
						技巧锦囊
					</view>
				</view>
				<view style="display: flex;margin: 30rpx 0;justify-content: space-between;">
					<view style="" :style="{'font-size':font_size+'rpx'}">
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
					<view :style="{'font-size':font_size+'rpx'}">
						正确答案是A，无证驾驶可构成危险驾驶罪
					</view>
				</view>
			</view>

		</view>


		<view class="jinnang" v-show="jinnang">
			<view class="jinnang_1">
				<image src="https://z3.ax1x.com/2021/07/26/WRqnXT.png" mode="widthFix"
					style="width: 100rpx;margin-top: 10rpx;"></image>
				<view style="margin-top: 10rpx;">
					小霖锦囊
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
					<image src="https://z3.ax1x.com/2021/07/26/WWpPBt.png" mode="widthFix" class="footer_photo"></image>
					<view class="">
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

			</view>
		</view>
		<view class="size" v-show="size">
			<view @click="fons">
				<view class="size_bottom" @click.stop="stop">
					<view>
						<view class="bottom_topic">
							字体大小设置
						</view>
						<view class="line_5"></view>
					</view>
					<view class="size_bottom_text">
						<view class="">
							小号
						</view>
						<view class="">
							标准
						</view>
						<view class="">
							特大
						</view>
					</view>
					<view style="display:flex ;margin-left:100rpx  ;">
						<view class="">
							A
						</view>
						<view :class="font_size==30 ? 'size_cir1':'size_cir'" @click="font_size0"></view>
						<view class="size-line"></view>
						<view :class="font_size==35 ? 'size_cir1':'size_cir'" @click="font_size2"></view>
						<view class="size-line"></view>
						<view :class="font_size==40 ? 'size_cir1':'size_cir'" @click="font_size3"></view>
						<view class="size-line"></view>
						<view :class="font_size==45 ? 'size_cir1':'size_cir'" @click="font_size4"></view>
						<view class="size-line"></view>
						<view :class="font_size==50 ? 'size_cir1':'size_cir'" @click="font_size5"></view>
						<view style="font-size: 50rpx;">
							A
						</view>
					</view>
				</view>
			</view>
		</view>
		<view class="remind_change" v-show="remind_change" @click="remind_change1">
			<image src="https://z3.ax1x.com/2021/08/02/fSrWjJ.png" mode="widthFix"
				style="width: 500rpx;position: absolute;margin-top: -150rpx;"></image>
		</view>


	</view>
</template>

<script>
	var that=this
	export default {
		methods: {
			cli(index){
				that.index_1=index
				console.log(that.index_1)
			},
			questio(index) {
				// console.log(index)
				this.quesiton_now = this.quesiton_now + 1
				var that = this
				that.qus = that.qus + 1;
				let i = that.qus;
				// if(index==0){
				// 	that.answer_or='A'
				// }else if(index==1){
				// 	that.answer_or='B'
				// }else if(index==2){
				// 	that.answer_or='C'
				// }else if(index==3){
				// 	that.answer_or='D'
				// 	// console.log(that.answer_or)
				// }
				if (that.qus > 9) {
					that.remind_change = true
					that.qus = 0
					that.quesiton_now = 1
					that.eq_question_type = that.eq_question_type + 1;
					if (that.eq_question_type > 3) {
						that.eq_question_type = 1
					}
					that.request_1()
				} else {
					// that.topic = that.quesiton_tot[i].question_content
					// that.question[0].ques = that.quesiton_tot[i].option1
					// that.question[1].ques = that.quesiton_tot[i].option2
					// that.question[2].ques = that.quesiton_tot[i].option3
					// that.question[3].ques = that.quesiton_tot[i].option4
					// if (that.question[3].ques == null) {
					// 	that.question[0].ques = '对'
					// 	that.question[1].ques = '错'
					// 	that.question[2].ques = ''
					// 	that.question[3].ques = ''
					// }
				}

			},
			font_size5() {
				this.font_size = 50
			},
			font_size4() {
				this.font_size = 45
			},
			font_size3() {
				this.font_size = 40
			},
			font_size2() {
				this.font_size = 35
			},
			font_size0() {
				this.font_size = 30
			},
			pop() {
				if (this.box === false) {
					this.box = true;
					this.jinnang = false;
				} else {
					this.box = false;
					this.jinnang = true;
				}
				if (this.jiyi == true) {
					this.jinnang = false
				}
			},
			fons() {
				if (this.size == false) {
					this.size = true;
					this.jinnang = false;
				} else {
					this.size = false;
					this.jinnang = true;
				}
				if (this.jiyi == true) {
					this.jinnang = false
				}
			},
			stop() {

			},
			request_1(){
				// var that =this
				uni.request({
					url: 'http://jiakao.maiwd.cn/api/question/random_ten',
					method: "POST",
					data: {
						token: '465456ugi',
						eq_car_type: 1,
						eq_subject: 1,
						eq_question_type: that.eq_question_type,
						limit:10
					},
					success: (res) => {
						let i = this.qus
						that.quesiton_tot = res.data.data
						that.topic = that.quesiton_tot[i].question_content
						console.log(JSON.stringify(that.quesiton_tot[i].answer))
						that.answer=that.quesiton_tot[i].answer
						that.question[0].ques = that.quesiton_tot[i].option1
						that.question[1].ques = that.quesiton_tot[i].option2
						that.question[2].ques = that.quesiton_tot[i].option3
						that.question[3].ques = that.quesiton_tot[i].option4
						if(that.quesiton_tot[i].answer=='A'){
							that.question[0].answer=0
						}else if(that.quesiton_tot[i].answer=='B'){
							that.question[0].answer=1
						}else if(that.quesiton_tot[i].answer=='C'){
							that.question[0].answer=2
						}else if(that.quesiton_tot[i].answer=='D'){
							that.question[0].answer=3
						}
							// console.log(that.question[0].answer)
						if (that.question[3].ques == null) {
							that.question[0].ques = '对'
							that.question[1].ques = '错'
							that.question[2].ques = ''
							that.question[3].ques = ''
						}
						if (res.data.data[i].question_type == 1) {
							that.type = '单选'
						} else if (res.data.data[i].question_type == 2) {
							that.type = '多选'
						} else {
							that.type = '判断'
						}
					}
				})
				
			},
			remind_change1() {
				that.remind_change = false
			},
			change() {
				this.none = this.bgc;
				this.bgc = this.ccc;
				this.ccc = this.none;

				this.text = this.text1;
				this.text1 = this.text2;
				this.text2 = this.text;

				if (this.jinnang == true) {
					this.jinnang = false
				} else this.jinnang = true

				if (this.jiyi == false) {
					this.jiyi = true
				} else this.jiyi = false

			},
			con() {
				uni.switchTab({
					url: '/pages/index/index'
				});
			},
		},
		onLoad() {
			 that = this;
			// console.log(that.question[0].id);
			that.request_1()
		},
		data() {
			return {
				index_1:'',
				answer_or:'',
				answer:'',
				remind_change: false,
				eq_question_type: 1,
				quesion_1: '',
				question_tot: '',
				qus: 0,
				jiyi: false,
				bgc: 'white',
				ccc: '#2C5DFE',
				none: '',
				chan: true,
				pages: 17,
				// font_size1:30,
				font_size: 35,
				size: false,
				topic: '',
				type: '',
				jinnang: true,
				box: false,
				quesiton_now: 1,
				quesiton_total: '/10',
				question: [{
					ques: '',
					answer:''
				}, {
					ques: '',
					answer:''
				}, {
					ques: '',
					answer:''
				}, {
					ques: '',
					answer:''
				}]
			}
		},

	}
</script>

<style scoped>
	.size-line {
		width: 120rpx;
		height: 5rpx;
		background-color: #C8C7CC;
		margin: 8rpx -10rpx;
	}

	.size_cir1 {
		height: 30rpx;
		width: 30rpx;
		border-radius: 50%;
		background-color: #2C5DFE;
		z-index: 10;
		margin-top: -5rpx;
	}

	.size_cir {
		height: 20rpx;
		width: 20rpx;
		border-radius: 50%;
		background-color: #000000;
		z-index: 10;
	}

	.size_bottom_text {
		display: flex;
		justify-content: space-around;
		margin: 30rpx;
	}

	.line_5 {
		width: 15%;
		height: 5rpx;
		margin-left: 42.5%;
		background-color: #0000FF;
	}

	.bottom_topic {
		text-align: center;
		font-size: 35rpx;
		padding: 30rpx 0 20rpx;
	}

	.size_bottom {
		position: fixed;
		bottom: 0;
		width: 100%;
		height: 350rpx;
		background-color: white;
	}

	.protect {
		width: 100%;
		/* height: 1700rpx; */
		background: rgba(0, 0, 0, 0.4);
		position: absolute;
		z-index: 10;
		/* margin-top: -800rpx; */
		overflow: hidden;
		z-index: 500;
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
		padding-top: 20rpx;
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

	.jinnang {
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

	.answer_text {
		margin-left: 30rpx;
	}

	.answer_pad {
		margin-left: 30rpx;
		display: flex;
		/* z-index: ; */
		/* position: absolute; */

	}

	.answer {
		width: 90%;
		margin-top: 30rpx;
		margin-left: 5%;
		/* height: 90rpx; */
		background-color: #EBEBEB;
		border-radius: 10rpx;
		/* padding: 10rpx 0; */
		/* vertical-align: middle; */
		/* z-index: 10; */
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

	.header_middle_right {
		width: 100rpx;
		height: 58rpx;
		text-align: center;
		border-radius: 0 10rpx 10rpx 0;
		/* border:  1rpx #000000 solid; */
	}

	.header_middle_left {
		/* background-color: white; */
		width: 50%;
		/* height: 80rpx; */
		text-align: center;
		border-radius: 10rpx 0 0 10rpx;
		/* border:  1rpx #000000 solid; */
	}

	.header_middle {
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

	.header_header {
		width: 100%;
		height: 133rpx;
		background-color: #F8F8F8;

	}

	/* 收藏 */
	.box_vip {
		width: 250rpx;
		height: 50rpx;
		line-height: 50rpx;
		background-image: linear-gradient(to right, #FFBC00, #FFE6A2);
		text-align: center;
		border-radius: 30rpx;
	}

	.jinnang2 {
		width: 90%;
		margin-top: 30rpx;
		margin-left: 5%;

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
