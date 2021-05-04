# Office365-Global-Management
Office365 全局管理（新建、删除、禁用子用户，提升子用户管理权）


1.多全局集中管理（登录可选、管理页可切换）
2.不使用数据库，数据用api获取
3.新建账号、删除、禁用、提权等。。。

强调一下，这个管理要基于几个权限（见论坛其他贴）也就是说提权这些操作的api权限需要管理账号授权。
作用是开好api权限以后，可以用这个php管理，当管理被封的时候也可以给任一账户提权为管理员。
不是用来给买了域名发现有管理提权的！

程序入口admin.php
配置文件config.php（只要改这个，accounts是一个数组，多个全局的配置分别写这里）

账号API授权：
主要是RoleManagement.ReadWrite.Directory（务必保证权限正确开启），而且你的SPO没有被封禁（子账号的onedrive可以正常使用）
附上权限图：
![c4Lmp8](https://user-images.githubusercontent.com/68975045/116994043-d339f080-ad0a-11eb-9821-595d4b2e9c5e.jpg)


官方api教程：
        https://docs.microsoft.com/en-us ... view=graph-rest-1.0

脚
