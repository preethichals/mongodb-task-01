# mongodb-task-01

Design database for Zen class programme
users
codekata
attendance
topics
tasks
company_drives
mentors

Find all the topics and tasks which are thought in the month of October

db.topics.find({month: "October"}).pretty()
db.tasks.find({month:"October"}).pretty()

Find all the company drives which appeared between 15 oct-2020 and 31-oct-2020

db.company_drives({appeared:{$gte:ISODate("15 oct-2020"),$lt:ISODate("31-oct-2020"}}).pretty()

Find all the company drives and students who are appeared for the placement.

db.company_drives({placement : {company:1, students:1}}).pretty()

Find all the mentors with who has the mentee's count more than 15

db.mentors.find(mentees :{$gt : 15}).pretty()
 
 Find the number of problems solved by the user in codekata
 
 db.users.find({name: 1}{codekata: {solved : 1}}).pretty()
 
 Find the number of users who are absent and task is not submitted  between 15 oct-2020 and 31-oct-2020
 
 db.movies.aggregate( [ { $match: { attendence: absent } } ] )
