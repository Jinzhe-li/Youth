<template>
	<view style="background-color: #FFFFFF;">
		<scroll-view scroll-y="true" style="height: 695px;margin-top: 35px;">
			<view style="padding-left: 3%;padding-top: 5%; height: 30px;">
				<view style="float: left;"><text style="font-size: 20px;">我的课程库</text></view>
				<uni-icons type="bars" style="margin-left: 60%;"  size="20"></uni-icons>
			</view> 
			<view style="margin-left: 3%;width: 94%;height: 10px; background-color: #f3f3f3;"></view>
			<view  style="padding-top: 5%;">
				<view style="float: left;"><image src="../../static/7.jpg" style="width: 80px;height: 40px;"></image></view>
				<view style="float: left;">
					<text style="font-size: 20px;">我学过的课程</text>
				</view>
				<uni-icons type="forward" size="30" style="margin-left: 67%;color: #1BB088;"></uni-icons>
			</view>
			<view style="margin-left: 3%;width: 94%;height: 15px; background-color: #f3f3f3;"></view>
			<view style="padding-left: 3%;padding-top: 2%;position: relative;">
				<navigator url="./planList" open-type="redirect">
					<view style="float: left;" ><text  style="font-size: 24upx;color: #1BB088;font-size:22px;">推荐计划</text></view>
					<uni-icons type="forward" size="20" style="margin-left: 67%;color: #1BB088;"></uni-icons><br>
				</navigator>
				<view style="position: relative;">
					<image src="../../static/15.jpg" style="width: 337px;height: 200px; border-radius: 3%;"></image>
					<view><text  style="font-size: 24upx; position: absolute;top: 90px;left: 130px;font-size: 50upx;">高能燃脂瑜伽计划</text></view>
				</view>
			</view>
			<view style="margin-left: 3%;width: 94%;height: 30px; background-color: #f3f3f3;"></view>
			<view style="padding-left: 3%;padding-top: 2%;position: relative;">
				<view style="float: left;" ><text  style="font-size: 24upx;color: #1BB088;font-size:22px;">推荐课程</text></view>
				<uni-icons type="forward" size="20" style="margin-left: 67%;color: #1BB088;"></uni-icons><br>
				<view style="position: relative;">
					<image src="../../static/6.jpg" style="width: 337px;height: 200px; border-radius: 3%;"></image>
					<view><text  style="font-size: 24upx; position: absolute;top: 90px;left: 130px;font-size: 50upx;">高能燃脂瑜伽课程</text></view>
				</view>
			</view>
		</scroll-view>
		<view style="margin-left: 3%;margin-right: 3%;">
			<bottomNav color2="#00D2BF"></bottomNav>
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
