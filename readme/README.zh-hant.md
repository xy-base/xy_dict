<!--
 * @Author: yuyangit yuyangit.0515@qq.com
 * @Date: 2024-10-18 13:21:27
 * @LastEditors: yuyangit yuyangit.0515@qq.com
 * @LastEditTime: 2024-10-24 19:52:09
 * @FilePath: /xy_dict/readme/README.zh-hant.md
 * @Description: 这是默认设置,请设置`customMade`, 打开koroFileHeader查看配置 进行设置: https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE
-->
# xy_dict

| [简体中文](../README.md)         | [繁體中文](./README.zh-hant.md)        |                      [English](./README.en.md)          |
| ----------- | -------------|---------------------------------------|

## 說明
字典工具。

## 程式碼庫

| [Github](https://github.com/xy-base/xy_dict.git)         | [Gitee](https://gitee.com/xy-opensource/xy_dict.git)        |                      [GitCode](https://gitcode.com/xy-opensource/xy_dict.git)          |
| ----------- | -------------|---------------------------------------|

## 安裝

```bash
# bash
pip install xy_dict
```

## 使用

```python
# Python 解释器

from xy_dict.utils import is_empty_dict, dict_get

object_map_0 = {}
is_empty_dict(object_map_0)
# True

object_map_1 = {"key_0":"object_0"}
is_empty_dict(object_map_1)
# False

dict_get(object_map_1, "key_0")
# object_0

dict_get(object_map_0, "key_0")
# None

from xy_dict.Dict import Dict

object_map_2 = {"key_0":"object_0", "key_1":{"key_2":"object_2"}, "key_3":["object_3"]}
object_dict = Dict(object_map_2)

object_dict.search_k("key_0")
object_dict.key_map
# {'key_0': 'object_0'}

object_dict.search_k("key_1")
object_dict.key_map
# {'key_1': {'key_2': 'object_2'}}

object_dict.search_v("object_0")
object_dict.key_map
# {'key_0': 'object_0'}

object_dict.search_v({"key_2":"object_2"})
object_dict.key_map
# {'key_1': {'key_2': 'object_2'}}

object_dict.search_kv('key_0', 'object_0')
object_dict.key_map
# {'key_0': 'object_0'}

object_dict.search_kv('key_0', 'object_0')
object_dict.key_map
# {'key_0': 'object_0'}

object_dict.search_kv('key_0', 'object_01')
object_dict.key_map
# {}

```

## 許可證
xy_dict 根據 <木蘭寬鬆許可證, 第2版> 獲得許可。有關詳細信息，請參閱 [LICENSE](../LICENSE) 文件。

## 捐贈

如果小夥伴們覺得這些工具還不錯的話，能否請咱喝一杯咖啡呢?  

![Pay-Total](./Pay-Total.png)

## 聯繫方式

```
微信: yuyangiit
郵箱: yuyangit.0515@qq.com
```