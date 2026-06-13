# iOS 越狱 Stash 目录说明
iOS 设备越狱后，为缓解**系统分区存储空间紧张**，越狱工具与 Cydia 会自动将系统分区内体积较大的程序、资源目录迁移至用户分区，并在原路径创建**符号链接（软链接，对应 Windows 快捷方式）**，保证系统正常调用。

## 一、常规迁移目录清单
以下为默认迁移的系统目录，原始路径均位于系统分区：
| 目录用途 | 原始系统路径 |
| ---- | ---- |
| 系统应用 | `/Applications` |
| 系统铃声 | `/Library/Ringtones` |
| 系统壁纸 | `/Library/Wallpaper` |
| PAM 认证模块 | `/usr/lib/pam` |
| 共享资源 | `/usr/share` |
| 头文件目录 | `/usr/include` |
| Activator 手势配置 | `/Library/Activator` |
| 主题资源 | `/Library/Themes` |

## 二、Stash 存储路径说明
所有迁移文件统一存放至用户分区 `stash` 目录，路径随 Cydia 版本迭代调整：
1. **Cydia 1.1.16 及更早版本**
   表层路径：`/var/stash`
   真实物理路径：`/private/var/stash`
   备注：`/var` 本身为软链接，实际指向 `/private/var`

2. **Cydia 1.1.16 之后版本**
   为修复 iTunes 备份恢复后设置密码引发的白苹果问题，路径变更为：
   真实物理路径：`/private/var/db/stash`

## 三、两种迁移规则
### 1. 通用越狱方案
将原系统目录迁移至 `/var/stash` 下，**目录名追加随机字符后缀**，示例：
- 原路径：`/Library/Ringtones`
- 迁移后路径：`/var/stash/Ringtones.FG56e`
原位置保留软链接，维持原有访问逻辑。

### 2. 盘古越狱专属方案
迁移逻辑略有差异，执行流程：
1. 在 `/var/stash` 内创建随机命名文件夹；
2. 将原系统目录整体移入该随机目录；
3. 在原系统路径创建软链接指向新位置；
4. 在 `/var/stash` 生成同名 `.lnk` 链接文件（前台不显示后缀），文件内记录目录原始路径与名称。
