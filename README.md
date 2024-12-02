# VRN-security

This is a web application developed using the MERN stack to demonstrate **Role-Based Access Control (RBAC)**. It is designed for a security service company with three user roles: **Guard**, **Manager**, and **Authority**. Each role has different access permissions to the available services.
## API Documentation

Endpoint: ``` POST /signup  ```
Input:
     ```req.body ```

```
{
  "employee_id": "string",
  "password": "string",
  "name": "string",
  "phone": "string",
  "role": "string"
}
```
Output:
On success:
```
{
  "role": "guard",
  "employee_id": "string",
  "token": "string"
}

```

Endpoint:  ``` POST /signin  ```
```
{
  "employee_id": "string",
  "password": "string"
}

```
Output:
On success:

```
{
  "role": "string",
  "employee_id": "string",
  "token": "string"
}


```

Endpoint: ``` GET /service/cctv  ```
output:
```
{
  "message": "✅OK as a gurad you are authorized to access CCTV."
}

```
Endpoint: ``` GET /service/gdeployed  ```
output:
```
  {
  "message": " as a gurad you can not see all deployments."
}
```

Endpoint:   ``` GET /service/attendence ```
output:
```
{
  "message": "✅OK as a gurad you can check attendance."
}
```


## Features

- **Authentication**: JWT (JSON Web Tokens) are used for authenticating users.
- **Authorization**: Different roles have access to different sets of services.
- **Roles**:
  - **Guard**: Limited access to services like CCTV surveillance.
  - **Manager**: Extended access to services such as guards deployment and attendance records.
  - **Authority**: Full access to all services, including active units and more.

## Technologies Used

- **Frontend**: React.js
- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **Authentication**: JWT (JSON Web Tokens)
- **Password Hashing**: bcrypt.js



### Clone the repository and install required dependencies in client & server.


