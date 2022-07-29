# mock-assessment-cgi-2022

## PROBLEM STATEMENT

Develop the Microservices Application Using Spring Boot by using following requirement : 

  - Step1 : Develop the student-service by taking the following details:

                  - com.cgi.main
                         - StudentMainApplication.java
                  
                  - com.cgi.model
                          - Student
                            -id
                            -name
                            -mobilenum
                            -cid
                 
                 - com.cgi.repository
                            - StudentRepository
                 
                 - com.cgi.service
                            - StudentService
                 
                 - com.cgi.controller
                            - StudentController
                                - Inside the StudentController the  following handlers methods:
                                   
                                   -saveStudent()
                                        - save the  student information
                                   -getAllStudent()
                                         - getAll student information along with course details.
  
  - Step2:  Develop the course-service by taking the following details:
                            - com.cgi.main
                                    - CourseMainApplication.java
                  - com.cgi.model
                          - Course
                            -id
                            -name
                            -duration
  
                  - com.cgi.repository
                            - CourseRepository
                  
                  - com.cgi.service
                            - CourseService
                  
                  - com.cgi.controller
                            - CourseController
                                - Inside the CourseController the  following handlers methods:
                                   
                                   -saveCourse()
                                        - save the  course information
                                   -getAllCourse()
                                         - getAll course information.
 ----------------------------------------------------------------------------------------------------------------------------------
 
 Note: Student  should  get the course  information by  invoking the rest call to course-service.
 
 ---------------------------------------------------------------------------------------------------------------------------
 
 
   - The  following URL to test it:
             course-service:
                     
                     -
                     URL:http://localhost:7001/api/save
                     Method:POST
                     Body  : {
                                    "name":"JAVA",
                                    "duration":30
                             }
                             
                     -
                     URL: http://localhost:7001/api/allcourse
                     Method:GET
                     Response:
                     {
                                 "id":1,
                                 "name":"JAVA",
                                 "duration":30
                     
                     }
                     
   - The following URL to test it for student-service:
                   -
                    URL: http://localhost:7002/api/save
                    Method: POST
                    Body  :{
                                  "name":"RAJU",
                                  "mobilenum":"9988771122"
                           }
                   
                   URL: http://localhost:7002/api/1
                   Method:GET
                   Response{
                              "id" : 1,
                              "name":"RAJU",
                              "mobilenum":"9988771122",
                              "cid":
                                 {
                                 "id":1,
                                 "name":"JAVA",
                                 "duration":30
                                 }
                           }
