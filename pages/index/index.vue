<template>
	<view class="container">
		<view  :class="colors">{{user}}</view>
		<view class="intro">本项目已包含uni ui组件，无需import和注册，可直接使用。在代码区键入字母u，即可通过代码助手列出所有可用组件。光标置于组件名称处按F1，即可查看组件文档。</view>
		<text class="intro">详见：</text>
		<text @click="handleClick">{{useraddone}}</text>
		<input v-model="username" type="text">
		<input v-model="password" type="text">
		<uni-link :href="href" :text="href"></uni-link>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				href: 'https://uniapp.dcloud.io/component/README?id=uniui',
				user: '周',
				colors: 'dadsa',
				firstNum: 1,
				secondNum: 2,
				username: '',
				password: ''
			}
		},
		methods: {
			handleClick() {
			let a = this.user
				this.user = '叶'
				this.colors="ss"
				console.log(this.user, this.password)
			}
		},
		computed:{ //计算属性
			useraddone() {
				return this.firstNum / 2
			}
		}
	}
</script>

<style lang="scss">
	.container {
		padding: 20px;
		font-size: 14px;
		line-height: 24px;
		.dadsa{
			color: $uni-color-warning;
		}
		.ss {
			color: black;
		}
	}
</style>
