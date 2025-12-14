## Modules

| Name                  | Module Prefix | Description                                           |
| --------------------- | ------------- | ----------------------------------------------------- |
| **common**            | 无固定前缀         | **基础设施**。提供支持ANSI彩色格式的日志 `Log`、断言`Assert`等工具，以及常用宏定义。 |
| **database**          | `db_`         | **数据持久层**。封装数据库操作，负责数据的“落地”。                          |
| **parser**            | `psr_`        | **数据翻译层**。利用`cJSON`，负责结构体与 JSON 互转。                   |
| **monitor**           | `monitor_`    | **监控器**。处理用户输入、调用逻辑层。                                 |
| **assigned debugger** | `adb_`        | **简易调试器**。交互式命令行工具，负责用户交互，同时也是开发过程中的调试工具。             |
| **ai_client**         | `aic_`        | **AI连接器**。集成 `libcurl` 调用 DeepSeek API。               |
