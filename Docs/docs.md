# User API
## Create User
***
### Create User Request
```http
POST /api/v1/candidate/register
```
```json
{
  "username": "sathvik29",
  "password": "astrongpassword",
  "firstName": "Tellakulaa",
  "middleName": "",
  "lastName": "Sathvik",
  "preferredName": "Sathvik",
  "email": "sathvik@gmail.com",
  "phoneNumber": "+91 1234567890",
  "location": "Bangalore, Karnataka", 
  "linkedInUrl": "https://linkedin.com/user",
  "skills": [{"application security": 1}, {"penetration testing": 2}],
  "education": [
    {
      "instituteName": "MVJCE",
      "branch": "Computer Science and Engineering",
      "yearOfPassing": 2024,
      "cgpa": 8.0
    },
    {
      "instituteName": "Air Force School, ASTE",
      "branch": "Science",
      "yearOfPassing": 2020,
      "cgpa": 8.0
    }
  ],
  "workExperience": [
    {
      "role": ["CyberSecurity Engineer", "Full stack developer"],
      "employmentType": "internship",
      "companyName": "Subhanu Technologies",
      "startDate": "Jul 2023",
      "endDate": "Aug 2024",
      "skills": ["Application Security", "Penetration Testing"],
      "description": ["What did you do?", "How did you do?", "What was the impact?"]
    },
    {
      "role": ["Lead Web Developer", "Web Developer"],
      "employmentType": "part-time",
      "companyName": "TEDxMVJCE",
      "startDate": "Jul 2020",
      "endDate": "Aug 2024",
      "skills": ["Web Development", "Web designing"],
      "description": ["What did you do?", "How did you do?", "What was the impact?"]
    }
  ],
  "certifications": ["Google cybersecurity Analyst Certificate"],
  "projects": [
    {
      "name": "Name",
      "link": "https://github.com/user/project",
      "liveLink": "http://project.io"
    },
    {
      "name": "Name",
      "link": "https://github.com/user/project",
      "liveLink": "http://project.io"
    }
  ],
  "hobbies": ["football"]
}
```
### Create User Response
```
201 Created
```
## Login
***
### Login Request
```http
POST /api/v1/candidate/login
```
```json
{
  "username": "sathvik29",
  "password": "astrongpassword"
}
```
### Login response
```http
200 OK
```
```json
{
  "accessToken": "token",
  "tokenType": "Brearer",
  "expiresIn": 3600
}
```
## Get Profile
***
### Get Profile Request
```http
GET /api/v1/candidate/{candidateId}
```
### Get Profile Response
```http
200 Ok
```
```json
{
  "userId": "0000-0000-0000-0000",
  "username": "sathvik29",
  "firstName": "Tellakulaa",
  "middleName": "",
  "lastName": "Sathvik",
  "preferredName": "Sathvik",
  "email": "sathvik@gmail.com",
  "phoneNumber": "+91 1234567890",
  "location": "Bangalore, Karnataka", 
  "linkedInUrl": "https://linkedin.com/user",
  "skills": [{"application security": 1}, {"penetration testing": 2}],
  "education": [
    {
      "instituteName": "MVJCE",
      "branch": "Computer Science and Engineering",
      "yearOfPassing": 2024,
      "cgpa": 8.0
    },
    {
      "instituteName": "Air Force School, ASTE",
      "branch": "Science",
      "yearOfPassing": 2020,
      "cgpa": 8.0
    }
  ],
  "workExperience": [
    {
      "role": ["CyberSecurity Engineer", "Full stack developer"],
      "employmentType": "internship",
      "companyName": "Subhanu Technologies",
      "startDate": "Jul 2023",
      "endDate": "Aug 2024",
      "skills": ["Application Security", "Penetration Testing"],
      "description": ["What did you do?", "How did you do?", "What was the impact?"]
    },
    {
      "role": ["Lead Web Developer", "Web Developer"],
      "employmentType": "part-time",
      "companyName": "TEDxMVJCE",
      "startDate": "Jul 2020",
      "endDate": "Aug 2024",
      "skills": ["Web Development", "Web designing"],
      "description": ["What did you do?", "How did you do?", "What was the impact?"]
    }
  ],
  "certifications": ["Google cybersecurity Analyst Certificate"],
  "projects": [
    {
      "name": "Name",
      "link": "https://github.com/user/project",
      "liveLink": "http://project.io"
    },
    {
      "name": "Name",
      "link": "https://github.com/user/project",
      "liveLink": "http://project.io"
    }
  ],
  "hobbies": ["football"]
}
```
## Update Profile
***
### Edit Profile Request
```http
PATCH /api/v1/user/profile
```
```json
{
  "middleName": ""
}
```
### Edit Profile Response
```
200 ok
```
## Delete Profile
***
### Delete Profile Request
```http
DELETE /api/v1/profile
```
### Delete Profile Response
```http
204 No Content
```

# HR API
## Create HR account
***
### Create HR account request
```http
POST /api/v1/hr
```
```json

```
### Create HR account response
```http
200 Ok
```
```json
{
  "email": "sathvik@company.com",
  "password": "anotherstrongpassword",
  "firstName": "Tellakulaa",
  "lastName": "Sathvik",
  "middleName": "",
  "phoneNumber": "+91 1234567890"
}
```
## Login
***
### Login HR account request
```http
POST /api/v1/hr/login
```
```json
{
  "username": "sathvik@company.com",
  "password": "anotherstrongpassword"
}
```
### Login HR account response
```http
200 OK
```
```json
{
  "accessToken": "token",
  "tokenType": "Brearer",
  "expiresIn": 3600
}
```
## Read HR Account
***
### Read HR account request
```http
GET /api/v1/hr/{hrId}
```
### Read HR account response
```http
200 OK
```
```json
{
  "id": "0000-0000-0000-0000",
  "email": "sathvik@company.com",
  "firstName": "Tellakula",
  "lastName": "Sathvik",
  "middleName": "",
  "phoneNumber": "+91 1234567890"
}
```
## Update HR account
***
### Update HR account request
```http
PATCH /api/v1/profile/{hrId}
```
```json
{
  "firstName": "Tellakulaa"
}
```
### Update HR account response
```http
204 No Content
```
## Delete HR account
***
### Delete HR account request
```http
DELETE /api/v1/profile/{hrID}
```
### Delete HR response
```http
204 No Content
```
# JOB 
## Create Job - HR
***
### Create Job Request
```http
POST /api/v1/jobs
```
```json
{
  "jobTitle": "Full stack developer",
  "skills": [{"Java": 4}, {"MySQL": 3}, {"Angular": 3}]
}
```
### Create Job Response 
```http
201 Ok
```
```text
Location: /api/v1/jobs/{jobId}
```
```json
{
  "jobId": "0000-0000-0000-0000",
  "jobTitle": "Full stuck developer",
  "skills": [{"Java": 4}, {"MySQL": 3}, {"Angular": 3}]
}
```
## Update Job - HR
***
### Update Job Request
```http
PATCH /api/v1/jobs/{jobId}
```
```json
{
  "jobTitle": "Full stack developer"
}
```
### Update Job Response
```http
204 No Content
```
## Find Candidates - HR
***
### Find Candidates Request
```http
GET url
```
### Find Candidates Response
```http
200 Ok
```
```json
{
  "candidates": ["candidateID1", "candidateID2"]
}
```
## Delete Job - HR
***
### Delete Job Request
```http
DELETE /api/v1/job/{jobId}
```
### Delete Job Response
```http
204 No Content
```
## Get Job - Candidate and HR
***
### Get job request
```http
GET /api/v1/jobs/{jobId}
```
### Get job response
```http
200 Ok
```
```json
{
  "jobId": "0000-0000-0000-0000",
  "jobTitle": "Full stuck developer",
  "skills": [{"Java": 4}, {"MySQL": 3}, {"Angular": 3}]
}
```

## Get jobs of a company - Candidate and HR
***
### Get jobs of a company request
```http
GET /api/v1/jobs?company=companyName
```
### Get jobs of a company response
```http
200 Ok
```
```json
{
  "companyName": "Company Name",
  "jobs": [
    {
      "role": "Full stack developer",
      "postedAt": "DateTimeObject",
      "postedBy": "HR Name"
    }
  ]
}
```
## Apply - Candidate
***
### Apply Request
```http
POST url
```
### Apply Response
```http
200 OK
```
```json
{
  "msg": "msg"
}
```

