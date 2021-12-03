
# API_v1_login_auth



## Indices

* [manager](#manager)

  * [Delete user with specific username](#1-delete-user-with-specific-username)
  * [Get all users](#2-get-all-users)
  * [Get user with specific username](#3-get-user-with-specific-username)
  * [Get users with params](#4-get-users-with-params)
  * [Register user](#5-register-user)
  * [Update user with specific username](#6-update-user-with-specific-username)

* [user](#user)

  * [Get user data](#1-get-user-data)
  * [Login user](#2-login-user)
  * [Update user data](#3-update-user-data)
  * [Update user password](#4-update-user-password)


--------


## manager
menadżer użytkowników (admin)



### 1. Delete user with specific username



***Endpoint:***

```bash
Method: DELETE
Type: RAW
URL: {{URL}}/manager/user/12AB
```



### 2. Get all users


pobierz wszystkich użytkowników


***Endpoint:***

```bash
Method: GET
Type: RAW
URL: {{URL}}/manager/users
```



### 3. Get user with specific username



***Endpoint:***

```bash
Method: GET
Type: RAW
URL: {{URL}}/manager/user/12AC
```



### 4. Get users with params



***Endpoint:***

```bash
Method: GET
Type: RAW
URL: {{URL}}/manager/users
```



***Query params:***

| Key | Value | Description |
| --- | ------|-------------|
| client | HumanIT |  |



### 5. Register user


zarządzanie urzytkownikami aplikacji


***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{URL}}/manager/register
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
    "username": "1234",
    "password": "mojehaslo",
    "email": "mail@mail.com",
    "first_name": "piotr",
    "last_name": "cudak",
    "job_function": "pracownik",
    "supervisor": "ktos tam",
    "client": "HumanIT",
    "phone": "123456789",
    "admin": "False"
}
```



### 6. Update user with specific username



***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: {{URL}}/manager/user/12AB
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
    "first_name": "Adam", 
    "last_name": "Kowalski",
    "email": "inny2email@mail.com",
    "phone": "123987453",
    "job_function": "inna rola",
    "supervisor": "inny",
    "client": "inny2",
    "admin": "False"
}
```



## user
Użytkownicy (pracownicy)



### 1. Get user data



***Endpoint:***

```bash
Method: GET
Type: RAW
URL: {{URL}}/user/me
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Authorization | Bearer token |  |



### 2. Login user



***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{URL}}/user/login
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |



***Body:***

```js        
{
    "username": "12AB",
    "password": "mojehaslo"    
}
```



### 3. Update user data



***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: {{URL}}/user/update/data
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |
| Authorization | Bearer token |  |



***Body:***

```js        
{
    "email": "innymail@mail.com",
    "phone": "987654321"
}
```



### 4. Update user password



***Endpoint:***

```bash
Method: PUT
Type: RAW
URL: {{URL}}/user/update/password
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| Content-Type | application/json |  |
| Authorization | Bearer token |  |



***Body:***

```js        
{
    "current_password": "mojehaslo",
    "new_password": "innehaslo"
}
```



---
[Back to top](#api_v1_login_auth)
> Made with &#9829; by [thedevsaddam](https://github.com/thedevsaddam) | Generated at: 2021-12-03 08:08:11 by [docgen](https://github.com/thedevsaddam/docgen)
