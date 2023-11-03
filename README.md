# 百度翻译API封装

### Usage:

- 定位到您的项目路径运行

```
composer require Lambq/baidu-translation
```

```php

    use Lambq\BaiduTranslation\BaiduTranslation;
    
    # $app_id = 您的ID;
    # $secrect_key = 您的Key;

    $translation = new BaiduTranslation($app_id,$secrect_key);

    # $query 要查询的内容
    # $from 源语言（见语言列表）
    # $to 目标语言 （见语言列表）


    $res = $translation->translate($query,$from,$to);

```

返回值为json格式

```json
成功：
{
    'result':'翻译结果',
    'status': 0
}

失败：
{
    'result':'错误原因',
    'status': 1
}
```