# Disillusion ：基于生成模型的开源欺骗防御产品

[English Version](https://github.com/SECSpell/Disillusion/blob/main/README.md)

Disillusion（aka幻灭咒）是一款针对Linux主机，尤其是容器使用场景进行设计的欺骗防御工具。利用生成模型的仿真能力，为主机带去一种新的“蜜饵”形态----命令蜜饵。

蜜饵（honeybait）是一种在欺骗防御中广泛采用的防御手段。通常为各种格式的文件，用敏感信息吸引攻击者的关注，利用文件信息引导攻击者进入蜜网；或者当蜜饵文件被打开时，就能触发防御者相关的告警能力。

蜜饵的优点和缺点都极其明显！

最吸引人的优点是就是它除了占用一点点存储空间外，几乎不产生任何额外的性能开销。

让人比较失望的地方是过于被动，尤其是当攻击者提高了自己的警惕时，蜜饵很难让攻击者中招。

而大模型时代，为我们带来了开发 Disillusion的想法。利用生成模型的仿真能力，针对攻击者信息收集场景，一个文件就能带来很好的欺骗防御效果。

## 原理

Linux 系统环境变量中，通常会配置有多个指向执行文件目录的配置项。我们通过在“执行优先级”更高的目录中，放置 Disillusion，就能实现“劫持”通用命令执行的目的。

劫持命令后，一方面对防御者进行告警，**另一方面利用大模型的仿真能力，误导、迷惑和拖延攻击者的攻击。**

使用方法只需简单几步：

1. 配置 config 文件
2. 复制disillusion 至高优先级目录
3. 修改disillusion的文件名
4. 等待……

视频演示：

https://v.qq.com/x/page/x3536kwwhr3.html


