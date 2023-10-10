# Course-Scheduling
The Course Scheduling App is a Python application built using the tkinter library and MySQL database to manage course scheduling for a university or educational institution. It allows users to add rooms, courses, and timings, and then generates a timetable based on input data. This project, originally, was implemented in C++ with file inputs and terminal interaction. We aimed to upgrade the system by implementing GUI and database interaction using Python.

## Prerequisites

Before running the application, make sure you have the following prerequisites installed:

- Python 3.10.10
- tkinter (usually included in Python standard library)
- MySQL Connector (`mysql-connector-python`)

You should also have a MySQL database server set up with a database named "course" (you can change the database name in the code if needed).

## Getting Started
1. Clone this repository to your local machine: `git clone https://github.com/HarSen0604/course-scheduling-app.git`
2. Install the required Python packages
   2.1. `pip3.10 install mysql-connector-python`
   2.2. `pip3.10 install re`
3. Enter the details of the MySQL database in the Python code. Defined in the `__init__` of the class `CourseSchedulingApp`.
4. Run the application: `python3.10 CourseSchedulingApp.py`.
5. Follow the on - screen instructions.

## Usage:
1. Add Rooms: Enter room numbers and capacities. The app validates input and ensures constraints are met.
   1.1. Constraints:
     1.1.1. Room numbers are in three digit format.
     1.1.2. The building can have a maximum of 20 rooms.
     1.1.3. Room capacities are within the range [10, 300]
2. Add Courses: Enter course codes in the format 'csddd' (e.g., cs101). The app validates input and checks for duplicates.
3. Add Timings: Enter time slots (e.g., MWF1, TT2:30). The app validates input and checks for duplicates.
   3.1. Constraints:
     3.1.1. Valid lecture times are of the form “MWFd” or “MWFdd” or “TTd” or “TTd:dd” or “TTdd:dd”.
     3.2.2. There are no more than 15 such valid lecture times.
4. Submit: Displays tables with added rooms, courses, and timings.
5. Course Scheduling 2:
   5.1. Contains details about the courses that are being given. It lists the course number, anticipated enrollment, and a selection of preferred lecture times for each individual course. A post-graduate course is one with a course number greater than 600; all other courses are undergraduate.
   5.2. `Enrollment` are integers in the range [3..250].
   5.3. `Preferences` are time preferences of the instructor, separated by commas (a maximum of 5 preferences are allowed for a course).
6. Generate Time Table: Generates a course timetable based on added data and displays it in a new window.
7. Exception Window: The exceptions are displayed in this window.
