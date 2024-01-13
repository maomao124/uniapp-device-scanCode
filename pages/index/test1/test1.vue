<template>
	<view>
		<button type="primary" @click="button1">扫码</button>
		<button type="primary" @click="button2">只能从相机扫码</button>
		<button type="primary" @click="button3">扫码类型 一维码</button>
		<button type="primary" @click="button4">扫码类型 二维码</button>
		<button type="primary" @click="button5">扫码类型 Data Matrix 码</button>
		<button type="primary" @click="button6">扫码类型 PDF417 条码</button>
		<button type="primary" @click="button7">自动识别字符编码</button>
		<button type="primary" @click="button8">禁用自动放大</button>
		<button type="primary" @click="button9">支持手动输入条形码</button>
		<button type="primary" @click="button10">隐藏相册</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			button1()
			{
				uni.scanCode({
					success: (res) => {
						console.log('内容：',res);
					},
					fail: (err) => {
						console.log("错误：",err);
					}
				})
			},
			button2()
			{
				uni.scanCode({
					onlyFromCamera:true,
					success: (res) => {
						console.log('内容：',res);
					},
					fail: (err) => {
						console.log("错误：",err);
					}
				})
			},
			button3()
			{
				uni.scanCode({
					onlyFromCamera:true,
					scanType:'barCode',
					success: (res) => {
						console.log('内容：',res);
					},
					fail: (err) => {
						console.log("错误：",err);
					}
				})
			},
			button4()
			{
				uni.scanCode({
					onlyFromCamera:true,
					scanType:'qrCode',
					success: (res) => {
						console.log('内容：',res);
					},
					fail: (err) => {
						console.log("错误：",err);
					}
				})
			},
			button5()
			{
				uni.scanCode({
					onlyFromCamera:true,
					scanType:'datamatrix',
					success: (res) => {
						console.log('内容：',res);
					},
					fail: (err) => {
						console.log("错误：",err);
					}
				})
			},
			button6()
			{
				uni.scanCode({
					onlyFromCamera:true,
					scanType:'pdf417',
					success: (res) => {
						console.log('内容：',res);
					},
					fail: (err) => {
						console.log("错误：",err);
					}
				})
			},
			button7()
			{
				uni.scanCode({
					onlyFromCamera:true,
					autoDecodeCharset:true,
					success: (res) => {
						console.log('内容：',res);
					},
					fail: (err) => {
						console.log("错误：",err);
					}
				})
			},
			button8()
			{
				uni.scanCode({
					onlyFromCamera:true,
					autoDecodeCharset:false,
					success: (res) => {
						console.log('内容：',res);
					},
					fail: (err) => {
						console.log("错误：",err);
					}
				})
			},
			button9()
			{
				uni.scanCode({
					onlyFromCamera:true,
					scanType:'barCode',
					barCodeInput:true,
					success: (res) => {
						console.log('内容：',res);
					},
					fail: (err) => {
						console.log("错误：",err);
					}
				})
			},
			button10()
			{
				uni.scanCode({
					hideAlbum:true,
					success: (res) => {
						console.log('内容：',res);
					},
					fail: (err) => {
						console.log("错误：",err);
					}
				})
			},
		}
	}
</script>

<style>
button{
	margin: 5px;
}
</style>
