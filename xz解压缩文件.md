### 1. xz 压缩文件方法或命令 

```shell
$ xz -z 要压缩的文件
```

如果要保留被压缩的文件加上参数 `-k` ，如果要设置压缩率加入参数 `-0` 到 `-9` 调节压缩率。如果不设置，默认压缩等级是 6.

### 2. xz 解压文件方法或命令 

```shell
$ xz -d 要解压的文件
```

同样使用 `-k` 参数来保留被解压缩的文件。

### 3. 创建或解压 tar.xz 文件的方法 

习惯了 `tar czvf` 或 `tar xzvf` 的人可能碰到 `tar.xz` 也会想用单一命令搞定解压或压缩。其实不行 `tar` 里面没有征对 `xz` 格式的参数比如 `-z` 是针对 `gzip`，`-j`是针对 [bzip2](https://www.baidu.com/s?wd=bzip2&tn=24004469_oem_dg&rsv_dl=gh_pl_sl_csd)。

创建 `tar.xz` 文件：

```shell
$ tar cvf xxx.tar xxx/
$ xz -z xxx.tar   # 将 xxx.tar 压缩成为 xxx.tar.xz
```

解压 `tar.xz` 文件：

```shell
$ xz -d xxx.tar.xz   # 将 xxx.tar.xz 解压成 xxx.tar
$ tar xvf xxx.tar
```

