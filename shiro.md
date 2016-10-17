
# shiro 权限框架

	用户的认证和授权
	
	1. subject 
	2. security 
	3. Manager
	4. authenticator认证
	5. authorizer   授权
	6. sessionManager   web容器管理session
	7. sessionDao     针对个性化的session数据存储
	8. cache Manager  缓存管理器  将授权数据通过cacheManager 进行缓存
	9. realm   写认证和授权的逻辑
	10. cryptography : 安全加密


# shiro 与spring的整合
	【shiro在web中是以filter的形式整合的】

	shiro默认认证成功后会返回上一个链接

	熟悉: shiro的认证流程


		 shiro的鉴权流程:
			[
				注解方式
				shiro标签方式
			]




# shiro 的认证和授权 缓存
	针对大量的鉴权信息频繁查询数据库  需要使用缓存来处理
	默认是关闭认证的缓存信息 开启鉴权的缓存信息
	
	