[油猴脚本链接](https://greasyfork.org/en/scripts/531799-%E5%B0%8F%E9%BB%91%E7%9B%92%E8%AF%84%E8%AE%BA%E5%8C%BA%E6%8A%BD%E5%A5%96)

最近发现在小黑盒 roll 游戏帖子中，大家还在用传统的随机数方式。我记得最开始的时候还有显示楼层的功能，后面不知道什么时候删除了，只能通过倒序或者顺序查看评论区回复；而且如果回复参与数量很多又或是开奖数量多的话，找对应的楼层比较麻烦。

![1](https://github.com/user-attachments/assets/35521ce3-57b9-4679-8916-e1de3a0bc8b5)
正好上周我自己创建了一个关于“研究生复试送祝福”的 roll 贴，于是自己研究了一下，决定做一个小工具方便 roll 奖。黑盒帖子是有防爬取的设定，如果用抓包什么的一个是本身很麻烦，其次就是如果有人也想用学习成本很高，最后决定用网页版做一个油猴 js 脚本来实现，目前工具已经上传 greasyfork 供学习下载使用。浏览器油猴插件使用方法请自行搜索，黑盒有很多教程了。

![6](https://github.com/user-attachments/assets/39347fa3-127a-4654-9299-e111d6ffc4c5)
下面讲讲原理和使用方法：
使用网页端小黑盒，在[小黑盒开放平台](https://open.xiaoheihe.cn/zh_cn/home)右边头像我的主页。找到自己发布的帖子。

![heihe1](https://github.com/user-attachments/assets/4b81f34f-9758-4ffd-aa10-7c866a72ef85)
下拉评论区，让它全部加载，方便后续一次性获取，每次应该是默认加载 20 条左右，中途有概率弹出验证码（为了反爬这方面做的挺好的，就是我有时候手机正常刷评论区也要验证，可能是我账号被风控的问题）。

![2](https://github.com/user-attachments/assets/7857dfad-bb26-4ed6-beae-812fd05be5d3)
到了最下面之后点击页面右下角我设置的按钮，会获取页面中所有的评论所属 div，将里面的用户名+个人资料链接+评论内容提取到一个 Map 里。Map 内容放到记事本里面直观大概是这样的：

![4](https://github.com/user-attachments/assets/d9d17c85-2a9e-4409-9011-768f98e734b8)
最后选择你的开奖数量。注意：如果你允许多次评论，那么有可能抽中多次某个人的多个评论，如果不想这样的话，自行修改一下代码。

![3](https://github.com/user-attachments/assets/2bf3b71d-a0e6-4520-8005-5db5331571d3)

![5](https://github.com/user-attachments/assets/e0050dd3-9166-46f9-aa4d-26dd4f68ca5b)
开奖后显示随机抽中的用户名+个人资料地址（用于方便你联系中奖者呀）+评论内容。由于我的帖子还没开奖，就先打码了，大致示例输出如下：

![11](https://github.com/user-attachments/assets/248a7284-809b-40ce-a201-e245aff2d138)
如果有问题欢迎讨论交流，谢谢！
