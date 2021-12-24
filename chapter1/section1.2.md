# 一些常见问题

## 1、github 经常连接超时：

> 配置 DNS 可缓解此问题，步骤如下：

1.  寻找可用 ip：

    <http://ping.chinaz.com/github.com>，在这个网站 ping `github.com`,找到最快的一个 ip 地址；

2.  修改 host：

    `C:\Windows\System32\drivers\etc`，在该位置找到 host 文件，将上面找的 ip 地址，如`140.82.121.3 github.com`追加到 host 里面;

3.  刷新 DNS：

    **cmd** 里输入`ipconfig /flushdns`执行，完毕。
