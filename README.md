[![Latest Stable Version](https://poser.pugx.org/zoujingli/think-smarty/v/stable)](https://packagist.org/packages/zoujingli/think-smarty)
[![Total Downloads](https://poser.pugx.org/zoujingli/think-smarty/downloads)](https://packagist.org/packages/zoujingli/think-smarty)
[![Latest Unstable Version](https://poser.pugx.org/zoujingli/think-smarty/v/unstable)](https://packagist.org/packages/zoujingli/think-smarty)
[![License](https://poser.pugx.org/zoujingli/think-smarty/license)](https://packagist.org/packages/zoujingli/think-smarty)

# think-smarty
ThinkPHP5 Smarty 引擎驱动

## 安装方法

使用composer安装模版引擎方法: `composer require zoujingli/think-smarty`

## ThinkPHP5 配置文件中`template`参数

```
[
	// 模板引擎类型，指定为'Smarty'
	'type'         => 'Smarty',
	// 模板路径，默认为当前模块下的`view`目录
	'view_path'    => '',
	// 模板后缀
	'view_suffix'  => 'tpl',
	// 模板文件名分隔符
	'view_depr'    => '.',
	// 模板引擎普通标签开始标记
	'tpl_begin'    => '<{',
	// 模板引擎普通标签结束标记
	'tpl_end'      => '}>',
	// 标签库标签开始标记
	'taglib_begin' => '{',
	// 标签库标签结束标记
	'taglib_end'   => '}',
],
```
那么在控制器 `index/index::index` 中 `return view();`时会加载模板 `index/view/index.index.tpl`

## 模板常量定义
```
[
  '__ROOT__' => 'http://localhost/service/public',
  '__SELF__' => 'http://localhost/service/public/index.php/index/index.html?id=1&name=3',
  '__APP__' => 'http://localhost/service/public/index.php',
  '__LIB__' => 'http://localhost/service/public/static/plugs',
  '__STATIC__' => 'http://localhost/service/public/static',
  '__UPLOAD__' => 'http://localhost/service/public/static/upload',
]
```