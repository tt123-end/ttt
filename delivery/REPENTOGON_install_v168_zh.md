# 猎手v1.68：忏悔+与REPENTOGON

当前用户环境为忏悔+＋REPENTOGON，本版所需接口已核对官方1.1.3源码。官方Launcher负责匹配运行版本；不要把普通忏悔的1.0.12 DLL包混装到忏悔+。

- 官方Launcher：https://github.com/TeamREPENTOGON/Launcher/releases/latest
- 官方中文安装与存档迁移说明：https://github.com/TeamREPENTOGON/REPENTOGON/blob/1.1.3/docs/docs/install_zh.md
- 原生Weapon接口：https://github.com/TeamREPENTOGON/REPENTOGON/blob/1.1.3/docs/docs/Weapon.md
- 原生挥剑、受伤、激光回调：https://github.com/TeamREPENTOGON/REPENTOGON/blob/1.1.3/docs/docs/enums/ModCallbacks.md

猎手安装：完全退出游戏，备份移出旧模组文件夹，完整解压本包到mods，只保留一份启用版本。通过对应Launcher启动，在测试局输入hunterdiag，应显示[Hunter v1.68] REPENTOGON=true。

本版英灵剑改为真实主武器的原生蓄满释放，不再创建缺少Spin素材的普通飞刀实体。三圣颂沿用已确认的实际命中增伤链并改为8倍，科技主激光基础为400%面板伤害。诊断显示的是实际incoming/applied及原生释放阶段；历史v1.66说明中要求BaseDamage=67.2的检查已不适用。

本包不包含第三方DLL；本地验证是接口和逻辑模型，不是游戏实测结果。
