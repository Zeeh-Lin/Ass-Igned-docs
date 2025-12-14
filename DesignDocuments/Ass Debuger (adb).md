## Commands Table

包含5条指令。

| Commands | Description                                         |
| -------- | --------------------------------------------------- |
| help     | Display information about all supported commands.   |
| quit     | Quit Ass-Igned.                                     |
| task     | To CRUD a task.                                     |
| ai       | A set of commands related to ai, such as `ai chat`. |
| rpt      | Generate weekly/monthly report.                     |

### `task`

包含一系列任务相关的子命令。

| Subcommands | Description                       |
| ----------- | --------------------------------- |
| add         | Create a task.                    |
| del         | Delete a task.                    |
| done        | Set a task's status to be `DONE`. |
| update      | Update a task's information.      |


### `ai`

包含一系列AI相关的子命令。

| Subcommands Name | Description  |
| ---------------- | ------------ |
| chat             | Chat with ai |
| sug              | AI suggest   |
| plan             | AI plan      |
| sum              | AI summaries |

### `rpt`

生成周报/月报。

| Subcommands Name | Description    |
| ---------------- | -------------- |
| week             | Weekly report  |
| month            | Monthly report |
