<!--
 * @Author: yuyangit yuyangit.0515@qq.com
 * @Date: 2024-10-18 13:21:27
 * @LastEditors: yuyangit yuyangit.0515@qq.com
 * @LastEditTime: 2024-10-24 19:51:45
 * @FilePath: /xy_dict/readme/README_en.md
 * @Description: 这是默认设置,请设置`customMade`, 打开koroFileHeader查看配置 进行设置: https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE
-->
# xy_dict

- [简体中文](README_zh_CN.md)
- [繁体中文](README_zh_TW.md)
- [English](README_en.md)

## Description
Dict tools.

## Source Code Repositories

- <a href="https://github.com/xy-base/xy_dict.git" target="_blank">Github</a>  
- <a href="https://gitee.com/xy-opensource/xy_dict.git" target="_blank">Gitee</a>  
- <a href="https://gitcode.com/xy-opensource/xy_dict.git" target="_blank">GitCode</a>  

## Installation

```bash
# bash
pip install xy_dict
```

## How to use


```python

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

## License
xy_dict is licensed under the <Mulan Permissive Software License，Version 2>. See the [LICENSE](../LICENSE) file for more info.

## Donate

If you think these tools are pretty good, Can you please have a cup of coffee?  

![Pay-Total](./Pay-Total.png)  


## Contact

```
WeChat: yuyangiit
Mail: yuyangit.0515@qq.com
```