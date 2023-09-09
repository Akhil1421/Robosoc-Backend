<center><h1>Robosoc API Documentation</h1></center>

# Auth API

## Login (POST)
- This route is for logging in as admin.
``` baseUrl/services/login ```

Body:
- username: required
- password: required

Command:
```
curl --location 'baseUrl/services/login' 
--header 'Content-Type: application/json' 
--data '{
    "username":"username_of_admin",
    "password":"password_for_admin_control"
}'
```
## Routes for Admin

- ```baseurl```
    - This route is for admin logging in screen.

- ```baseurl/projects```
    - This route is for viewing, editing and deleting projects.
- ```baseurl/projects/addProject```
    - This route is for adding a new project.

- ```baseurl/achievements```
    - This route is for viewing, editing and deleting achievements.
- ```baseurl/achievements/addAchievement```
    - This route is for adding a new achievement.

- ```baseurl/members```
    - This route is for viewing, editing and deleting members.
- ```baseurl/members/addMember```
    - This route is for adding a new member.
 
# Projects API

## Get Projects (GET)
``` baseUrl/services/projects```

Command:
```
curl --location 'baseUrl/services/projects' 
```

<hr>
<br>

## Post Projects (POST)
``` baseUrl/services/projects```

Body:
- image: required (the file to be uploaded in multipart form data)
- name: required
- description: required

Command:
```
curl --location 'baseUrl/services/projects' 
--header 'Content-Type: multipart/form-data' 
--header 'Cookie: ROBOSOC_TOKEN=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MX0.fzKy1H_vgaWe4c7fXtJz82iT7AFaxqO2kCWAPVR92Dg'
--data '{
    "name": "name_of_project",
    "description": "description_of_project",
    "image" : "image_of_project"
}'
```
<hr>
<br>

## Put Projects (PUT)
``` baseUrl/services/projects```

Body:
- id : required
- image: optional (the file to be uploaded in multipart form data)
- name: optional
- description: optional

Command:
```
curl --location 'baseUrl/services/projects' 
--header 'Content-Type: multipart/form-data' 
--header 'Cookie: ROBOSOC_TOKEN=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MX0.fzKy1H_vgaWe4c7fXtJz82iT7AFaxqO2kCWAPVR92Dg'
--data '{
    "name": "name_of_project",
    "description": "description_of_project",
    "image" : "image_of_project"
}'
```
<hr>
<br>

## Delete Projects (DELETE)
``` baseUrl/services/projects```

Body:
- id : required

Command:
```
curl --location 'baseUrl/services/projects' 
--header 'Cookie: ROBOSOC_TOKEN=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MX0.fzKy1H_vgaWe4c7fXtJz82iT7AFaxqO2kCWAPVR92Dg'
--data '{
    "id" : "id_of_project_to_be_deleted"
}'
```

# Achievements API

## Get Achievements (GET)
``` baseUrl/services/achievements```

Command:
```
curl --location 'baseUrl/services/achievements' 
```

<hr>
<br>

## Post Achievements (POST)
``` baseUrl/services/achievements```

Body:
- image: required (the file to be uploaded in multipart form data)
- name: required
- description: required

Command:
```
curl --location 'baseUrl/services/achievements' 
--header 'Content-Type: multipart/form-data' 
--header 'Cookie: ROBOSOC_TOKEN=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MX0.fzKy1H_vgaWe4c7fXtJz82iT7AFaxqO2kCWAPVR92Dg'
--data '{
    "name": "name_of_project",
    "description": "description_of_project",
    "image" : "image_of_project"
}'
```
<hr>
<br>

## Put Achievements (PUT)
``` baseUrl/services/achievements```

Body:
- id : required
- image: optional (the file to be uploaded in multipart form data)
- name: optional
- description: optional

Command:
```
curl --location 'baseUrl/services/achievements' 
--header 'Content-Type: multipart/form-data' 
--header 'Cookie: ROBOSOC_TOKEN=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MX0.fzKy1H_vgaWe4c7fXtJz82iT7AFaxqO2kCWAPVR92Dg'
--data '{
    "name": "name_of_achievement",
    "description": "description_of_achievement",
    "image" : "image_of_achievement"
}'
```
<hr>
<br>

## Delete Achievements (DELETE)
``` baseUrl/services/achievements```

Body:
- id : required

Command:
```
curl --location 'baseUrl/services/achievements' 
--header 'Cookie: ROBOSOC_TOKEN=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MX0.fzKy1H_vgaWe4c7fXtJz82iT7AFaxqO2kCWAPVR92Dg'
--data '{
    "id" : "id_of_achievement_to_be_deleted"
}'
```
# Members API

## Get Members (GET)
``` baseUrl/services/members```

Command:
```
curl --location 'baseUrl/services/members' 
```

<hr>
<br>

## Post Members (POST)
``` baseUrl/services/members```

Body:
- image: required (the file to be uploaded in multipart form data)
- name: required
- position: required (must be one of the following : ['alumni','president','vice president','secretary','programming head','treasurer','pr head', 'external affairs head','electroics head','core coordinator','coordinator','executive'])
- techStack : required

Command:
```
curl --location 'baseUrl/services/members' 
--header 'Content-Type: multipart/form-data' 
--header 'Cookie: ROBOSOC_TOKEN=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MX0.fzKy1H_vgaWe4c7fXtJz82iT7AFaxqO2kCWAPVR92Dg'
--data '{
    "name": "name_of_member",
    "position": "position_of_member",
    "techStack" : "techStack_of_member"
    "image" : "image_of_member"
}'
```
<hr>
<br>

## Put Members (PUT)
``` baseUrl/services/members```

Body:
- id : required
- image: optional (the file to be uploaded in multipart form data)
- name: optional
- position: optional (must be one of the following : ['alumni','president','vice president','secretary','programming head','treasurer','pr head', 'external affairs head','electroics head','core coordinator','coordinator','executive'])
- techStack : optional

Command:
```
curl --location 'baseUrl/services/members' 
--header 'Content-Type: multipart/form-data' 
--header 'Cookie: ROBOSOC_TOKEN=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MX0.fzKy1H_vgaWe4c7fXtJz82iT7AFaxqO2kCWAPVR92Dg'
--data '{
    "id" : "id_of_member",
    "name": "name_of_member",
    "position": "position_of_member",
    "techStack" : "techStack_of_member"
    "image" : "image_of_member"
}'
```
<hr>
<br>

## Delete Members (DELETE)
``` baseUrl/services/members```

Body:
- id : required

Command:
```
curl --location 'baseUrl/services/members' 
--header 'Cookie: ROBOSOC_TOKEN=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MX0.fzKy1H_vgaWe4c7fXtJz82iT7AFaxqO2kCWAPVR92Dg'
--data '{
    "id" : "id_of_member_to_be_deleted"
}'
```
