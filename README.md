# OnlineVotingPortal

INTRODUCTION

		Modules :	-      Admin
-	  Organization
-	  Candidate
-	  Voter

		Technology      -    .Net
		Tools                 -    SQL Server Management Studio
					-    Microsoft Visual Studio	
OVERVIEW 

		Online voting Portal is a website to make the voting process 
1.	Easy as just on a single click sitting on your home you can cast a vote.
2.	Cheaper as workers for conducting elections and public facilities are not needed and there is no need to go to voting center.
3.	Faster as result declaration do not take much time.
4.	Eco-Friendly by not using papers for ballot.
5.	Authentic as no one can influence your vote. 




			        MODULE  DESCRIPTION
 
1. ADMIN
Admin will Verify the Organization who will registered to the System. It will                                                           add the Organization to system if the details provided by the Organization would be correct or would reject the request.


2. ORGANIZATION
Here first Organization would register to the system by providing the details. After verification done by admin Organization can login to the system. After Login Organization can  add categories and on basis of that categories it will add users For Example:-Student, Teachers etc. Then it will Schedule the Election. After scheduling Organization would add voters and candidates from their existing users. It can also edit the election details. After election is completed organization can view the results by generating the reports. Organization can also see how many voters have voted.  	


3. CANDIDATES
Candidates are been added by the Organization. After login Candidates would be able to enter the personal details. They can see the elections which are they part of. Candidates can also add Manifesto for the elections so that Voters can know the candidate. After Election they can see the results. 





4. Voters
As Similar to candidates voters would be added by the Organization. After Login they can add or update their personal details. They can see the elections which are they part of. They can view the candidate and there manifesto. After Election starts they will able to vote for their candidate and can only give one vote. After Election they can see the results that is number of votes each candidate got.



				DATA DICTIONARY
1.Address
Name	Data Type
Address_id	Numeric(18,0)  [Primary Key]
Country	Varchar(50)
State	Varchar(50)
City	Varchar(50)
Description	Ntext

2.Admin
Name	Data Type
User_id	Numeric(18,0)  [Primary Key]
Name	Nvarchar(50)
ContactNo	Nvarchar(18)
Address_id	Numeric(18,0)  [Foreign Key]
Photo	Nvarchar(50)

 3.Category
Name	Data Type
CategoryId	Numeric(18,0)  [Primary Key]
OrganizationId	Numeric(18,0)  [Foreign Key]
CategoryName	Varchar(20)




4.City
Name	Data Type
CityId	Int  [Primary Key]
CityName	Varchar(50)
StateId	Int  [Foreign Key]

5.Country
Name	Data Type
CountryId	Int   [Primary Key]
CountryName	Varchar(50)

6.Election
Name	Data Type
EventId	Numeric(18,0)  [Primary Key]
OrganizationId	Numeric(18,0)  [Foreign Key]
Title	Nvarchar(50)
StartDateTime	Datetime2(7)
EndDateTime	Datetime2(7)
Description	Nvarchar(MAX)

7.Login
Name	Data Type
User_id	Numeric(18,0)  [Primary Key]
Email	Nvarchar(50)
Password	Nvarchar(20)



8.Organization
Name	Data Type
User_id	Numeric(18,0)  [Primary Key]
Name	Nvarchar(50)
ContactNo	Nvarchar(18)
Address_id	Numeric(18,0)  [Foreign Key]
Photo	Nvarchar(50)
Verify	Bit

9.Reset
Name	Data Type
Email	Nvarchar(50)  [Primary Key]
Id	Uniqueidentifier
Request	Datetime

10.Result
Name	Date Type
EventId	Numeric(18,0) [Primary Key]
CandidateId	Numeric(18,0) [Foreign Key]
OrganizationId	Numeric(18,0) [Foreign Key]
Result	Numeric(18,0)

11.Roles
Name	Data Type
Role_id	Numeric(18,0)  [Primary Key]
Role_name	Varchar(20)



12.State
Name	Data Type
StateId	int  [Primary Key]
StateName	Varchar(50)
CountryId	Int


13.User
Name	Data Type
User_id	Numeric(18,0)  [Primary Key]
Organization_id	Numeric(18,0)  [Foreign Key]
Name	Nvarchar(50)
ContactNo	Nvarchar(18)
Address_id	Numeric(18,0)
Photo	Nvarchar(50)
Category_id	Numeric(18,0)
Manifesto	Nvarchar(MAX)


14.User Roles
Name	Data Type
Role_id	Numeric(18,0) [Primary Key]
User_id	Numeric(18,0) [Foreign Key]




15.Vote
Name	Data Type
EventId	Numeric(18,0)  [Primary Key]
VoterId	Numeric(18,0)  [Foreign Key]
OrganizationId	Numeric(18,0)
Vote	Bit


















