<template>
	<view style="background-color: #FFFFFF;">
		<view style="height: 500px;background: linear-gradient(#00c1ae,#90f0c0,#ffffff);margin-top: 35px;">
			<view style="margin-left: 3%;font-size: 35px;padding-top: 5%;color: #FFFFFF;">训练计划</view>
			<view style="margin-left: 3%;font-size: 25px;color: #FFFFFF;margin-top: 3px;">高效矫正瑜伽体式</view>
			<view style="margin-left: 3%;font-size: 20px;color: #FFFFFF;margin-top: 3px;">·实时矫正</view>
			<view style="margin-left: 3%;font-size: 20px;color: #FFFFFF;margin-top: 3px;">·智能提醒</view>
		</view>
		<scroll-view scroll-y="true" style="margin-left: 3%;margin-top: -85%;width: 94%;height: 500px;">
			<view style="position: relative;">
				<image src="../../static/14.jpg" style="width: 375px;height: 200px;"></image>
				<view><text  style="font-size: 24upx; position: absolute;top: 90px;left: 80px;font-size: 50upx;">高能燃脂瑜伽课程</text></view>
			</view>
			<navigator url="./plan" open-type="redirect">
				<view style="padding-top: 0px;">
					<view style="width: 100%;height: 30px; background-color: #f3f3f3;"></view>
					<view style="position: relative;margin-top: 0px;">
						<image src="../../static/3.jpeg" style="width: 375px;height: 200px;"></image>
						<view><text  style="font-size: 24upx; position: absolute;top: 90px;left: 80px;font-size: 50upx;">高能燃脂瑜伽课程</text></view>
					</view>
				</view>
			</navigator>
			
		</scroll-view>
		<bottom-nav></bottom-nav>
	</view>
</template>

<script>
	import bottomNav from '../component/bottomNav.vue'
	
	export default{
		data(){
			return{
				items:[{message:'1'},{message:'2'},{message:'3'},{message:'4'}]
			}
		},
		components:{
			bottomNav
		}
	}
</script>

<style>
</style>
