<template>
	<view class="container">
		<header class='login-title' >QAU科研学生团队</header>
		<!-- <div class='logo-wrapper'> -->
		<img class='login-logo' src="@/static/boy.jpg" alt="帅哥"/>
		<!-- </div > -->
	    <view class='login-form'>   
			<view class="username" >
				用户名
				<input />
			</view>
	    	<view class='password'>	密码
				<input/>
			</view>
		</view>
		<div class="check">
		
		</div>
		<button class='login-button'>登录</button>
		<button class="reg-button">注册</button>
		
		<uni-link ></uni-link>
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
	
    .container{
		height: 100%;
		background-color: green;
		padding-top: 120rpx;
		.login-title{

			color:red;
			font-size:20px;
			text-align: center;	
	  	}
		.login-logo{
			width:150rpx;
			height:150rpx;
			margin:50rpx auto 0;
			display: block;
			border-radius:50%;
		 }	
		.login-form{
			width: 60%;  
			font-size: 40rpx;
			margin:0 auto;
		 	input{
					border: 1px solid black;
				}	  
		}
		.login-button{
			width: 30%;
			margin-top: 60rpx;
			background-color: rgb(55, 0, 255);
		}
		.reg-button{
			width: 30%;
			margin-top: 30rpx;
			background-color: rgb(55, 0, 255);
		}
	
	}
	page{
		height: 100%;
    }

   
    // .login-logo{
	// 	text-align: center;      图片居中方法
	// }
</style>
