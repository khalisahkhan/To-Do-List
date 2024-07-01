# To-Do-List
Track your tasks by adding it to the list

# Flask Todo App

## Overview

This is a simple Todo application built with Flask and SQLAlchemy. It allows users to add, view, toggle completion status, and delete tasks (todos).

## Setup and Run Instructions

### Prerequisites

- Python 3.7+
- pip (Python package installer)

### Installation

1. **Clone the repository:**

   ```bash
   git clone <repository_url>
   cd <repository_directory>

# Create a virtual environment
python -m venv venv

# Activate virtual environment
# On Windows
venv\Scripts\activate
# On macOS/Linux
source venv/bin/activate

### Design and Coding Choices

#### Flask and SQLAlchemy:
- Flask
- SQLAlchemy

#### Database Choice:
- SQLite

#### Model Structure:
- **Todo Model**: Includes fields for `id` (primary key), `content` (task description), and `completed` (task status).

### Challenges Faced

   - Integrating Flask's Jinja templating with HTML to display data (todos) and handle user interactions (adding, toggling, deleting todos). 
   
   - Tasks are listed in numerical order - This was a new change that was added. The challenge
   I faced was trying to add a reoccurring toggle to each tasks. I added the following codes below but eventually removed it as my server would not run
   python:
            recurring = db.Column(db.Boolean, default=False) 
   html code:
            <a href="{{ url_for('toggle_recurring', id=todo.id) }}">
                        {% if todo.recurring %}
                        (Make Non-recurring) 
                        {% else %}
                        (Make Recurring) 
                        {% endif %}

Using styles.css I was able to play around with the colors and change the background of the webpage.