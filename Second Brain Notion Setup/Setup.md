# Second Brain - Home Page

Title: Second Brain
Purpose: Building a second brain

- Overview Explaining Second Brain
- Databases Page
- LifeOS Page

# Databases Page

Title: Databases
Purpose: To organize data in tables

- Callout Box Titled Projects Database having Database named Projects DB
- Callout Box Titled Tasks Database having Database named Tasks DB
- Callout Box Titled Images Database having Database named Images DB

<a id="projects-db"></a>

## Projects DB

Purpose: To store the data of the projects

### Properties

| Property Name | Type |
|---------------|------|
| [Start Log](#project-button-automations) | Button |
| [End Log](#project-button-automations) | Button |
| Project Name | Text |
| Tasks | Two way Relation |
| Date | Created time |
| [Progress](#rollup-system) | Rollup |
| [Overview](#project-overview) | Formula |
| Start Date | Date |
| End Date | Date |
| Deadline | Date |
| [Time Deviation](#project-time-deviation) | Formula |
| [Deadline Comparitive](#project-deadline-comparitive) | Formula |
| [Duration](#project-duration) | Formula |
| [Calendar Overview](#project-calendar-overview) | Formula |
| [Project Status](#project-project-status) | Formula |

<a id="project-button-automations"></a>

### Button Automations

1. Start Log - Enters Start Date
2. End Log - Enters End Date

### Rollup System

1. Progress
    - Relation - Tasks
    - Target Property - Status
    - Calculate - Percent Checked
    - Show as - Bar

### Property Formulae

<a id="project-overview"></a>

1. Overview

    ```
    lets(
    totalTasks, prop("Tasks").length(),
    finishedTasks, prop("Tasks").filter(current.prop("Status")).length(),
    unfinishedTasks, prop("Tasks").filter(not current.prop("Status")).length(),

    if(totalTasks == 0,
        "⚪ No tasks yet",
        
        "📊 Overview".style("b", "green") + "\n" +
        "🗂 Total: " + format(totalTasks) + "\n" +
        "✅ Finished: " + format(finishedTasks) + "\n" +
        "⏳ Pending: " + format(unfinishedTasks)
    )
    )
    ```

<a id="project-time-deviation"></a>

2. Time Deviation
    ```
    if(
    empty(prop("Deadline")),
    0,
    
    if(
        prop("Progress") == 1,
        
        /* COMPLETED → deviation */
        dateBetween(prop("Deadline"), prop("End Date"), "days"),
        
        /* NOT COMPLETED → time left */
        dateBetween(prop("Deadline"), now(), "days")
    )
    )
    ```

<a id="project-deadline-comparitive"></a>

3. Deadline Comparitive
    ```
    if(prop("Progress") == 1,
    "",
    lets(
        daysLeft, dateBetween(prop("Deadline"), now(), "days"),

        if(
        empty(prop("Deadline")),
        "",

        if(
            daysLeft == 0,
            "Due today",

            if(
            daysLeft > 0,
            format(daysLeft) + " days left",

            "Overdue by " + format(abs(daysLeft)) + " days"
            )
        )
        )
    )
    )
    ```

<a id="project-duration"></a>

4. Duration

    ```
    if(prop("Progress") == 1,
    lets(
        totalMinutes, dateBetween(prop("End Date"), prop("Start Date"), "minutes"),
    
        days, floor(totalMinutes / 1440),
        remainingMinutesAfterDays, mod(totalMinutes, 1440),
    
        hours, floor(remainingMinutesAfterDays / 60),
        minutes, mod(remainingMinutesAfterDays, 60),
    
        ifs(
        empty(prop("Start Date")) or empty(prop("End Date")), "",
        totalMinutes < 0, "Invalid: End before Start",
        totalMinutes == 0, "0m",
    
        days > 0 and hours == 0 and minutes == 0,
            format(days) + "d",
    
        days > 0 and hours > 0 and minutes == 0,
            format(days) + "d " + format(hours) + "h",
    
        days > 0,
            format(days) + "d " + format(hours) + "h " + format(minutes) + "m",
    
        hours > 0 and minutes == 0,
            format(hours) + "h",
    
        hours > 0,
            format(hours) + "h " + format(minutes) + "m",
    
        format(minutes) + "m"
        )
    ),
    ""
    )
    ```

<a id="project-calendar-overview"></a>

5. Calendar Overview
    ```
    lets(
    totalTasks, prop("Tasks").length(),
    finishedTasks, prop("Tasks").filter(current.prop("Status")).length(),

    if(
        totalTasks == 0,
        "⚪ No tasks",
        
        "✅ " + format(finishedTasks) + "/" + format(totalTasks)
    )
    )
    ```

<a id="project-project-status"></a>

6. Project Status

    ```
    if(
    prop("Progress") == 1,
    "Completed",

    if(
        now() > prop("Deadline"),
        "Overdue",

        "In Progress"
    )
    )
    ```

## Tasks DB

Purpose: To store the data of the tasks

### Properties

| Property Name | Type |
|---------------|------|
| Status | Checkbox |
| [Start Log](#task-button-automations) | Button |
| [End Log](#task-button-automations) | Button |
| Projects Relation | Relation inserted from the [Projects DB](#projects-db) |
| Task Name | Text |
| Date | Created time |
| Start Date | Date |
| End Date | Date |
| [Duration](#task-duration) | Formula |
| Deadline | Date |

<a id="task-button-automations"></a>

### Button Automations

1. Start Log - Enters Start Date
2. End Log - Enters End Date & Checks the status checkbox

### Property Formulae

<a id="task-duration"></a>

1. task-duration

    ```
    /* Only calculate time if task is marked as done */
    if(prop("Status"),
    lets(
        totalMinutes, dateBetween(prop("End Date"), prop("Start Date"), "minutes"),
    
        days, floor(totalMinutes / 1440),
        remainingMinutesAfterDays, mod(totalMinutes, 1440),
    
        hours, floor(remainingMinutesAfterDays / 60),
        minutes, mod(remainingMinutesAfterDays, 60),
    
        ifs(
        empty(prop("Start Date")) or empty(prop("End Date")), "",
        totalMinutes < 0, "Invalid: End before Start",
        totalMinutes == 0, "0m",
    
        days > 0 and hours == 0 and minutes == 0,
            format(days) + "d",
    
        days > 0 and hours > 0 and minutes == 0,
            format(days) + "d " + format(hours) + "h",
    
        days > 0,
            format(days) + "d " + format(hours) + "h " + format(minutes) + "m",
    
        hours > 0 and minutes == 0,
            format(hours) + "h",
    
        hours > 0,
            format(hours) + "h " + format(minutes) + "m",
    
        format(minutes) + "m"
        )
    ),
    /* Return empty if task not done */
    "" 
    )
    ```

## Images DB

Purpose: To store the images like coverpages, uploaded in google drive linked as URL's, and given tags like - Notion Cover Image

### Properties

| Property Name | Type |
|---------------|------|
| Name | Text |
| Image | URL |
| Tag | Select |