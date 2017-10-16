---
title: Project 2 Overview
layout: activity
---
### Overview

Project 2 provides you the opportunity to build a single page application. You will design the interface and screen states for a simple task management application. Then you'll use provided flowchart and data services to code the interactions. The application will include the following features:

* Account setup for new users
* Login form
* View all existing tasks and filter by category
* Add/edit/delete categories
* Add/edit/delete tasks

Consider these user stories to understand how the application should function ([app] is a placeholder for the app you're creating and will name as you see fit):

1. *SETUP:* Sarah wants a digital tool to help her keep track of her tasks from day to day. She finds [app] online and decides to create an account. She enters an email address and password to create her account. She sees a confirmation that her account has been created and proceeds to log in.
2. *ADDING TASKS:* Sarah now see an interface she quickly understands as the space that can hold any tasks she creates. She sees the option to create a task and clicks it. A dialogue appears that prompts her to enter the details for the task including its description, due date, category, and "task type." She's not sure what "category" and "task type" mean so she leaves them as-is. There is also a prominent box that she can tell allows her to mark the task as complete but that is not activated yet (logically since she's just now creating the task... she looks forward to changing that later). She saves the task and it appears on her overall task list in the application. She adds a few more tasks and begins to feel like she's getting the hang of it---and feels great that her mental task list is now looking manageable.
3. *COMPLETING TASKS:* Coming soon.
4. *CHANGING TAKS TYPE:* Coming soon.
5. *ADDING CATEGORIES:* Coming soon.
6. *MARKING OVERDUE TASKS:* Coming soon.

Tasks will include the following structure:

* Owner (defaults to current user)
* Description
* Due date (optional)
* Category (optional)
* Task type (preset from three types: normal (default), urgent, backburner)
* Completion status (toggle on or off)

Users will include the follow structure:

* Name
* Email
* Password (not readable by the API)
