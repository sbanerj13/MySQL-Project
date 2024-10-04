**Below are the codes used in this project**
CREATE DATABASE EmployeeAttendanceDB;
USE EmployeeAttendanceDB;
CREATE TABLE Employees (
    employee_id INT AUTO_INCREMENT PRIMARY KEY,
    employee_name VARCHAR(100) NOT NULL,
    designation VARCHAR(50) NOT NULL,
    Salary bigint NOT NUll 
);
CREATE TABLE Attendance (
    attendance_id INT AUTO_INCREMENT PRIMARY KEY,
    employee_id INT not null,
    login_time DATETIME NOT NULL,
    logout_time DATETIME NOT NULL,
    break_time TIME NOT NULL,
    valid_duty_hours TIME NOT NULL,
    FOREIGN KEY (employee_id) REFERENCES Employees(employee_id)
);
INSERT INTO Employees VALUES
(1,'Alice Johnson', 'Software Engineer', 50000),
(2, 'Bob Smith', 'Project Manager', 45000),
(3, 'Charlie Brown', 'Data Analyst', 46000),
(4, 'David Wilson', 'HR Manager', 38000),
(5, 'Eva Green', 'Marketing Specialist', 60000),
(6, 'Frank Black', 'Sales Representative', 70000),
(7, 'Grace White', 'Web Developer', 65000),
(8, 'Henry Gray', 'Database Administrator', 55000),
(9, 'Ivy Blue', 'Graphic Designer',80000),
(10, 'Jack Red', 'DevOps Engineer', 85000 ),
(11, 'Zoe Pink', 'Content Writer', 35000),
(12, 'Alice Smith', 'Software Engineer', 60000),
(13, 'Bob Johnson', 'Project Manager', 62000),
(14, 'Charlie Brown', 'Product Designer', 50000),
(15, 'Diana Prince', 'Data Analyst', 45000),
(16,'Ethan Hunt', 'Quality Assurance', 38000),
(17, 'Fiona Gallagher', 'HR Manager', 35000),
(18, 'George Costanza', 'Sales Representative', 40000),
(19, 'Hannah Baker', 'Marketing Specialist', 36000),
(20, 'Ian Malcolm', 'Business Analyst', 45000),
(21, 'Jenna Marbles', 'Web Developer', 60000),
(22, 'Kyle Reese', 'System Administrator', 40000),
(23, 'Laura Croft', 'Graphic Designer', 55000),
(24, 'Mike Wazowski', 'Customer Support', 25000),
(25, 'Nina Simone', 'Finance Manager', 40000),
(26, 'Oscar Wilde', 'Operations Manager', 40000),
(27, 'Paula Patton', 'Executive Assistant', 28000),
(28, 'Quincy Adams', 'Research Scientist', 26000),
(29, 'Rachel Green', 'Fashion Consultant', 29000),
(30, 'Steve Rogers', 'Technical Lead', 50000),
(31, 'Tina Fey', 'Content Writer', 25000),
(32, 'Aarav Sharma', 'Software Engineer', 52000),
(33, 'Vivaan Gupta', 'Project Manager', 60000),
(34, 'Aditya Singh', 'Data Analyst', 35000),
(35, 'Vihaan Mehta', 'Business Analyst', 40000),
(36, 'Arjun Verma', 'UX Designer', 34000),
(37, 'Sai Patel', 'DevOps Engineer', 50000),
(38, 'Reyansh Rao', 'Quality Assurance', 30000),
(39, 'Ayaan Kumar', 'System Administrator', 38000),
(40, 'Krishna Nair', 'Network Engineer', 48000),
(41, 'Dhruv Iyer', 'Database Administrator', 45000),
(42, 'Kabir Joshi', 'Web Developer', 55000),
(43, 'Rudra Bhatia', 'Marketing Specialist', 38000),
(44, 'Anik Jain', 'Sales Executive', 30000),
(45, 'Tanmay Kapoor', 'Product Owner', 35000),
(46, 'Rishabh Choudhary', 'Technical Lead', 50000),
(47, 'Kiaan Saxena', 'Support Specialist', 30000),
(48, 'Lakshay Agarwal', 'HR Executive', 32000),
(49, 'Nirvaan Bansal', 'Content Writer', 25000),
(50, 'Samarth Desai', 'Graphic Designer', 48000);
select * from employees;
INSERT INTO Attendance (employee_id, login_time, logout_time, break_time, valid_duty_hours) VALUES
(1, '2024-10-01 09:00:00', '2024-10-01 17:00:00', '00:30:00', '07:30:00'),
(2, '2024-10-01 09:15:00', '2024-10-01 17:15:00', '00:30:00', '07:45:00'),
(3, '2024-10-01 09:05:00', '2024-10-01 17:05:00', '00:15:00', '07:45:00'),
(4, '2024-10-01 09:30:00', '2024-10-01 17:30:00', '00:45:00', '07:15:00'),
(5, '2024-10-01 09:10:00', '2024-10-01 17:10:00', '00:30:00', '07:30:00'),
(6, '2024-10-01 09:00:00', '2024-10-01 17:00:00', '00:30:00', '07:20:00'),
(7, '2024-10-01 09:15:00', '2024-10-01 17:15:00', '00:30:00', '07:29:00'),
(8, '2024-10-01 09:05:00', '2024-10-01 17:05:00', '00:10:00', '07:45:00'),
(9, '2024-10-01 09:30:00', '2024-10-01 17:30:00', '00:35:00', '07:25:00'),
(10, '2024-10-01 09:10:00', '2024-10-01 17:10:00', '00:40:00', '07:40:00'),
(11, '2024-10-01 09:00:00', '2024-10-01 17:00:00', '00:30:00', '07:30:00'),
(12, '2024-10-01 09:25:00', '2024-10-01 17:15:00', '00:30:00', '07:45:00'),
(13, '2024-10-01 09:15:00', '2024-10-01 17:05:00', '00:15:00', '07:45:00'),
(14, '2024-10-01 09:20:00', '2024-10-01 17:30:00', '00:45:00', '07:15:00'),
(15, '2024-10-01 09:10:00', '2024-10-01 17:10:00', '00:30:00', '07:30:00'),
(16, '2024-10-01 09:00:00', '2024-10-01 17:00:00', '00:30:00', '07:30:00'),
(17, '2024-10-01 09:15:00', '2024-10-01 17:15:00', '00:30:00', '07:45:00'),
(18, '2024-10-01 09:05:00', '2024-10-01 17:05:00', '00:15:00', '07:45:00'),
(19, '2024-10-01 09:30:00', '2024-10-01 17:30:00', '00:45:00', '07:15:00'),
(20, '2024-10-01 09:10:00', '2024-10-01 17:10:00', '00:30:00', '07:30:00'),
(21, '2024-10-01 09:00:00', '2024-10-01 17:00:00', '00:30:00', '07:30:00'),
(22, '2024-10-01 09:15:00', '2024-10-01 17:15:00', '00:30:00', '07:45:00'),
(23, '2024-10-01 09:05:00', '2024-10-01 17:15:00', '00:15:00', '07:45:00'),
(24, '2024-10-01 09:30:00', '2024-10-01 17:40:00', '00:45:00', '07:15:00'),
(25, '2024-10-01 09:10:00', '2024-10-01 17:30:00', '00:30:00', '07:30:00'),
(26, '2024-10-01 09:10:00', '2024-10-01 17:00:00', '00:30:00', '07:30:00'),
(27, '2024-10-01 09:35:00', '2024-10-01 17:15:00', '00:30:00', '07:45:00'),
(28, '2024-10-01 09:05:00', '2024-10-01 17:05:00', '00:15:00', '07:45:00'),
(29, '2024-10-01 09:40:00', '2024-10-01 17:30:00', '00:45:00', '07:15:00'),
(30, '2024-10-01 09:10:00', '2024-10-01 17:10:00', '00:30:00', '07:30:00'),
(31, '2024-10-01 09:00:00', '2024-10-01 17:00:00', '00:30:00', '07:30:00'),
(32, '2024-10-01 09:15:00', '2024-10-01 17:15:00', '00:30:00', '07:45:00'),
(33, '2024-10-01 09:05:00', '2024-10-01 17:05:00', '00:15:00', '07:45:00'),
(34, '2024-10-01 09:30:00', '2024-10-01 17:30:00', '00:45:00', '07:15:00'),
(35, '2024-10-01 09:10:00', '2024-10-01 17:10:00', '00:30:00', '07:30:00'),
(36, '2024-10-01 09:00:00', '2024-10-01 17:00:00', '00:30:00', '07:30:00'),
(37, '2024-10-01 09:15:00', '2024-10-01 17:15:00', '01:30:00', '07:45:00'),
(38, '2024-10-01 09:05:00', '2024-10-01 17:05:00', '00:15:00', '07:45:00'),
(39, '2024-10-01 09:30:00', '2024-10-01 17:30:00', '00:05:00', '07:15:00'),
(40, '2024-10-01 09:10:00', '2024-10-01 17:10:00', '00:30:00', '07:30:00'),
(41, '2024-10-01 09:00:00', '2024-10-01 17:00:00', '00:30:00', '07:30:00'),
(42, '2024-10-01 09:15:00', '2024-10-01 17:15:00', '00:30:00', '07:45:00'),
(43, '2024-10-01 09:05:00', '2024-10-01 17:05:00', '00:15:00', '08:45:00'),
(44, '2024-10-01 09:30:00', '2024-10-01 16:30:00', '00:45:00', '07:15:00'),
(45, '2024-10-01 09:10:00', '2024-10-01 17:10:00', '00:30:00', '06:30:00'),
(46, '2024-10-01 09:00:00', '2024-10-01 17:00:00', '00:30:00', '07:30:00'),
(47, '2024-10-01 09:15:00', '2024-10-01 17:15:00', '00:30:00', '07:45:00'),
(48, '2024-10-01 09:05:00', '2024-10-01 17:05:00', '00:15:00', '07:45:00'),
(49, '2024-10-01 09:30:00', '2024-10-01 17:30:00', '00:45:00', '07:15:00'),
(50, '2024-10-01 09:10:00', '2024-10-01 17:10:00', '00:30:00', '07:30:00');
select * from attendance;
select * from attendance where employee_id=1;
SELECT e.employee_name, SUM(time_to_sec(a.valid_duty_hours)) AS total_valid_hours_in_sec
FROM Employees e
JOIN Attendance a ON e.employee_id = a.employee_id
GROUP BY e.employee_id;
SELECT e.employee_id, e.employee_name, a.login_time, a.logout_time, a.break_time, a.valid_duty_hours
FROM Employees e
JOIN Attendance a ON e.employee_id = a.employee_id
WHERE DATE(a.login_time) = '2024-10-01';
CREATE VIEW EmployeeAttendanceSummary AS
SELECT 
    e.employee_id,
    e.employee_name,
    e.designation,
    a.login_time,
    a.logout_time,
    a.break_time,
    a.valid_duty_hours,
    TIME_TO_SEC(a.valid_duty_hours) / 3600 AS valid_duty_hours_in_hours  -- Converts to hours
FROM 
    Employees e
JOIN 
    Attendance a ON e.employee_id = a.employee_id;
    SELECT * FROM EmployeeAttendanceSummary;
    SELECT * FROM EmployeeAttendanceSummary WHERE employee_id = 1;
    SELECT * 
FROM EmployeeAttendanceSummary 
WHERE DATE(login_time) = '2024-10-01';
USE EmployeeAttendanceDB;
select * from employees;
select * from employees where salary= 40000;
