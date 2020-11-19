# Angularjs 多語系 練習
> 此為測試使用 angular.js 多語系支用


## 系統需求

1. library 設定
```html
<!-- 引入 angular-translate -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/angular-translate/2.9.2/angular-translate.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/angular-translate/2.9.2/angular-translate-loader-static-files/angular-translate-loader-static-files.min.js"></script>
```
2. angular.js 設定
```javascript
var app = angular
			// pascalprecht.translate 引入
			.module('app', ['pascalprecht.translate'])
			.controller('myController', ['$scope', '$translate',
				function ($scope, $translate) {
                }])
			.config(function ($translateProvider) {
				// 读取本地JSON文件，prefix代表文件路径前缀，suffix代表文件后续
				$translateProvider.useStaticFilesLoader({
					prefix: './lang/',
					suffix: '.json'
				});
				// 设置默认的语言
				$translateProvider.preferredLanguage('zh');
			});;                    
                    
```





## 參考文章

