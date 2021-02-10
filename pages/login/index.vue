<template>
	<view class="container">
		<header class='login-title' >QAU科研学生团队</header>
		<!-- <div class='logo-wrapper'> -->
		<img class='login-logo' src="@/static/boy.jpg" alt="帅哥"/>
		<!-- </div > -->
	    <view class='login-form'>   
			<view class="username"  >
				用户名
				<input v-model="username"/>
			</view>
			 <!-- v-model="password"获取和变更数据 -->
	    	<view class='password'  >	密码
				<input type="password" v-model="password"/>
			</view>
		</view>
		<div class="check">
			<input type="radio" />
		</div>
		<button class='login-page-btn ' @click="loginBtnHandleClick">登录</button>
		<button class="login-page-btn reg-button" @click="regBtnHandleclick">注册</button>
		
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
			loginBtnHandleClick() {
			
				console.log(this.username, this.password)
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
	
	
		.login-page-btn{
		width: 30%;
		background-color: rgb(55, 0, 255);
		margin-top: 60rpx;

		}
		.reg-button{
			margin-top: 30rpx;	
		}
	}
	page{
		height: 100%;
    }

   
    // .login-logo{
	// 	text-align: center;      图片居中方法
	// }
</style>
