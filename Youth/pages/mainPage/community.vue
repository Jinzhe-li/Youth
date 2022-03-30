<template>
	<view style="background-color: #FFFFFF;">
		<scroll-view scroll-y="true" style="padding-left: 3%;width: 94%;height: 695px;margin-top: 35px;">
			<uni-segmented-control :current="current" :values="items" @clickItem="onClickItem" styleType="text"
				activeColor="#4cd964"></uni-segmented-control>
			<view class="content" style="background-color: #FFFFFF;">
				<view v-show="current === 0">
					<scroll-view scroll-y="true" style="height: 700px;">
						<view >
							<view style="height: 10px; background-color: #f3f3f3;"></view>
							<view>
								<avatar></avatar><br>
								<view>
									<view style="width: 375px;">
										<text style="white-space: pre-wrap; word-wrap: break-word;height: auto;">瑜伽练好的人，走到哪里都会吸引人们的眼球。平时穿衣会更英姿挺拔，整个人看着也非常有精气神。</text>
									</view>
									<image src="../../static/10.jpg" style="width: 50%;height: 187.5px;float: left;"></image>
									<image src="../../static/11.jpg" style="width: 50%;height: 187.5px;"></image><br>
									<view>
										<view style="float: left;">
										    <uni-icons type="redo" size="18" color="#999"></uni-icons>
										    <text class="card-actions-item-text">分享</text>
										</view>
										<view style="float: left;margin-left: 5%;">
										    <uni-icons type="heart" size="18" color="#999"></uni-icons>
										    <text class="card-actions-item-text">点赞</text>
										</view>
										<view style="float: left;margin-left: 5%;">
										    <uni-icons type="chatbubble" size="18" color="#999"></uni-icons>
										    <text class="card-actions-item-text">评论</text>
										</view>
									</view>
								</view>
							</view><br>
						</view>
						<view >
							<view style="height: 10px; background-color: #f3f3f3;"></view>
							<view>
								<avatar></avatar><br>
								<view>
									<view style="width: 375px;">
										<text style="white-space: pre-wrap; word-wrap: break-word;height: auto;">HIIT高效燃脂动作 | 锻炼十分钟等于慢跑半小时！</text>
									</view>
									<image src="../../static/5.jpg" style="width: 50%;height: 187.5px;float: left;"></image>
									<image src="../../static/6.jpg" style="width: 50%;height: 187.5px;"></image><br>
									<view>
										<view style="float: left;">
										    <uni-icons type="redo" size="18" color="#999"></uni-icons>
										    <text class="card-actions-item-text">分享</text>
										</view>
										<view style="float: left;margin-left: 5%;">
										    <uni-icons type="heart" size="18" color="#999"></uni-icons>
										    <text class="card-actions-item-text">点赞</text>
										</view>
										<view style="float: left;margin-left: 5%;">
										    <uni-icons type="chatbubble" size="18" color="#999"></uni-icons>
										    <text class="card-actions-item-text">评论</text>
										</view>
									</view>
								</view>
							</view><br>
						</view>
					</scroll-view>
				</view>
				<view v-show="current === 1"  style="background-color: #FFFFFF;">
					<scroll-view scroll-y="true" style="height: 700px;">
						<text style="color: #18BC37;">正在热议</text>
						<view style="margin-top: 1%;">
							<uni-icons type="fire" style="float: left;" size="25"></uni-icons>
							<text style="width: 50%;display: block;float: left;">我与冠军pk</text>
							<text style="margin-left: 10%;">3.5万人围观</text>
						</view>
						<view style="margin-top: 2%;">
							<uni-icons type="fire" style="float: left;" size="25"></uni-icons>
							<text style="width: 50%;display: block;float: left;">越吃越瘦的秘密</text>
							<text style="margin-left: 10%;">3.3万人围观</text>
						</view>
						<view style="margin-top: 2%;">
							<uni-icons type="fire" style="float: left;" size="25"></uni-icons>
							<text style="width: 50%;display: block;float: left;">适合碎片时间的课程</text>
							<text style="margin-left: 10%;">3.1万人围观</text>
						</view>
						<view style="margin-top: 3%;">
							<view style="width: 47.5%; float: left;">
								<image src="../../static/12.jpg" style="width: 100%;"></image>
								<text style="white-space: pre-wrap; word-wrap: break-word;height: 30px;display: block;">现在开始30天强化训练</text><br>
								<image src="../../static/1.jpeg" style="border-radius: 50%;width: 30px;height: 30px;" ></image>
								<text style="font-size: 20px;color: grey;">Jack马</text><br>
							</view>
							<view style="width: 47.5%; float: left;margin-left: 5%;">
								<image src="../../static/8.jpg" style="width: 100%;"></image>
								<text style="white-space: pre-wrap; word-wrap: break-word;height: 30px;display: block;">分享一波训练照</text><br>
								<image src="../../static/9.jpg" style="border-radius: 50%;width: 30px;height: 30px;" ></image>
								<text style="font-size: 20px;color: grey;">爱德华</text><br>
							</view>
						</view>
						<view style="margin-top: 10%;">
							<view style="width: 47.5%; float: left;">
								<image src="../../static/14.jpg" style="width: 100%;"></image>
								<text style="white-space: pre-wrap; word-wrap: break-word;height: auto;">hhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhh</text><br>
								<image src="../../static/10.jpg" style="border-radius: 50%;width: 30px;height: 30px;" ></image>
								<text style="font-size: 20px;color: grey;">Jack马1</text><br>
							</view>
							<view style="width: 47.5%; float: left;margin-left: 5%;">
								<image src="../../static/16.jpg" style="width: 100%;"></image>
								<text style="white-space: pre-wrap; word-wrap: break-word;height: auto;">hhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhh</text><br>
								<image src="../../static/11.jpg" style="border-radius: 50%;width: 30px;height: 30px;" ></image>
								<text style="font-size: 20px;color: grey;">Jack马</text><br>
							</view>
						</view>
					</scroll-view>
				</view>
			</view>
		</scroll-view>
		<view style="margin-left: 3%;margin-right: 3%;">
			<bottomNav color3="#00D2BF"></bottomNav>
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
		methods:{
			onClickItem(e){
				if (this.current != e.currentIndex) {
				  this.current = e.currentIndex;
				}
			}
		},
		data(){
			return{
				items:['关注','热门'],
				current:0,
				keys:['1','2','3']
			}
		}
	}
</script>

<style>
</style>
