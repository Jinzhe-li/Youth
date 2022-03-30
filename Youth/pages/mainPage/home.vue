<template>
	<view style="background-color: #FFFFFF;">
		<scroll-view scroll-y="true" style="height: 695px;margin-top: 35px;">
			<view>
				<image src="../../static/Youth.png" style="width: 120px; height: 120px; float: left;"></image>
				<view style="padding-top: 5%;"><text  style="font-size: 50upx; float: left;color:  #00D2BF;">首页</text></view>
				<view style="padding-top: 2%;">
					<uni-icons type="personadd-filled" size="30" style="margin-left: 30%;color:  #00D2BF;"></uni-icons>
					<uni-icons type="search" size="30" style="color:  #00D2BF;" ></uni-icons>
				</view>
			</view><br>
			<view style="padding-top: 12%; padding-left: 3%;padding-right: 3%;">
				<view style="float: left;">
					<view class="t-icon t-icon-homepage" style="width: 60px;height: 60px; "></view>
					<view ><text  style="font-size: 24upx;color: #616A6B ;">全部课程</text></view>
				</view>
				<view style="float: left;margin-left: 2.5%;">
					<view class="t-icon t-icon-tag" style="width: 60px;height: 60px;"></view>
					<view ><text  style="font-size: 24upx;color: #616A6B ;">热门课程</text></view>
				</view>
				<view style="float: left;margin-left: 2.5%;">
					<view class="t-icon t-icon-cloud" style="width: 60px;height: 60px;"></view>
					<view ><text  style="font-size: 24upx;color:#616A6B  ;">直播课程</text></view>
				</view>
				<view style="float: left;margin-left: 2.5%;">
					<view class="t-icon t-icon-box" style="width: 60px;height: 60px;"></view>
					<view ><text  style="font-size: 24upx;color: #616A6B ;">多人瑜伽</text></view>
				</view>
				<view style="float: left;margin-left: 2.5%;">
					<navigator url="./exam" open-type="redirect">
						<view class="t-icon t-icon-list" style="width: 60px;height: 60px;"></view>
						<view ><text  style="font-size: 24upx;color: #616A6B ;">瑜伽备考</text></view>
					</navigator>
				</view>
			</view>
			<br><br><br><br>
			<view style="padding-left: 3%;padding-top: 2%; padding-right: 3%;position: relative;">
				<view style="float: left;" ><text  style="font-size: 24upx;color:  #00D2BF;font-size:22px;">推荐</text></view>
				<uni-icons type="forward" size="20" style="margin-left: 76%;color:  #00D2BF;"></uni-icons><br>
				<view style="position: relative;">
					<image src="../../static/2.jpeg" style="width: 337px;height: 200px; border-radius: 3%;"></image>
					<view><text  style=" position: absolute;top: 90px;left: 90px;font-size: 45upx;">高能燃脂瑜伽计划</text></view>
				</view>
			</view>
			<view style="padding-left: 3%;padding-right: 3%; margin-top: 5%;" v-for="item in items">
				<avatar></avatar><br>
				<view>
					<view style="width: 337px;">
						<text style="white-space: pre-wrap; word-wrap: break-word;height: auto;">听说多做瑜伽会瘦肚子</text>
					</view>
					<image src="../../static/3.jpeg" style="width: 160.5px;height: 160.5px;float: left;"></image>
					<image src="../../static/4.jpeg" style="width: 160.5px;height: 160.5px;"></image><br>
					<view>
						<text>2.5万点赞</text>
						<text style="margin-left: 55%;">15万浏览</text>
					</view>
				</view>
			</view>
		</scroll-view>
		<view style="margin-left: 3%;margin-right: 3%;">
			<bottomNav color1="#00D2BF"></bottomNav>
		</view>
	</view>
</template>

<script>
	import avatar from '../component/avatar.vue';
	import bottomNav from '../component/bottomNav.vue'
	
	export default{
		components:{
			avatar,
			bottomNav
		},
		data(){
			return{
				items:[{message:'1'},{message:'2'}]
			}
		}
	}
</script>

<style>
</style>
