

# Rollback-Mod

Minecraft  Forge 模组，提供强大的回滚系统和各种核心道具能力。

## 简介

Rollback-Mod 是一个为 Minecraft Forge 设计的服务器辅助模组，专注于提供灵活的回滚机制和多样化的核心道具系统。玩家可以使用多种"核心"道具来获得不同的能力，包括时间控制、标记目标、自我牺牲保护等高级功能。

## 核心道具

本模组提供 8 种核心道具，通过吸入器（Inhaler）使用时会产生不同效果：

| 核心类型 | 功能描述 |
|---------|----------|
| **Chronos Core** | 时间回溯核心，可减缓时间流逝 |
| **Disconnection Core** | 断开连接核心 |
| **Molting Core** | 蜕皮核心 |
| **Tower Core** | 塔之核心 |
| **Sand Core** | 沙土核心 |
| **Causality Core** | 因果核心，实现死亡回滚 |
| **Myriad Core** | 万象核心，防止死亡 |
| **Stasis Core** | 滞息核心，定格目标状态 |

## 主要功能

### 检查点与回滚系统
- 创建游戏检查点，记录当前世界状态
- 玩家死亡时可选择回滚到检查点
- 支持回滚所有玩家或仅回滚当前玩家
- 可配置首次世界加载时自动创建初始检查点

### 标记系统
-玩家可以使用核心标记实体（玩家或生物）
- 被标记的目标受到伤害时会触发相应效果
- 支持每玩家仅一个标记、标记目标死亡时清除等配置

### 时间控制
- 与时间时钟模组（Time Clock）兼容
- 可按键激活/关闭时间减缓效果
- 支持自定义时间减缓倍数

### HUD 显示
- 显示当前游戏天数
- 支持倒计时模式
- 天数过渡动画效果

## 配置选项

本模组通过 `rollbackmod.toml` 配置文件提供丰富的自定义选项：

```toml
# 回滚设置
enableDeathRollback = true          # 启用死亡回滚
destroyAllCoresOnRollback = false   # 回滚时销毁所有核心
saveOnFirstWorldLoad = true         # 首次加载时保存
rollbackAllPlayersOnDeath = false  # 死亡时回滚所有玩家
syncInventoryAndHealth = true      # 同步背包和生命值

# Chronos 设置
chronosDurationTicks = 12000        # Chronos 持续时间
chronosKeyMode = "toggle"           # 按键模式 (toggle/hold)
chronosSlowTimeFactor = 0.5        # 时间减缓倍数
requireTimeClockMod = false        # 是否需要时间时钟模组

# Stasis 设置
stasisDurationTicks = 24000         # Stasis 持续时间

# 标记设置
onlyOneMarkPerPlayer = true        # 每玩家仅一个标记
markLostWhenTargetDead = true       # 目标死亡时清除标记
myriadRequiresWeaponToPreventDeath = true # 万象核心需要武器才能防止死亡

# HUD 设置
showDayHUD = true                   # 显示天数 HUD
showDayTransition = true             # 显示天数过渡
countdownMode = false               # 倒计时模式
countdownDays = 30                 # 倒计时天数
```

## 安装方法

1. 下载本模组的 JAR 文件
2. 将 JAR 文件放入 Minecraft 服务端或客户端的 `mods` 文件夹中
3. 对于服务端，建议同时安装 `fabric-api`（如使用 Fabric）或对应版本的 `forge`
4. 启动游戏，配置文件将在首次运行后自动生成

## 使用方法

### 基础操作
1. **获取核心道具**：在创造模式标签页中找到对应核心物品
2. **使用核心**：手持吸入器，右键点击玩家或生物以应用核心效果
3. **创建检查点**：通过模组命令或游戏内交互创建
4. **触发回滚**：玩家死亡时自动回滚到检查点（如已启用）

### 按键绑定
- **Chronos 慢时间按键**：默认绑定，可自定义

## 兼容信息

- 本模组需要 Minecraft Forge 1.20.1 或更高版本
- 可选：安装 Time Clock 模组以启用更高级的时间控制功能

## 许可证

本模组遵守 MIT 许可证开源发布。

## 贡献者

感谢所有为本模组提供代码和 ideas 的开发者。