<template>
	<view class="main" id="modified-data">
		<view class="content"></view>
		<view class="return">
			<view class="return_box" @click="returnClick">
				<image src="../../static/img-percenter/return.png"></image>
			</view>
		</view>
		<view class="datum">
			<view class="headPortrait">
				<view class="datum_one">头像</view>
				<view class="datum_img">
					<image :src="img"></image>
				</view>
			</view>
			<view class="name">
				<view class="datum_one">姓名</view>
				<view class="datum_two">
					<image src="../../static/img-percenter/orders.png"></image>
				</view>
			</view>
			<view class="sex">
				<view class="datum_one">性别</view>
				<view class="datum_two">
					<image src="../../static/img-percenter/orders.png"></image>
				</view>
			</view>
			<view class="birthday">
				<view class="datum_one">生日</view>
				<view class="datum_two">
					<image src="../../static/img-percenter/orders.png"></image>
				</view>
			</view>
		</view>
		<view class="privacy">
			<view class="changePassword">
				<view class="datum_one">修改密码</view>
				<view class="datum_two">
					<image src="../../static/img-percenter/orders.png"></image>
				</view>
			</view>
			<view class="encrypted">
				<view class="datum_one">密保手机</view>
				<view class="datum_two">
					<image src="../../static/img-percenter/orders.png"></image>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default{
		data(){
			return{
				img:''
			}
		},
		onLoad(data) {
			this.img = data.img
		},
		methods:{
			returnClick(){
				uni.navigateBack({
					delta:1
				})
			},
		}
	}
</script>

<style scoped>
	.main{background-color:#eaeaea;height: 1334rpx;}
	image{width: 100%;height: 100%;}
	.content{width:100%;height:80rpx;background-color:#eaeaea;}
	.return{margin-left:32rpx;}
	.return .return_box{width:40rpx;height: 40rpx;}
	/* 个人资料: */
	.datum{width: 100%;background-color: #eaeaea;padding-top: 20rpx;font-size: 32rpx;font-weight: 550;}
	.headPortrait{width: 100%;height: 150rpx;line-height:150rpx; margin-bottom: 2rpx;background-color: white;}
	.datum_one{width: 300rpx;float: left;margin-left: 32rpx;}
	.datum_two{float: right;width: 42rpx;height: 42rpx;margin-right: 32rpx;}
	.datum_img{float: right;width: 100rpx;height: 100rpx;border: 2rpx solid #EEEEEE;margin-right: 32rpx;border-radius: 50%;margin-top: 18rpx;}
	.name,.sex,.birthday,.changePassword,.encrypted{background-color: white;width: 100%;height: 100rpx;line-height: 100rpx; margin-bottom: 2rpx;}
	.privacy{margin-top: 20rpx;font-size: 32rpx;font-weight: 550;}
</style>
