# iOS 越狱 Stash 目录详解
越狱后为释放系统分区空间，工具会将系统大文件、应用、资源迁移至用户分区，并通过**软链接**保证正常使用。

## 迁移目录列表
- 系统应用：`/Applications`
- 系统铃声：`/Library/Ringtones`
- 系统壁纸：`/Library/Wallpaper`
- PAM 模块：`/usr/lib/pam`
- 共享资源：`/usr/share`
- 头文件：`/usr/include`
- 手势配置：`/Library/Activator`
- 主题资源：`/Library/Themes`

## 存储位置
- Cydia 1.1.16 及更早：`/private/var/stash`（`/var/stash` 为软链接）
- Cydia 1.1.16 之后（修复备份白苹果）：`/private/var/db/stash`

## 迁移格式
1. 常规越狱：目录名添加随机后缀，例：`Ringtones.FG56e`
2. 盘古越狱：在 `stash` 下新建随机目录存放文件，同时生成 `.lnk` 文件记录原始路径。
