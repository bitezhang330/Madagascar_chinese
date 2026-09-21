# Madagascar 中文化说明

本仓库基于 Madagascar 主源码，并对旧版 **tkMadagascar** 图形界面进行了简体中文本地化。

## 本次汉化范围

主要修改目录：

`framework/rsf/gui`

涉及文件：

- `Browser.py`：程序浏览器、搜索、Flow/Plot/Result 添加按钮与提示
- `Flow.py`：参数编辑、预览、文档、连接错误提示
- `Gui.py`：文件/视图/运行菜单、状态保存与加载、日志和进程提示
- `Parameter.py`：参数校验提示
- `Program.py`：程序自文档中的名称、用法、使用位置、另请参阅
- `Sandbox.py`：连接、取消连接、删除及右键菜单

## 汉化原则

本次改动只处理用户可见界面文字，尽量不改变 Madagascar 的处理逻辑。

以下内容继续保留英文：

- `sf*` 程序名
- Madagascar 参数名
- `Flow / Plot / Result` 内部类型语义
- `SConstruct`
- `scons`、`scons view`、`scons lock`、`scons -c`、`scons -n`

这样可以避免中文化影响已有处理脚本和命令兼容性。

## 编码兼容

tkMadagascar 属于较早期的 Python/Tkinter GUI 代码。本次中文化：

- 为修改后的 Python 文件加入 UTF-8 编码声明
- 中文界面字符串使用 Unicode 字面量
- 不修改原有算法与流程构建逻辑

## 入口

tkMadagascar 相关代码位于：

`framework/rsf/gui`

其中 `Gui.py` 为主 GUI 类，`Browser.py` 为 Madagascar 程序浏览器。

## 后续建议

后续可继续进行两类改进：

1. 完善剩余少量英文提示和程序说明的中文化；
2. 将旧版 Tkinter GUI 迁移为 Python 3 / tkinter，并针对 Windows 环境增加更友好的启动器。
