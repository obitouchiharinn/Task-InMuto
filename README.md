# InMuto Task Management System

A robust task management application with dependency tracking, visual layouts, and priority management.

## Prerequisites
- **Python**: 3.10 or higher
- **Node.js**: 18 or higher
- **npm**: Included with Node.js

## Project Structure
- `manage.py`: Django entry point.
- `backend/`: Contains Django project settings (`backend`), `tasks` app, and `frontend` source.
- `backend/frontend/`: React + Vite frontend application.
- `db.sqlite3`: Default SQLite database (for development).

## Backend Setup (Django)

1. **Navigate to the root directory** (where `manage.py` is located):
   ```bash
   cd c:\Users\HP ELITEBOOK 840 G6\Desktop\Inmuto
   ```
   *(Adjust path as necessary if you moved the folder)*

2. **Create a virtual environment**:
   ```bash
   python -m venv venv
   ```

3. **Activate the virtual environment**:
   - **Windows**:
     ```bash
     venv\Scripts\activate
     ```
   - **Mac/Linux**:
     ```bash
     source venv/bin/activate
     ```

4. **Install Python dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

5. **Run Database Migrations**:
   ```bash
   python manage.py migrate
   ```

6. **Start the Django Development Server**:
   ```bash
   python manage.py runserver
   ```
   - The backend API will be running at `http://localhost:8000`.

## Frontend Setup (React + Vite)

1. **Open a new terminal** and navigate to the frontend directory:
   ```bash
   cd backend/frontend
   ```

2. **Install Node dependencies**:
   ```bash
   npm install
   ```

3. **Run the Frontend Development Server**:
   ```bash
   npm run dev
   ```
   - The application will be accessible at `http://localhost:5173` (or the port shown in your terminal).

## Key Features

- **Task Management**: Create, update, delete, and view tasks.
- <img width="1120" height="900" alt="image" src="https://github.com/user-attachments/assets/07f08aef-b7b2-48fb-bd72-60baa16c9509" />

- **Priority Levels**: Assign 1-5 stars to tasks.
- **Dependency Graph**: Visualize task dependencies.
  - **Circular Layout**: Default, connects nodes in a ring.
  - **Tree Layout**: Hierarchical view of dependencies.
  - **Grid Layout**: Organized grid view.
- **Safety Checks**:
  - Prevents tasks from depending on themselves.
  - Detects and prevents circular dependencies (loops).
  - Handles concurrent updates gracefully.
