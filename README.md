# rime-wubi-simp

根据 [rime/rime-wubi#8](https://github.com/rime/rime-wubi/issues/8) 提出的解决方案。

Rime 五笔的默认词库包含很多繁体字，如果我的理解没错，当前对简体字处理是在输出时转换，这样会导致输入 `tvfh`，出现 `笔（ttfn）`的尴尬。

这里根据现行最新标准[《通用规范汉字表》](http://www.gov.cn/zwgk/2013-08/19/content_2469793.htm) 对原词库 [wubi86.dict.yaml](https://github.com/rime/rime-wubi/blob/master/wubi86.dict.yaml) 作处理，删除所有不在汉字表的字符，生成 `wubi86_simp.dict.yaml`。

文件说明

- GB2312.txt

  GB2312 标准，共 6763 个中文字符，部分简体字如`啰 镕 喆`未被收录。

- 8105.txt

  通用规范汉字表，共 8105 个中文字符。（收录大部分 GB2312 字符，删去`矽 诶`等字符）

- wubi86_del.dict.yaml

  根据以上规范删除的词库。

- wubi86_simp.dict.yaml

  根据以上规范生成的词库，只修改名称，其它内容（版本号、规则）与原词库保持一致。
