# 1 路径或是cvx问题

>   SDPT3: unexpected error:
    错误使用 cd
    无法将目录更改为 F:\总结\论文代码\MIN1PIPE\utilities\cvx\shims (名称不存在或不是目录)。
    错误使用 cvx_global (line 143)
    All solvers were disabled due to various errors.
    Please re-run CVX_SETUP and, if necessary, contact CVX Research for support.

- 解决方案

将路径MIN1PIPE-master修改为MIN1PIPE; 最好使用git进行代码下载避免该问题

    可能是路经不对，MIN1PIPE-master命名时并未能将下载的cvx相关的代码加入到路径中。

# 2 数组索引必须为正整数或逻辑值。

> 数组索引必须为正整数或逻辑值。
>    
>   出错 data_info (line 20)
>            ids = ids(end);

视频名字全部为数字时，以下正则提取公式导致的 data_info (line 19，20)：

```matlab

    ids = regexp(file_name{i}(1: end - 4), '[^\d]');
    ids = ids(end);
```

- 解决方案

修改文件名
