# Employee Payroll Management System

A comprehensive employee payroll management system built with React and Express.js. This application allows you to manage employees, process payrolls, track attendance, and handle leave requests.

## Features

- **Employee Management**: Add, view, and manage employee information
- **Payroll Processing**: Generate and view payroll records for employees
- **Attendance Tracking**: Mark and monitor employee attendance
- **Leave Management**: Request and approve employee leaves

## Tech Stack

- **Frontend**: React, CSS
- **Backend**: Express.js, SQLite
- **Database**: SQLite

## Getting Started

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn

### Installation

1. Clone the repository
2. Install dependencies:
   ```
   npm install
   cd server && npm install
   ```

### Database Setup

Initialize the database with sample data:

```
npm run seed
```

### Running the Application

1. Start both the frontend and backend concurrently:

   ```
   npm run dev:all
   ```

   Or run them separately:

   ```
   # Terminal 1 - Backend
   npm run server

   # Terminal 2 - Frontend
   npm run dev
   ```

2. Open your browser and navigate to `http://localhost:5173`

## API Endpoints

### Employees

- `GET /api/employees` - Get all employees
- `GET /api/employees/:id` - Get employee by ID
- `POST /api/employees` - Add new employee
- `PUT /api/employees/:id` - Update employee

### Payrolls

- `GET /api/payrolls` - Get all payrolls
- `GET /api/payrolls/:month/:year` - Get payrolls by month and year
- `GET /api/payrolls/employee/:employeeId` - Get employee's payroll history
- `POST /api/payrolls` - Generate new payroll for an employee
- `PATCH /api/payrolls/:id` - Update payroll status

### Attendance

- `GET /api/attendance` - Get attendance records by date range
- `GET /api/attendance/employee/:employeeId` - Get employee's attendance
- `POST /api/attendance` - Mark attendance

### Leaves

- `GET /api/leaves` - Get all leave requests
- `GET /api/leaves/employee/:employeeId` - Get employee's leave history
- `POST /api/leaves` - Request leave
- `PATCH /api/leaves/:id` - Update leave status
