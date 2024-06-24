# IAHD Lifestyle Life Manager
#### Description: Productivity App

## Screenshots of Web App

#### Register Page
![Homepage](/screenshots/register.png)

#### Login Page
![Homepage](/screenshots/login.png)

#### Homepage/Calendar
![Homepage](/screenshots/index-page.png)

#### Task List Page
![Homepage](/screenshots/task_list.png)

#### Time Tracker Page
![Homepage](/screenshots/time-tracker.png)

#### Notes Page
![Homepage](/screenshots/Notes.png)

#### Video Notes Page
![Homepage](/screenshots/video_notes.png)

#### Folders Page
![Homepage](/screenshots/Folders.png)

## Motivation behind the Project

Here's a rephrased version that mentions the IAHD Lifestyle Hackathon:
For the IAHD Lifestyle Hackathon, I developed a personalized Flask-based web application to enhance my daily productivity. While the individual features aren't novel, this project combines tools that are specifically tailored to my needs. A unique aspect is its integration with my Chrome extensions and a custom multi-device time tracker, which sets it apart from existing solutions.
This webapp isn't designed for wider distribution due to its highly personalized nature. However, it addresses my specific use cases and has potential for future expansion as my requirements evolve. While similar functionality could potentially be replicated in platforms like Notion, this custom solution offers unparalleled flexibility and a deep understanding of its inner workings.

## Features [Not Updated! See Screenshots for Better View of Current State of Project]

For the IAHD Lifestyle Hackathon, I've developed a "Life Manager" web application that combines five essential productivity features in a streamlined interface. This Flask-based app, inspired by the Finance web app from problem set 9, utilizes Python, HTML, CSS, Bootstrap, JavaScript, and SQLite3. Additional background functionality is implemented primarily in Python. The key components of this personal productivity tool include:

1. A customizable agenda displaying schedules for a user-defined number of days on the homepage.
2. A curated collection of notes from watched YouTube videos.
3. A task list for managing activities without specific time constraints, complementing the time-based agenda.
4. A comprehensive time tracker that:
* a) Presents daily activities in customizable categories using a Gantt chart.
* b) Provides a detailed log of apps and web pages accessed throughout the day. 
5. A dedicated Notes page for quick capture of thoughts and ideas.

This project, tailored for the IAHD Lifestyle Hackathon, aims to streamline daily productivity management in a personalized and efficient manner.

#### The Agenda

I've implemented an Agenda feature in my Life Manager app. This straightforward yet effective component allows users to:

1. Input future events with specific dates, times, and descriptions
2. Store event data in a SQLite database, managed through the app.py file
3. Display upcoming events on the homepage

The number of days shown is customizable, allowing users to view their schedule as far ahead as they prefer. This Agenda serves as a core organizational tool, helping users visualize and manage their upcoming commitments efficiently.

#### The Video Notes

For the IAHD Lifestyle Hackathon, I developed a Video Notes feature in my Life Manager app to address the issue of losing valuable insights from watched videos. Here's an overview of this component:

1. Utilizes the TubersLab Chrome extension for taking notes while watching videos
2. Leverages TubersLab's API to retrieve stored notes
3. Implements a Python script using the requests library to fetch data from the API
4. Processes the JSON-formatted data and stores relevant information in the app's database
5. Displays the collected notes on a dedicated page within the app

Challenges and considerations:

* Device-specific API requests require conditional logic based on the user's device
* Potential legal concerns regarding the use of TubersLab's API
* Need for improved note organization and display as the collection grows
* Originally planned to develop a custom extension, but opted for TubersLab due to time constraints

This feature aims to preserve and organize insights gained from video content, enhancing long-term learning and retention for the user.

#### The Task List

I implemented a straightforward Task List feature in the Life Manager app. This component is inspired by the "birthdays" page from a previous problem set and includes:

1. An SQLite3 table to store tasks
2. A dedicated page displaying all tasks
3. Functionality to add new tasks at the top of the page
4. Ability to delete tasks as needed

While the core functionality is complete and sufficient for basic task management, there's room for improvement in the HTML structure. Currently, tasks occasionally cluster in the same row, which could be addressed to enhance the visual organization of the list.
This simple yet effective Task List complements the Agenda feature by providing a space for managing non-time-specific activities, contributing to a more comprehensive productivity system.

#### The Time Tracker

Time Tracker feature proved to be the most complex and challenging component of the Life Manager app. This feature, while functional, still has significant potential for optimization. To better explain its intricacies, I've divided the Time Tracker into three distinct categories, each addressing a different aspect of time management and activity tracking:

###### Activity Logging System

I implemented an Activity Logging System as part of the Time Tracker feature. This system uses the win32gui Python library to monitor the user's active window, serving as a proxy for their current activity. While this method is generally accurate, it may occasionally misinterpret user actions.
Key features of the Activity Logging System include:

1. Automatic startup: A pythonw version of the program runs at system boot.
2. Continuous monitoring: The program loops on an event schedule.
3. Activity categorization: Uses a predefined dictionary to classify activities based on program names or URL substrings.
4. Comprehensive data storage: Records user activity, associated app, window name, and browser URL in a dedicated table.

This system provides a foundation for detailed activity tracking, enabling users to gain insights into their daily computer usage patterns.

###### Data Visualization and Analysis

![Gantt-Chart](/screenshots/time-tracker.png)

I prioritized creating an intuitive way to visualize daily activities. The Data Visualization and Analysis component of the Time Tracker feature includes:

Gantt Chart:
1. Implemented using matplotlib 
2. Provides a high-level overview of daily activities 
3. Easily customizable categories to adapt to changing interests and needs

Detailed Activity Log:

1. HTML table displaying individual time-tracking entries
2. Allows for granular review of specific moments
3. Clickable rows for easy reference to visited pages or used applications

This dual approach to data presentation enables users to both get a quick overview of their day and dive deep into specific activities when needed, enhancing the app's utility for time management and productivity analysis.

#### Quick Notes
As the final component of my Life Manager app, I implemented a minimalist Quick Notes feature. While simple in design, it serves a practical purpose:

1. Input field: A basic text box for entering brief notes or thoughts
2. Storage: Notes are saved to a database table
3. Display: All previously entered notes are shown below the input box

This straightforward feature allows users to quickly jot down ideas or information without disrupting their workflow, complementing the more complex features of the app with its simplicity and ease of use.