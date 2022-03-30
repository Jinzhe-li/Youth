<template>
	<view style="background-color: #FFFFFF;height: 60px;">
		<navigator url="../mainPage/home" open-type="redirect">
			<view style="margin-top: 1%;float: left;">
				<uni-icons type="home" :color="color1" size="30"></uni-icons><br>
				<text :style="{color: color1}">首页</text>
			</view>
		</navigator>
		<navigator url="../mainPage/sport" open-type="redirect">
			<view style="margin-top: 1%;float: left; margin-left:20%;">
				<uni-icons type="star" :color="color2" size="30"></uni-icons><br>
				<text :style="{color: color2}">运动</text>
			</view>
		</navigator>
		<navigator url="../mainPage/community" open-type="redirect">
			<view style="margin-top: 1%;float: left; margin-left:20%;">
				<uni-icons type="chat" :color="color3" size="30"></uni-icons><br>
				<text :style="{color: color3}">论坛</text>
			</view>
		</navigator>
		<navigator url="../mainPage/user" open-type="redirect">
			<view style="margin-top: 1%;float: left; margin-left:20%;">
				<uni-icons type="person" :color="color4" size="30"></uni-icons><br>
				<text :style="{color: color4}">我的</text>
			</view>
		</navigator>

	</view>
</template>

<script>
	export default {
			props:['color1','color2','color3','color4']
		}
</script>

<style>
</style>
