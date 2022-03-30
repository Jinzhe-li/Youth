<template>
	<view style="background-color: #FFFFFF;">
		<view style="background-color: #FFFFFF; height: 505px;margin-top: 35px;margin-left: 3%;margin-right: 3%;">
			<view>
				<uni-icons type="arrowleft" size="25"></uni-icons>
				<text style="margin-left: 30%;font-size: 25px;">瑜伽备考</text>
			</view>
			<uni-segmented-control :current="current" :values="items" @clickItem="onClickItem" styleType="text"
				activeColor="#4cd964" ></uni-segmented-control>
			<view style="margin-top: 15%;">
				<view v-show="current === 0">
					<view style="margin-top: 10%;">
						<view style="float: left;">
							<view>
								<view class="t-icon t-icon-dingdan" style="width: 60px;height: 60px; "></view>
								<view><text style="font-size: 24upx;color: #616A6B ;">等级详解</text></view>
							</view>
							<view style="margin-top: 70%;">
								<view class="t-icon t-icon-rili" style="width: 60px;height: 60px; "></view>
								<view><text style="font-size: 24upx;color: #616A6B ;">晋段规则</text></view>
							</view>
							<view style="margin-top: 70%;">
								<view class="t-icon t-icon-bianji " style="width: 60px;height: 60px; "></view>
								<view><text style="font-size: 24upx;color: #616A6B ;">在线答疑</text></view>
							</view>
						</view>
					
						<view class="progress_box" style="float: left;margin-left: 3%;margin-top: 10%;">
							
							<canvas class="progress_bar" canvas-id="cpbar"></canvas>
							<canvas class="progress_line" canvas-id="cpline"></canvas>
							<view class="progress_txt">
								<view class="progress_info">题库练习</view>
							</view>
						</view>
						<view class="progress_box" style="float: left;margin-left: 3%;margin-top: 20%;">
							<canvas class="progress_bar" canvas-id="cpbar"></canvas>
							<canvas class="progress_line" canvas-id="cpline"></canvas>
							<view class="progress_txt">
								<view class="progress_info">模考打分</view>
							</view>
						</view>
					
						<view style="float: right;margin-top: -40%;">
							<view>
								<view class="t-icon t-icon-kaobei" style="width: 60px;height: 60px; "></view>
								<view><text style="font-size: 24upx;color: #616A6B ;">体式训练</text></view>
							</view>
							<view style="margin-top: 70%;">
								<view class="t-icon t-icon-wenjianjia " style="width: 60px;height: 60px; "></view>
								<view><text style="font-size: 24upx;color: #616A6B ;">段位评估</text></view>
							</view>
							<view style="margin-top: 70%;">
								<view class="t-icon t-icon-shoucang " style="width: 60px;height: 60px; "></view>
								<view><text style="font-size: 24upx;color: #616A6B ;">VIP课程</text></view>
							</view>
						</view>
					</view>
				</view>
				<view v-show="current === 1">
					选项卡2的内容
				</view>
				<view v-show="current === 2">
					选项卡3的内容
				</view>
			</view>
		</view>
		<view style="margin-left: 3%;height: 180px;background-color: #FFFFFF;margin-right: 3%;">
			<image src="../../static/guanggap.jpg" style="height: 150px;width: 100%;"></image>
		</view>
		<view style="margin-left: 3%;margin-right: 3%;">
			<bottomNav ></bottomNav>
		</view>
	</view>
</template>

<script>
	import bottomNav from '../component/bottomNav.vue'
	
	export default {
		components:{
			bottomNav
		},
		data() {
			return {
				items: ['段前', '初级', '中级','高级'],
				current: 0
			};
		},
		props: {
			progress_txt: {
				type: Number,
				default: 100
			}
		},
		mounted: function() {
			this.drawProgressbg();
			this.drawCircle(this.progress_txt); //参数为1-100
			this.drawLine();
		},
		methods: {
			onClickItem(e) {
				if (this.current != e.currentIndex) {
					this.current = e.currentIndex;
				}
			},
			drawProgressbg: function() {
				// 自定义组件实例 this ，表示在这个自定义组件下查找拥有 canvas-id 的 <canvas/>
				var ctx = uni.createCanvasContext('cpbg', this);
				ctx.setLineWidth(12); // 设置圆环的宽度
				ctx.setStrokeStyle('#00ff7f'); // 设置圆环的颜色
				// ctx.setLineCap('round'); // 设置圆环端点的形状
				ctx.setLineCap('square'); // 设置圆环端点的形状
				ctx.beginPath(); //开始一个新的路径
				ctx.arc(110, 110, 70, 0 * Math.PI, 2 * Math.PI, false);
				//设置一个原点(110,110)，半径为100的圆的路径到当前路径
				ctx.stroke(); //对当前路径进行描边
				ctx.draw();
			},
			drawCircle: function(step) {
				var ctx = uni.createCanvasContext('cpbar', this);
				// 进度条的渐变(中心x坐标-半径-边宽，中心Y坐标，中心x坐标+半径+边宽，中心Y坐标)
				var gradient = ctx.createLinearGradient(0, 0, 130, 0);

				let increase = 0.05;
				let end = (step / 100) * 2 * Math.PI - Math.PI / 2; // 最后的角度
				let current = -Math.PI / 2; // 起始角度
				let timer = setInterval(() => {
					gradient.addColorStop('0', '#00F2FE');
					gradient.addColorStop('1.0', '#4FACFE');
					ctx.setLineWidth(12);
					ctx.setStrokeStyle(gradient);
					ctx.setLineCap('square');
					ctx.beginPath();
					// 参数step 为绘制的百分比
					if (current < end) {
						current = current + increase;
					}
					if (current >= end) {
						current = end;
						clearInterval(timer);
					}
					ctx.arc(110, 110, 70, -Math.PI / 2, current, false);
					ctx.stroke();
					ctx.draw();
				}, 20);
			},
			drawLine() {
				var context = uni.createCanvasContext("cpline", this);
				var r = 70;
				var x0 = 110;
				var y0 = 110;
				var x;
				var y;
				var lineWidth = 12;

				for (let i = 0; i < 60; i++) {
					context.beginPath();
					context.setLineWidth(lineWidth);
					context.setStrokeStyle("#FFFFFF");

					x = x0 - r * Math.sin(((6 * (i + 1) - 3) * Math.PI) / 180);
					y = y0 - r * Math.cos(((6 * (i + 1) - 3) * Math.PI) / 180);

					// console.log('x0:' + x0 + '   y0:' + y0 + '    x:' + x + '    y:' + y);
					context.moveTo(x, y);
					context.arc(
						x0,
						y0,
						r,
						((270 - 6 * (i + 1) + 3) * Math.PI) / 180,
						((270 - 6 * i) * Math.PI) / 180,
						false
					);
					context.stroke();
					context.closePath();
				}
				context.stroke();
				context.draw();
			}
		},
	}
</script>

<style>
	.progress_box {
		width: 200px;
		height: 100px;
		display: flex;
		align-items: center;
		justify-content: center;
		text-align: center;
	}

	.progress_bg {
		position: absolute;
		width: 220px;
		height: 220px;
	}

	.progress_bar {
		position: absolute;
		width: 220px;
		height: 220px;
		color: #000000;
	}

	.progress_line {
		position: absolute;
		width: 220px;
		height: 220px;
	}

	.progress_txt {
		position: absolute;
		font-size: 28upx;
	}

	.progress_info {
		font-size: 36upx;
		padding-left: 16upx;
		letter-spacing: 2upx;
		font-size: 52upx;
		color: #333333;
	}

	.progress_dot {
		width: 16upx;
		height: 16upx;
		border-radius: 50%;
		background-color: #fb9126;
	}
</style>
