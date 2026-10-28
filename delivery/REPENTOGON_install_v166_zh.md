# 猎手原生旋斩：REPENTOGON 下载与使用

先查看游戏的完整版本号。普通忏悔与忏悔+使用不同的REPENTOGON版本，不能混装。以下链接均为官方项目地址；2026-10-28已核对发布页及源码接口。

## 普通忏悔：v1.7.9b.J835

使用官方旧版 **REPENTOGON 1.0.12**。已确认该版本提供本次猎手使用的SetIsSpinAttack和SetIsSwinging接口，无需为了旋斩升级到忏悔+。

- 发布页：https://github.com/TeamREPENTOGON/REPENTOGON/releases/tag/1.0.12
- 官方ZIP直接下载：https://github.com/TeamREPENTOGON/REPENTOGON/releases/download/1.0.12/REPENTOGON.zip
- 对应版本的官方安装说明：https://github.com/TeamREPENTOGON/REPENTOGON/blob/1.0.12/docs/docs/install.md

Windows安装：

1. 退出以撒。
2. Steam库右键《The Binding of Isaac: Rebirth》→属性→已安装文件→浏览，找到包含 **isaac-ng.exe** 的游戏安装目录。
3. 将REPENTOGON.zip里的**内容**直接解压到这个目录。不要放进mods，也不要在外面再套一个REPENTOGON文件夹。解压后dsound.dll、libzhl.dll、Lua5.4.dll、zhlREPENTOGON.dll、freetype.dll等应与isaac-ng.exe同级，resources及resources-repentogon按包内路径合并。
4. 正常从Steam启动游戏。窗口标题应出现 **+ REPENTOGON**，游戏目录会生成zhl.log及repentogon.log；只有在mods列表勾选某个同名MOD并不等于完成DLL安装。
5. 将猎手v1.66里的zzzz_revolver_samson替换旧版，放到原来的mods目录，只启用一份猎手。进入里猎手、获得英灵剑，在非换弹期间射击测试原生满蓄力旋斩；满血剑气照常保留。

临时停用：在Steam启动选项添加 **-repentogonoff**；重新启用时删除这个选项。无需为了停用而删除猎手或存档。

该旧版官方说明只支持v1.7.9b.J835；其他本体版本不应直接套用此安装包。不要使用“最新版”链接来替代上面固定的1.0.12链接，因为当前最新1.1.x已面向忏悔+。

Linux/Steam Deck：该旧版官方说明要求使用Windows版游戏/Proton，并在Steam启动选项设置 `WINEDLLOVERRIDES="dsound=n,b" %command%`。Windows无需这个选项。

## 如果你的游戏实际是忏悔+

使用官方Launcher路线，不要安装上面的1.0.12包：

- 启动器官方下载：https://github.com/TeamREPENTOGON/Launcher/releases/latest
- 官方中文说明：https://repentogon.com/install_zh.html
- 若网站无法打开，可读相同官方仓库中的说明：https://github.com/TeamREPENTOGON/REPENTOGON/blob/main/docs/docs/install_zh.md

Windows下把启动器解压到游戏安装目录之外的独立文件夹，运行REPENTOGONLauncher.exe，选择忏悔+的isaac-ng.exe，按启动器提示安装并确认兼容状态。之后通过启动器启动。当前官方文档基于忏悔+v1.9.7.12.J273，并支持从Steam当前忏悔+版本由启动器准备兼容环境；由启动器处理版本匹配，不要混装普通忏悔的DLL包。

## v1.66行为与检查

英灵剑需要成功加载上述旋斩接口。接口不可用时，本版保留飞刀和满血剑气，**不会再显示上一版的模拟挥砍**。三圣颂、死亡之眼、专用巧克力牛奶和剖腹产不要求REPENTOGON；其中后面三项保留你已经确认正常的实现。

可选控制台命令 **hunterdiag** 会显示原生剑接口状态，以及三圣颂创建时的factor、BaseDamage和CollisionDamage。初始面板4.2、无其他单发增伤时，16倍三圣颂的BaseDamage应为67.2；原版光束仍按原生单段比例和命中频率结算，不代表每段都等于67.2。死亡之眼、牙齿等原生单发加成会在此基础上改变数值。

本次仅下载检查了官方ZIP结构、CRC和接口源码，没有在本环境运行游戏或安装第三方DLL。猎手包不夹带REPENTOGON二进制。
