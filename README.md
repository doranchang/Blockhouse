# Blockhouse Chart Application

This project is a web-based charting application that uses React on the frontend and Django REST framework on the backend. The application visualizes financial data such as candlestick charts and other types of data using the CanvasJS library for charting.

## Table of Contents

1. [Project Setup](#project-setup)
   - [Backend (Django)](#backend-setup)
   - [Frontend (React)](#frontend-setup)
2. [Libraries and Tools](#libraries-and-tools)
3. [Approach and Thought Process](#approach-and-thought-process)

---

## Project Setup

### Backend Setup (Django REST Framework)

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/doranchang/Blockhouse.git
   cd Blockhouse
2. **Set up a virtual environment**:
   ```python -m venv venv
   source venv/bin/activate  # For Windows: venv\Scripts\activate
3. **Install dependencies**:
   ```pip install -r requirements.txt
4. **Run Django migrations**:
   ```bash
   python manage.py migrate
5. **Run Django server**:
   ```python manage.py runserver
6. **Navigate to the frontend directory**:
   ```cd nextjs-charts
7. **Install dependencies**:
   ```npm install
8. **Run the React development server**:
   ```npm run dev

### Libraries and Tools
Backend (Django):
Django: A web framework for building the backend API.
Django REST Framework: An extension for Django that provides a powerful toolkit for building Web APIs.
Frontend (React):
React: A JavaScript library for building user interfaces.
Next.js: A React framework that supports server-side rendering and static site generation.
CanvasJS: A lightweight charting library for creating interactive charts.

### Approach and Thought Process
Backend:
API Endpoints: The backend exposes several endpoints to provide chart data in JSON format. Each endpoint corresponds to a specific chart type (e.g., line chart, bar chart, pie chart).
Data Management: Initially, the data is hard-coded for demonstration purposes. In a production setup, data would be stored in a database and managed through Django models.
Frontend:
Component-Based Architecture: React's component-based structure helps in managing and rendering UI elements efficiently. Each chart type (e.g., candlestick, line) is implemented as a separate component.
CanvasJS Integration: The CanvasJS library is used for rendering various types of charts. The data fetched from the backend API is passed to CanvasJS components to render the charts.
API Communication: Axios is used to make HTTP requests to the Django API endpoints to fetch the chart data.
Development Process:
Frontend and Backend Development: Development started concurrently on both frontend and backend. This allowed for early integration and testing of data flow between the two components.
Testing: Initial testing focused on verifying that the frontend correctly received and displayed data from the backend. Further improvements include enhancing interactivity and visual appeal.
