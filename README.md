<center><h1>Robosoc API Documentation</h1></center>

# Auth API

## Login (POST)
- This route is for logging in as admin.
``` base_url/services/login ```

Body:
- username: required
- password: required

Command:
```
curl --location 'base_url/services/login' \
--header 'Content-Type: application/json' \
--data '{
    "username":"username_of_admin",
    "password":"password_for_admin_control"
}'
```

# Projects API
