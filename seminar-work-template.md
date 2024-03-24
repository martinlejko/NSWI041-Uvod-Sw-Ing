# Student information system - [Personal Information]

The Personal Information Module is specifically designed to efficiently handle the management of individual personal details within the university system. Its primary functions encompass streamlining processes like the collection and organization of personal information during the admission phase, as well as the ongoing tracking of enrollment in various study programs.
Users of this module have the ability to search for other individuals and access their personal information. Notably, each user has the flexibility to define which aspects of their information are visible to others, allowing for a customizable and controlled sharing of personal details.
This versatile module facilitates the creation of personalized admission procedures tailored to specific study programs and academic years. It plays a crucial role in recording admission outcomes for individual participants and tracking whether admitted students have successfully enrolled in their respective studies before the commencement of the first academic year.
In addition to its core functions, the Personal Information Module offers a valuable feature that allows users to generate confirmation documents for their studies. This capability streamlines the process of obtaining official confirmation of enrollment, providing users with a convenient and efficient way to validate their academic status.
As the academic journey progresses, the module continues to manage the recording of personal information, providing the flexibility to update details in response to events such as changes in residence or shifts in academic faculties.
Users maintain access to both their personal details and those of others through the module, with the level of visibility determined by individual preferences. This nuanced control ensures that personal information can be selectively shared, enhancing privacy and data security. The Personal Information Module thus serves as a comprehensive and user-friendly tool for managing and accessing personal information within the university system.


## Functional Requirements

This section specifies the functional requirements.

### User requirements

Students
As a student, I should be able to see my current state of study because I want to be informed.
As a student, I should be able to edit my personal information because some event in my life can happen.
As a student, I should be able to change which information about myself I make visible to the public because I do not feel comfortable sharing everything.
As a student, I should be able to see the public information of other students because I may want to contact the person.
As a student, I should be able to generate confirmation documents of my studies because some organization may want it provided.
Study department/admin
As the study department, we should be able to add new users, and also remove them, because we decide who is our employee/student.
As the study department, we should be able to alter anyone's information because we are the admin and if students can we also can.
As the study department, we should be able to see anyone’s information because we are all knowing.
Employees
As an employee, I should be able to view my personal information because what is the point otherwise.
As an employee, I should be able to view my position because I want to keep myself posted.
As an employee, I should be able to edit my information
As an employee, I should be able to generate confirmation documents of my employment.
All users
As any user, I should be able to display information about myself, because
As any user, I should be able to display information about others that is made public because I may need to 

### System requirements


#### Actors

Students
Employees
Study department/admin
All users

##### [*Actor name*]

Students
A student is a person studying at a university. They can send admission requests. They are able to view and edit their personal information.

Employees
An employee is a person employed by the university. They can apply for a job. They can view and edit their personal information.

Study department
The study department manages admission procedures and records whether admitted students are enrolled or not.

All users
This represents any of the previous actors (All users of sis).

#### Use cases

[*Document here all use cases. Create a subsection for each use case diagram. If you have only one use case diagram, you do not need a special subsection*]

Students
```
@startuml
left to right direction


actor Student as s


package "Administration" {
 actor "Study Department" as sd
}


package "User information module" {
 usecase "Apply to university" as Apply
 usecase "Fill an admission form" as fillAdmissionForm
 usecase "Send admission request" as sendAdmissionRequest
 usecase "View personal data" as ViewPersonalData
 usecase "Edit personal data" as EditPersonalData
}


s -- fillAdmissionForm
sendAdmissionRequest ..> fillAdmissionForm : <<extends>>
Apply -- sd
sendAdmissionRequest -- sd
s -- Apply
s -- ViewPersonalData
s -- EditPersonalData


@enduml
```


Use case - Admission process of student

Precondition:

The student applied for study and was admitted

Normal flow:
The student has applied for study
The university checks if the student meets all criteria for admission
The student is admitted
The student confirms the registration
The study department is informed about the registration

What can go wrong:
The student does not meet the required criteria
The student is informed about his results
The student can not confirm the registration
The student has not confirmed the registration


Postcondition:
The student is registered for a subsequent unit of study.

—--
Use case - Admission process of employee

Precondition:

An employee appointed for a job

Normal flow:
The employee has been appointed for the job
The university checks if the employee meets the requirements 
The employee is admitted
The employee confirms the registration
The study department is informed about the registration

What can go wrong:
The employee does not meet the required criteria
The employee is informed about his results
The employee can not confirm the registration
The employee has not accepted the job offer

Postcondition:
The employee is registered in the study system.

—--
Use case - Change of personal information

Precondition:

The student applied for study and was admitted

Normal flow:
The student studies normally
The student changed his information.
The information is confirmed and valid.

What can go wrong:
The student does not meet the criteria needed.
The student does not have the authority to change certain information.
The student imputed the wrong type of information.


Postcondition:
The student is registered for a subsequent unit of study.

—-
Use case - Confirmation documents of student studies

Precondition:

A student has requested confirmation documents of their studies

Normal flow:
The student has requested confirmation documents
The student department checks if the student is able to get confirmation documents
The confirmation documents are available for student

What can go wrong:
The student is not able to get confirmation documents about their studies
The student is informed about this situation
The student can not obtain these documents


Postcondition:
The student obtains confirmation documents about their studies

Use case - Expulsion of the student

Study department:
```
@startuml
left to right direction


package "Administration" {
 actor "Study Department" as sd
}


package "User information module" {
   usecase "Create admission procedure" as CreateProcedure
   usecase "Record the results of the admission procedures" as RecordResults
   usecase "Record students enrollment" as RecordEnrollment
   usecase "Edit students personal information" as EditInfo
   usecase "Notify about a student not meeting criteria" as Notify
   usecase "End of study" as EndOfStudy
}


sd -- CreateProcedure
sd -- RecordResults
sd -- RecordEnrollment
sd -- Notify
sd -- EditInfo


Notify ..> EndOfStudy: <<include>>


@enduml
```


Precondition:

The student does not meet required criteria

Normal flow:
The student does not meet required criteria
The student department informs student about this situation
The student is expelled

What can go wrong:
Mismatch in his test results
The student is informed about this situation
The student can continue their studies


Postcondition:
The student leaves the university

Use case - Graduation of the student

Precondition:

The student  meets all required criteria

Normal flow:
The student pass all the tests and meets all criteria
The student department informs student about this success
The student graduates

What can go wrong:
Mismatch in his test results
The student is informed about this situation
The student can not graduate now


Postcondition:
The student leaves the university



Employee:
```
@startuml
left to right direction

actor Employee as e

package "Administration" {
  actor "Study Department" as sd
}

package "User information module" {
  usecase "Apply for a job at university" as Apply
  usecase "Accept job offer" as AcceptOffer
  usecase "View personal data" as ViewPersonalData
  usecase "Edit personal data" as EditPersonalData
}

Apply -- sd
AcceptOffer -- sd
e -- Apply
e -- AcceptOffer
e -- ViewPersonalData
e -- EditPersonalData

@enduml
```

Use case - The firing of an employee

Precondition:
The employee has been fired from his position.

Normal flow:
The university wants to fire an employee
Employee is fired

What can go wrong:

Postcondition:
Employee leaves the university

## Information model

```
@startuml
package “Student Information System” {
package “Student Information Module” {
	actor Student
	actor Employee
	actor “Study department/Admin” as StudyDepartment
	usecase “View Personal Information” as UC1
	usecase “Edit Personal Information” as UC2
	usecase “Change Visibility of Information” as UC3
	usecase “Generate Confirmation Documents” as UC4
	usecase “View Public Information of Others” as UC5
	usecase “Add or Remove Users” as UC6
	usecase “Alter Any User Information” as UC7
	usecase “View Any User Information” as UC8
	usecase “View Position Information” as UC9
	}
}

Student --> UC1
Student --> UC2
Student --> UC3
Student --> UC4
Student --> UC5

Employee --> UC1
Employee --> UC9
Employee --> UC2
Employee --> UC4

StudyDepartment --> UC6
StudyDepartment --> UC7
StudyDepartment --> UC8

UC3 .> UC5 : <<extend>>
UC6 .> UC7 : <<include>>
UC7 .> UC8 : <<extend>>

@enduml
```



