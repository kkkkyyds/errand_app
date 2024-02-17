<template>
	<view style="padding: 20rpx;">
		<view class="box" style="padding: 60rpx 30rpx;">
			<view style="font-size: 40rpx;">欢迎登录</view>
			<view style="margin: 60rpx 0;">
				<uni-forms ref="formRef" :modelValue="form" :rules="rules" validateTrigger="blur">
					<uni-forms-item name="username" required>
						<uni-easyinput prefixIcon="person" v-model="form.username" placeholder="请输入账号" />
					</uni-forms-item>
					<uni-forms-item name="password" required>
						<uni-easyinput type="password" prefixIcon="locked" v-model="form.password"
							placeholder="请输入密码" />
					</uni-forms-item>
					<uni-forms-item>
						<button type="primary"
							style="width: 100%; height: 70rpx; line-height: 70rpx; background-color: #006eff; border-color: #006eff;">登
							录</button>
					</uni-forms-item>
				</uni-forms>
			</view>
			
			<uni-forms-item style="text-align: right;">
					还没有账号？请<navigator style="display: inline; margin-left: 5rpx; color: #006eff;">注册</navigator>
			</uni-forms-item>
			
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				form: {},
				rules: {
					// 对字段进行必填验证
					username: {
						// username 字段的校验规则
						rules: [
							// 校验 username 不能为空
							{
								required: true,
								errorMessage: '请输入账号',
							},
						],
					},
					password: {
						// password 字段的校验规则
						rules: [
							// 校验 password 不能为空
							{
								required: true,
								errorMessage: '请输入密码',
							},
						]
					}
				}
			}
		},
		methods: {

		}
	}
</script>

<style>

</style>