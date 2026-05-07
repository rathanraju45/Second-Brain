# LiefOS Page

Title: LifeOS
Purpose: To manage the Life using the Second Brain

- Callout box titled [Dashboard](#dashboard) meant for showing metrics, currently empty
- Callout box titled [Projects](#projects) having Linked Views of Projects DB namely - [Today](#projects-today-view), [This Week](#projects-this-week-view), [This Month](#projects-this-month-view), [Finished](#projects-finished-view), [All](#projects-all-view)
- Callout box titled [Tasks](#tasks) having Linked Views of Tasks DB namely - [Today](#tasks-today-view), [This Week](#tasks-this-week-view), [This Month](#tasks-this-month-view), [Finished](#tasks-finished-view), [All](#tasks-all-view)
- Callout box titled [Calendar](LifeOS.md#calendar) having Linked Views of Tasks DB, Projects DB namely - [Pending Tasks](#calendar-pending-tasks), [Finished Tasks](#calendar-finished-tasks), [All Tasks](#calendar-all-tasks), [Pending Projects](#calendar-pending-projects), [Finished Projects](#calendar-finished-projects), [All Projects](#calendar-all-projects)

## Dashboard

Currently Empty Will Design in future

## Projects

Purpose: To display the Projects Database in differenet views

<a id="projects-today-view"></a>

### Today View

Purpose: To display the Projects Pending Today

| Setting | Value |
|---------|-------|
| Layout | Gallery |
| Properties Visible | Project Name, Overview, Deadline Comparitive, Progress |
| Filters | Progress != 1, Deadline is Today |
| Sorts | Ascending order by Project Name |
| Conditional Color | Time Deviation >= 0 → Card background: green; Time Deviation < 0 → Card background: red |

<a id="projects-this-week-view"></a>

### This Week View

Purpose: To display the Projects Pending This Week

| Setting | Value |
|---------|-------|
| Layout | Gallery |
| Properties Visible | Project Name, Overview, Deadline Comparitive, Progress |
| Filters | Progress != 1, Deadline is This Week |
| Sorts | Ascending order by Project Name |
| Conditional Color | Time Deviation >= 0 → Card background: green; Time Deviation < 0 → Card background: red |

<a id="projects-this-month-view"></a>

### This Month View

Purpose: To display the Projects Pending This Month

| Setting | Value |
|---------|-------|
| Layout | Gallery |
| Properties Visible | Project Name, Overview, Deadline Comparitive, Progress |
| Filters | Progress != 1, Deadline is This Month |
| Sorts | Ascending order by Project Name |
| Conditional Color | Time Deviation >= 0 → Card background: green; Time Deviation < 0 → Card background: red |

<a id="projects-finished-view"></a>

### Finished View

Purpose: To display the Projects Finished

| Setting | Value |
|---------|-------|
| Layout | Gallery |
| Properties Visible | Project Name, Date, Duration, Time Deviation |
| Filters | Progress = 1 |
| Sorts | Ascending order by Project Name |
| Conditional Color | Time Deviation = 0 → Card background: Default;Time Deviation > 0 → Card background: green; Time Deviation < 0 → Card background: red |

<a id="projects-all-view"></a>

### All View

Purpose: To display all the Projects

| Setting | Value |
|---------|-------|
| Layout | Gallery |
| Properties Visible | Project Name, Date, Overview, Deadline Comparitive, Progress, Duration, Time Deviation |
| Sorts | Ascending order by Project Name |
| Conditional Color | Time Deviation = 0 → Card background: Default;Time Deviation > 0 → Card background: green; Time Deviation < 0 → Card background: red |

## Tasks

Purpose: To display the Tasks Database in different views

<a id="tasks-today-view"></a>

### Today View

Purpose: To display the Tasks Pending Today

| Setting | Value |
|---------|-------|
| Layout | List |
| Properties Visible | Status, Start Log, End Log, Start Date, End Date, Task Name, Deadline |
| Filters | Status is unchecked, Deadline is Today |
| Sorts | Ascending order by Task Name & Start Date |
| Group | Group by Projects DB |

<a id="tasks-this-week-view"></a>

### This Week View

Purpose: To display the Tasks Pending This Week

| Setting | Value |
|---------|-------|
| Layout | List |
| Properties Visible | Status, Start Log, End Log, Start Date, End Date, Task Name, Deadline |
| Filters | Status is Unchecked, Deadline is This Week |
| Sorts | Ascending order by Task Name & Start Date |
| Group | Group by Projects DB |

<a id="tasks-this-month-view"></a>

### This Month View

Purpose: To display the Tasks Pending This Month

| Setting | Value |
|---------|-------|
| Layout | List |
| Properties Visible | Status, Start Log, End Log, Start Date, End Date, Task Name, Deadline |
| Filters | Status is Unchecked, Deadline is This Month |
| Sorts | Ascending order by Task Name & Start Date |
| Group | Group by Projects DB |

<a id="tasks-finished-view"></a>

### Finished View

Purpose: To display the Tasks Finished

| Setting | Value |
|---------|-------|
| Layout | List |
| Properties Visible | Status, Start Log, End Log, Start Date, End Date, Task Name, Deadline, Duration |
| Filters | Status is Checked |
| Sorts | Ascending order by Task Name & Projects DB, Descending Order by End Date |
| Group | Group by Projects DB |

<a id="tasks-all-view"></a>

### All View

Purpose: To display all the Tasks

| Setting | Value |
|---------|-------|
| Layout | List |
| Properties Visible | Status, Start Log, End Log, Start Date, End Date, Task Name, Deadline, Duration |
| Sorts | Ascending order by Task Name & Projects DB, Descending Order by End Date |
| Group | Group by Projects DB |

## Calendar

Purpose: To display the Projects Database, Tasks Database in different views on Calendar

<a id="calendar-pending-tasks"></a>

### Pending Tasks

Purpose: To display pending Tasks on calendar

| Setting | Value |
|---------|-------|
| Layout | Calendar |
| Properties Visible | Task Name, Projects DB,  Start Log, End Log|
| Filters | Status is Unchecked |
| Sorts | Ascending order by Task Name & Projects DB |
| Group | Group by Projects DB |

<a id="calendar-finished-tasks"></a>

### Finished Tasks

Purpose: To display finished Tasks on calendar

| Setting | Value |
|---------|-------|
| Layout | Calendar |
| Properties Visible | Task Name, Projects DB, Duration|
| Filters | Status is Checked |
| Sorts | Ascending order by Task Name & Projects DB, Descending Order by End Date |
| Group | Group by Projects DB |

<a id="calendar-all-tasks"></a>

### All Tasks

Purpose: To display all Tasks on calendar

| Setting | Value |
|---------|-------|
| Layout | Calendar |
| Properties Visible | Task Name, Projects DB, Duration|
| Sorts | Ascending order by Task Name & Projects DB, Descending Order by End Date |
| Group | Group by Projects DB |

<a id="calendar-pending-projects"></a>

### Pending Projects

Purpose: To display pending Projects on calendar

| Setting | Value |
|---------|-------|
| Layout | Calendar |
| Properties Visible | Project Name, Deadline Comparitive, Progress, Calendar Overview |
| Filters | Progress != 1 |
| Sorts | Ascending order by Project Name |

<a id="calendar-finished-projects"></a>

### Finished Projects

Purpose: To display finished Projects on calendar

| Setting | Value |
|---------|-------|
| Layout | Calendar |
| Properties Visible | Project Name, Deadline Comparitive, Calendar Overview, Duration |
| Filters | Progress = 1 |
| Sorts | Ascending order by Project Name |

<a id="calendar-all-projects"></a>

### All Projects

Purpose: To display all Projects on calendar

| Setting | Value |
|---------|-------|
| Layout | Calendar |
| Properties Visible | Project Name, Deadline Comparitive, Calendar Overview, Progress, Duration |
| Sorts | Ascending order by Project Name |