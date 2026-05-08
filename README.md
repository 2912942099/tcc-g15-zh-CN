# Dell G15 tcc-g15中文汉化版散热控制中心

[中文汉化版下载地址](https://github.com/2912942099/tcc-g15-zh-CN)（注意：应用程序需要管理员权限）

<img width="400" alt="主界面" src="https://github.com/user-attachments/assets/beb92c93-9891-44e1-a5e6-461888db7053" />

&nbsp;
<img width="150" alt="托盘菜单" src="https://github.com/user-attachments/assets/224b8654-271b-4a4d-a032-2e58387303e9" />

基于 [AlexIII/tcc-g15](https://github.com/AlexIII/tcc-g15) 的中文汉化版本

原项目是 Alienware Control Center (AWCC) 的开源替代品

[原项目地址](https://github.com/AlexIII/tcc-g15)

## 支持机型

已确认支持的机型（用户反馈）：
- Dell G15：5511、5515、5520、5525、5530、5535、5590
- Dell Alienware m16 R1
- Dell G3 3590、G3 15 3500
- Dell Alienware 16X Aurora

其他 Dell G15 / Alienware 笔记本也可能兼容。

如果你测试过是否可用，欢迎反馈。

## 功能

- 切换散热模式（均衡模式 / G模式 / 自定义）
- 显示 GPU/CPU 温度和风扇转速
- 半手动风扇转速控制
- 高温自动切换 G 模式（安全保护）
- 支持键盘 G 模式热键（Fn+F9）
- 开机自启（默认禁用）

## 使用说明

1. 下载 exe 文件，以管理员身份运行
2. 托盘图标右键可切换模式、启用/禁用开机自启
3. 双击托盘图标可打开主界面
4. 主界面可查看温度、风扇转速，调整安全保护阈值

### 安全保护

当 GPU 温度 ≥ 85°C 或 CPU 温度 ≥ 95°C 持续 8 秒后，自动切换到 G 模式（风扇全速）。温度恢复正常 60 秒后自动恢复原模式。可在主界面调整温度阈值。

### 卸载说明

如需卸载，请先在托盘菜单中**禁用开机自启**，再删除 exe 文件，否则会有残留的计划任务和配置文件。

如已直接删除 exe，可手动清理：
```cmd
schtasks /delete /tn "TCC_G15" /f
del %USERPROFILE%\tcc_g15_task_patched.xml
