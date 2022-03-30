<template>
	<view>
		<scroll-view scroll-y="true" style="height: 695px;margin-top: 35px;">
			<view style="height: 150px;background: linear-gradient(#99FFCC,#00D2BF);">
				<view style="margin-left: 75%;">
					<uni-icons type="gear" size="30"></uni-icons>
					<uni-icons type="scan" size="30"></uni-icons>
					<uni-icons type="email-filled" size="30"></uni-icons>
				</view>
				<view style="margin-top: 6%; margin-left: 5%;">
					<image src="../../static/1.jpeg" style="border-radius: 50%;width: 80px;height: 80px;float: left;" ></image>
					<view style="float: left;margin-left: 3%;margin-top: 3%;">
						<text style="font-size: 23px;">Jack马</text><br>
						<view>
							<uni-icons type="star-filled"></uni-icons>
							<text >健身达人</text>
						</view>
					</view>
					<uni-icons type="right" style="color: grey; position: absolute;left: 400px;top:100px" size="40"></uni-icons>
				</view>
			</view>
			<view>
				<view style="margin-left: 17%;margin-top: 3%;">
						<text >0</text>
						<text style="margin-left: 35%;">0</text>
						<text style="margin-left: 35%;">0</text>
				</view>
				<view style="margin-left: 14.5%;">
						<text style="color: grey;">关注</text>
						<text style="margin-left: 25%;color: grey;">粉丝</text>
						<text style="margin-left: 26.5%;color: grey;">动态</text>
				</view>
			</view>
			<view style="margin-top: 3%;">
				<text style="color: #00D2BF;font-size: 20px;margin-left: 3%;">数据报表</text><br>
				<view style="width: 50%;float: left;">
					<uni-card title="运动数据">
					    <text>总运动</text><br>
						<text>0千卡</text><br>
						<text>本周消耗0千卡</text><br>
						<text>本周训练次数0</text><br>
						<text>训练正确率0%</text><br>
					</uni-card>
				</view>
				<view style="width: 50%;float: left;">
					<uni-card title="健康数据">
					    <text>体重</text><br>
					    <text>0千克</text><br>
					    <text>本周减重0kg</text><br>
						<text>平均心率0</text><br>
						<text>上次记录 今天</text><br>
					</uni-card>
				</view>
			</view><br><br><br><br><br><br><br>
			<view style="margin-top: 10%;margin-left: 3%;">
				<text style="color: #00D2BF;font-size: 20px;">推荐服务</text><br>
				<view style="margin-top: 10%;float: left;margin-left: 8%;">
					<uni-icons type="cloud-download" size="50" style="color:#00D2BF;"></uni-icons><br>
					<view>
						<text style="color: grey;">离线缓存</text>
					</view>
				</view>
				<view style="margin-top: 10%;float: left;margin-left: 15%;">
					<uni-icons type="loop" size="50" style="color:#00D2BF;"></uni-icons>
					<view>
						<text style="color: grey;">历史记录</text>
					</view>
				</view>
				<view style="margin-top: 10%;float: left;margin-left: 15%;">
					<uni-icons type="star" size="50" style="color:#00D2BF;"></uni-icons><br>
					<view>
						<text style="color: grey;">我的收藏</text>
					</view>
				</view>
				<view style="margin-top: 5%;float: left;margin-left: 8%;">
					<uni-icons type="settings" size="50" style="color:#00D2BF;"></uni-icons><br>
					<view>
						<text style="color: grey;">安全阈值</text>
					</view>
				</view>
				<view style="margin-top: 5%;float: left;margin-left: 15%;">
					<uni-icons type="videocam" size="50" style="color:#00D2BF;"></uni-icons><br>
					<view>
						<text style="color: grey;">一键投屏</text>
					</view>
				</view>
				<view style="margin-top: 5%;float: left;margin-left: 15%;">
					<uni-icons type="flag" size="50" style="color:#00D2BF;"></uni-icons><br>
					<view>
						<text style="color: grey;">我的目标</text>
					</view>
				</view>
			</view>
		</scroll-view>
		
		<view style="margin-left: 3%;margin-right: 3%;">
			<bottomNav color4="#00D2BF"></bottomNav>
		</view>
	</view>
</template>

<script>
	import bottomNav from '../component/bottomNav.vue'
	
	export default{
		components:{
			bottomNav
		}
	}
</script>

<style>
</style>
