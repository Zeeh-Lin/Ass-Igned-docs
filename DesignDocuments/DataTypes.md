## task_model.h

``` C
#include <time.h>

// File: utils/task_model.h

// -----------------------------------------------------------------------------
// ENUMERATIONS
// -----------------------------------------------------------------------------

/**
 * @brief Defines the status of a task for scheduling and display.
 */
typedef enum {
    TASK_STATUS_TODO = 0,
    TASK_STATUS_DOING = 1,
    TASK_STATUS_DONE = 2,
    TASK_STATUS_DELETED = 3
} task_status_e;

/**
 * @brief Defines the priority level of a task (for the Scheduler).
 */
typedef enum {
    PRIORITY_URGENT = 0,    // Highest priority, must be done now.
    PRIORITY_IMPORTANT = 1,
    PRIORITY_MEDIUM = 2,
    PRIORITY_LOW = 3        // Lowest priority.
} task_priority_e;

// -----------------------------------------------------------------------------
// CORE STRUCT
// -----------------------------------------------------------------------------

/**
 * @brief The core data structure for a single task item.
 */
typedef struct {
    int id;                // Database primary key (unique ID).
    char title[128];       // Task's brief title.
    char description[256]; // Detailed task information.
    time_t created_at;     // Timestamp when the task was created.
    time_t due_date;       // The required completion time (deadline).
    time_t completed_at;   // Unix timestamp of completion (0 if pending).
    task_priority_e prio;  // Priority level (used by the Scheduler).
    task_status_e stat;    // Current status of the task.
} task_t;
```
