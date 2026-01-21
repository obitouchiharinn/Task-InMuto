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
- <img width="600" height="400" alt="image" src="https://github.com/user-attachments/assets/07f08aef-b7b2-48fb-bd72-60baa16c9509" />
<img width="600" height="400" alt="image" src="https://github.com/user-attachments/assets/4ba062e3-6351-4fbf-8e08-56c30caf5b37" />

- **Priority Levels**: Assign 1-5 stars to tasks.
- <img width="600" height="500" alt="image" src="https://github.com/user-attachments/assets/48f9c451-53a7-4115-8752-26c9104db52a" />
<img width="500" height="199" alt="image" src="https://github.com/user-attachments/assets/8861dc89-157a-45b6-8815-9938dee6509c" />

- **Dependency Graph**: Visualize task dependencies.
-  **Circular Layout**: Default, connects nodes in a ring.
- <img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/ad84aa19-d63f-4969-bd69-fe351bf2f81f" />

 - **Tree Layout**: Hierarchical view of dependencies.
<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/6015b3c1-a8a5-4dd2-9f9e-7e060316250f" />

  - **Grid Layout**: Organized grid view.
<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/89aea501-12cd-4663-b629-326416dd33e3" />

  -
 

- **Safety Checks**:
-  - Prevents tasks from depending on themselves.
  - Detects and prevents circular dependencies (loops).
- <img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/be2e8ebb-4935-4fcf-9159-c3c12c52a3d0" />

 - **Delete option**:
 - warm user that other taks depend on this.
 - <img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/8821cca0-26c1-44a0-8c47-f62dcad5c396" />


 - **status Option**:
<img width="306" height="316" alt="image" src="https://github.com/user-attachments/assets/9aba458a-70b6-4640-a1c5-a67c2ab7289c" />


 **Dragable option**:

<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/3f72a911-63c1-467a-9288-d53579454ff7" />

 **Search Option**:

 <img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/365f5bac-3aaa-48c1-946d-45936063d9c1" />

