
create database university_db;
use university_db;
create table student(
student_id int primary key auto_increment,
firstname varchar(250) not null ,
lasstname varchar(250) not null ,
email varchar(255) not null,
dob date ,
status varchar (255) default ('active')
)
desc student

create database department;
use department;
create table departments(
dept_id int primary key auto_increment ,
dept_name varchar (50) unique 
);

create table employee (
emp_id int primary key auto_increment ,
emp_name varchar (255) not null,
hire_date DATE DEFAULT (Current_Date ),
dept_id int ,
foreign key (dept_id) references departments(dept_id) 
);
desc employee 
