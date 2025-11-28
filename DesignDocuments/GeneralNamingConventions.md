| **符号类型**       | **命名风格**                | **示例**                                             | **备注**                                                   |
| -------------- | ----------------------- | -------------------------------------------------- | -------------------------------------------------------- |
| **文件/模块**      | 小写 `snake_case`         | `storage.c`, `ai_client.h`, `core_utils.c`         | 文件名即模块名，保持简洁。                                            |
| **公共函数 (API)** | `MOD_function_name`     | `sch_push(task_id)`, `stg_add_task()`, `cli_run()` | 强制使用模块缩写前缀 (`sch_`, `stg_`, `cli_`)，清晰标明函数归属。            |
| **私有函数**       | `_module_function_name` | `_sch_heapify_down(index)`, `_stg_open_db()`       | 使用**下划线**作为前缀，暗示此函数仅在当前 `.c` 文件内使用。                      |
| **结构体**        | `type_name_t`           | `task_t`, `task_node_t`                            | 推荐使用 `_t` 后缀（来源于 POSIX 标准），清晰表明是 `typedef struct` 定义的类型。 |
| **枚举**         | `type_name_e`           | `status_e`, `log_level_e`                          | 推荐使用 `_e` 后缀，或将枚举成员命名为全大写。                               |
| **宏/常量**       | `ALL_CAPS_SNAKE_CASE`   | `MAX_TAG_COUNT`, `AI_API_TIMEOUT_SEC`              | 必须使用全大写，区分于变量。**全局常量**可考虑项目前缀 `AIT_`。                    |
| **变量**         | 小写 `snake_case`         | `current_time`, `priority_value`, `db_handle`      | 保持小写和下划线，除非是循环计数器 `i, j, k`。                             |
