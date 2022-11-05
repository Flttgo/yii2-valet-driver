# yii2-valet-driver
提供yii2 basic 版本和 Advance 高级版的引用

## 引入本地

- 执行目录,找到对应用户下的目录：
- `cd ~/.config/valet/Drivers && wget https://github.com/Flttgo/yii2-valet-driver/blob/b80cbf0bb00a596ddd26dd587a4f8eace6c594ef/Yii2ValetDriver.php`

## basic 版本配置

- 进入和根`web`目录同级的目录下，执行 `valet link your_domain` 

- 在`config/main.php` 开启 `enablePrettyUrl=>true` 美化url

	```
	'urlManager' => [
            	'enablePrettyUrl' => true,
            	'showScriptName' => false,
            	'rules' => [
            	],
        	],
	```

## Advance 版本配置

- 我们进入会看到`backend`、`console`、`frontend` 三个目录
- 找到带有web 子目录的，如 `backend` 下的web 目录执行 `valet link your_domain`  [后台域名]
	+ 访问方式 your_domain/site/index, 其中site 为我们的控制器 index 为actionIndex
- 找到带有web 子目录的，如 `frontend` 下的web 目录执行 `valet link your_domain` 
	+ 访问方式 your_domain/site/index, 其中site 为我们的控制器 index 为actionIndex
	
## 脚本模式不受影响

- 依然是按照 `php yii site/index` 去执行
