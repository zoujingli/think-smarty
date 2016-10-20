# think-smarty
ThinkPHP5 Smarty 引擎驱动

## 安装方法

使用composer安装模版引擎方法: <code>composer require zoujingli/think-smarty</code>

## ThinkPHP5 参数配置

```
'template'  => [
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