25-11-28:
(1) 制定初步技术路线, 确定Naming Conventions, Commit Conventions. 引入Commitizen规范commit log, 便于团队协作开发. 
(2) 实现简单的log utils, 支持ANSI Color Code等功能. 
(3) 实现简单的交互式命令行调试器 `Ass-Igned Debugger` ( `adb` ), 该调试器支持基础的`help`, `q` (quit)等功能.

25-11-29:
(1) 为 `utils` 模块添加功能, 包括JSON文件的创建与解析(使用cJSON). 
(2) 使用 `curlib` 库实现与DeepSeek的通信, 实现 `AI_Clent` 模块 ( `aic_` ) 的基础功能.

25-11-30: 
(1) 重构了 `adb` 中的主命令执行函数, 让后续待添加的主命令可以复用一套基本的主命令执行框架; 在 `adb` 中实现简单的命令, 包括: `ai chat` 和DeepSeek聊天, 用于后续ai功能的快速验证; `task add` 让DeepSeek分析待办任务并返回JSON.
(2) 在 Makefile 中添加了一个使用 Valgrind 检查内存泄露的目标, 并用其修复了 ` task add` 命令中的内存泄露