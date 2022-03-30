<template>
	<view style="padding-left: 3%;width: 94%;">
		<view style="height: 695px;margin-top: 35px;">
			<navigator url="./planList" open-type="redirect">
				<uni-icons type="arrow-left" style="font-size: 30px; color: #18BC37;"></uni-icons>
			</navigator>
			<view style="position: relative;">
				<image src="../../static/3.jpeg" style="width: 345px;height: 200px;"></image>

				<view><text
						style="font-size: 24upx; position: absolute;top: 120px;font-size: 50upx;color: #18BC37;">高能燃脂瑜伽课程</text>
				</view>
			</view>
			<view>
				<uni-segmented-control style="width: 91%;" :current="current" :values="items" @clickItem="onClickItem"
					styleType="text" activeColor="#18BC37"></uni-segmented-control>
				<view class="content">
					<view v-show="current === 0">
						<scroll-view scroll-y="true">
							<text style="font-size: 25px; ">简介</text>
							<view style="width: 375px;">
								<text
									style="white-space: pre-wrap; word-wrap: break-word;height: auto;">通过热身的方式，带你练习瑜伽基础入门体式，熟悉体式和呼吸技巧，高效激活全身。本节课可每天作为热身来练习。</text>
							</view>
							<view style="margin-top: 10%;"></view>
							<text style="font-size: 25px; ">适用人群</text>
							<view style="width: 375px;">
								<text
									style="white-space: pre-wrap; word-wrap: break-word;height: auto;">想减脂塑形的朋友<br>想热身激活身体的朋友<br>想要入门的瑜伽爱好者</text>
							</view>
						</scroll-view>
					</view>
					<view v-show="current === 1">
						选项卡2的内容
					</view>
				</view>
			</view>
		</view>
		<button style="width: 50%;background-color: #18BC37;color: #FFFFFF;margin-left: 25%;"
			@click="saveVideo()()">开始训练</button>
	</view>
</template>

<script>
	export default {
		methods: {
			onClickItem() {
				return 1;
			},
			saveVideo() {
				let _this = this;
				uni.chooseVideo({
					count: 1,
					sourceType: ['camera'],
					success: res => {
						console.log(res.tempFilePath)
						this.videoPath = res.tempFilePath;
						this.getTempFilePath(res.tempFilePath, 'videoTempPath');
					},
					fail: (err) => {
						uni.getSetting({
							success: (res) => {
								let authStatus = res.authSetting['scope.camera'];
								if (!authStatus) {
									uni.showModal({
										title: '授权失败',
										content: 'Hello uni-app需要从您的相机获取视频，请在设置界面打开相关权限',
										success: (res) => {
											if (res.confirm) {
												uni.openSetting()
											}
										}
									})
								}
							}
						})
					}
				});
			},
			getTempFilePath(url, types) {
				uni.showLoading({
					title: '保存中...'
				});
				// 如果已经下载本地路径，那么直接储存
				let obj = {
					filePath: url,
					success: () => {
						uni.showModal({
							content: '保存成功',
							showCancel: false
						});
						uni.hideLoading();
					},
					fail: e => {
						uni.hideLoading();
						uni.showModal({
							content: '保存失败',
							showCancel: false
						});
					}
				};
			}
		},
		data() {
			return {
				items: ['计划介绍', '计划预览'],
				current: 0
			}
		}
	}
</script>

<style>
</style>
