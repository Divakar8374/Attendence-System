# Attendence-System

CREATE TABLE attend (

faculty_id varchar(30) DEFAULT NULL,
batch_id varchar(30) DEFAULT NULL,
student_id varchar(30) DEFAULT NULL,
student_name varchar(30) DEFAULT NULL
)

CREATE TABLE batch (

batch_id varchar(30) NOT NULL,
subject varchar(30) DEFAULT NULL,
days varchar(30) DEFAULT NULL,
faculty_id varchar(30) DEFAULT NULL,
PRIMARY KEY (batch_id)
)

insert into batch (batch_id,subject,days,faculty_id) values ('101','Core java','25','001');
insert into batch (batch_id,subject,days,faculty_id) values ('102','Advance Java','35','002');
insert into batch (batch_id,subject,days,faculty_id) values ('103','PHP','40','003');

CREATE TABLE faculty (

faculty_id varchar(30) NOT NULL,
faculty_name varchar(30) DEFAULT NULL,
user_id varchar(30) DEFAULT NULL,
password varchar(30) DEFAULT NULL,
contact varchar(30) DEFAULT NULL,
salary DECIMAL(10, 2) NOT NULL
)

insert into faculty (faculty_id,faculty_name,user_id,password,contact,salary) values ('001','Ankit','ankit001','ankit','9900998729','25000');
insert into faculty (faculty_id,faculty_name,user_id,password,contact,salary) values ('002','Sonu','sonu002','sonu','9900878987','30000');
insert into faculty (faculty_id,faculty_name,user_id,password,contact,salary) values ('003','Katrina','katrina003','katrina','9425022909','25000');

CREATE TABLE student (

student_id varchar(30) NOT NULL,
student_name varchar(30) DEFAULT NULL,
user_id varchar(30) DEFAULT NULL,
pass varchar(30) DEFAULT NULL,
gender varchar(30) DEFAULT NULL,
contact varchar(30) DEFAULT NULL,
batch_id varchar(30) DEFAULT NULL
)

insert into student (student_id,student_name,user_id,pass,gender,contact,batch_id) values ('001','Kaushal','kaushal001','1234','male','9988776655','101');
insert into student (student_id,student_name,user_id,pass,gender,contact,batch_id) values ('002','Rajeev','rajeev002','rajeev','male','9900998877','101');
insert into student (student_id,student_name,user_id,pass,gender,contact,batch_id) values ('004','Akshay','akshay004','akshay','male','9425099800','102');
insert into student (student_id,student_name,user_id,pass,gender,contact,batch_id) values ('005','Ranbir','ranbir005','ranbir','male','9425077229','101');

CREATE TABLE subject (

subject_id varchar(30) NOT NULL,
subject_name varchar(30) DEFAULT NULL
)

insert into subject (subject_id,subject_name) values ('201','Core java');
insert into subject (subject_id,subject_name) values ('202','Advance Java');
insert into subject (subject_id,subject_name) values ('203','PHP');

select * from batch;
select * from attend;
select * from faculty;
select * from student;
select * from subject;

