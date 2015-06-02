---
title: API Reference

search: true
---

# Authentication

> Basic Authen

```shell
curl {client_id}:{client_secret}@https://api.cpone-dev.com/oauth/token 
  -X POST
  -d grant_type=password 
  -d username={username} 
  -d password={password}
```

> Authen Header

```shell
# base64 of client:secret = Y2xpZW50OnNlY3JldA==
curl https://api.cpone-dev.com/oauth/token 
  -X POST
  -H "Authorization: Basic Y2xpZW50OnNlY3JldA==" 
  -d grant_type=password 
  -d username={username} 
  -d password={password}
```
> Response

```json
{
    "access_token": "40fb50a4-e0f8-42bd-b909-405e3654ed0b",
    "token_type": "bearer",
    "refresh_token": "0626a0d1-5a93-4e43-9fb9-0a2c38945718",
    "expires_in": 43199,
    "scope": "global"
}
```

### Request
`POST https://api.cpone-dev.com/oauth/token`

### Query Parameters
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
HEAD | Authorization | String | CLIENT_ID:CLIENT_SECRET base64 encrypt
POST | grant_type | String | Fix value to "password"
POST | username | String |
POST | password | String |

<aside class="notice">
You must replace <code>{client_id}</code> and <code>{client_secret}</code> with your personal API key.
</aside>

# Logout
> Request Logout

```shell
curl https://api.cpone-dev.com/logout
  -X POST
  -H "Authorization: bearer {access_token}"
```

### Request
`POST https://api.cpone-dev.com/logout`

### Query Parameters
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
HEAD | Authorization | String | access token from [Authentication](#authentication)

# Send OTP
> Request Send OTP

```shell
curl https://api.cpone-dev.com/otp/request
  -X POST
  -d mobile={mobile} 
```

### Request
`POST https://api.cpone-dev.com/otp/request`

### Query Parameters
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
POST | mobile | String | 

# Customer
## Register

> Request Send Register Data

```shell
curl https://api.cpone-dev.com/customers/register
  -X POST
  -H "Content-Type: application/json"
  -d '{
         "otpNumber":"{otpNumber}",
         "thaiId":"3670301396484",
         "email":"megaspeed@example.com",
         "mobile":"0879630303",
         "password":"123456",
         "firstName":"ฝอย",
         "lastName":"ขัดหม้อ",
         "birthDate":"03/04/2015",
         "registerChannel":"MOBILE",
         "title":{
            "id":1
         }
      }'
```

> Response

```json
{
    "id": 33,
    "thaiId": "3670301396484",
    "email": "megaspeed@example.com",
    "mobile": "0879630303",
    "firstName": "ฝอย",
    "lastName": "ขัดหม้อ",
    "title": {
        "id": 1,
        "nameTh": "นาย",
        "nameEn": "Mr.",
        "gender": "MALE"
    },
    "birthDate": "03/04/2015",
    "registerChannel": "MOBILE",
    "phone": null,
    "addresses": [],
    "cpOneCard": {
        "id": 33,
        "cardNumber": "0001000000000033",
        "cardLevel": {
            "id": 1,
            "name": "Normal"
        },
        "expiryDate": "28/05/2016"
    }
}
```

### Request
`POST https://api.cpone-dev.com/customers/register`

### Query Parameters
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
HEAD | Content-Type | String | Fix value to "application/json"
POST | otpNumber | String | [Send OTP](#send-otp)
POST | thaiId | String |
POST | email | String |
POST | mobile | String |
POST | password | String |
POST | firstName | String |
POST | lastName | String |
POST | birthDate | Date | Format : dd/MM/yyyy
POST | registerChannel | String | Accept : MOBILE,WEB,CALL
POST | title | Object | see. Title Object table

### Title Object
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
POST | id | Number | 1=Mr. 2=Mrs. 3=Ms. 4=Mstr. 5=Miss

## Register Validation

> Request Send Register Data

```shell
curl https://api.cpone-dev.com/customers/pre-register
  -X POST
  -H "Content-Type: application/json"
  -d '{
         "otpNumber":"{otpNumber}",
         "thaiId":"3670301396484",
         "email":"megaspeed@example.com",
         "mobile":"0879630303",
         "password":"123456",
         "firstName":"ฝอย",
         "lastName":"ขัดหม้อ",
         "birthDate":"03/04/2015",
         "registerChannel":"MOBILE",
         "title":{
            "id":1
         }
      }'
```

> Response


### Request
`POST https://api.cpone-dev.com/customers/pre-register`

### Query Parameters
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
HEAD | Content-Type | String | Fix value to "application/json"
POST | otpNumber | String | [Send OTP](#send-otp)
POST | thaiId | String |
POST | email | String |
POST | mobile | String |
POST | password | String |
POST | firstName | String |
POST | lastName | String |
POST | birthDate | Date | Format : dd/MM/yyyy
POST | registerChannel | String | Accept : MOBILE,WEB,CALL
POST | title | Object | see. Title Object table

### Title Object
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
POST | id | Number | 1=Mr. 2=Mrs. 3=Ms. 4=Mstr. 5=Miss

## Get Profile
> Request Get Profile

```shell
curl https://api.cpone-dev.com/customers
  -X GET
  -H "Authorization: bearer {access_token}"
```

> Response

```json
{
    "id": 33,
    "thaiId": "3670301396484",
    "email": "megaspeed@example.com",
    "mobile": "0879630303",
    "firstName": "ฝอย",
    "lastName": "ขัดหม้อ",
    "title": {
        "id": 1,
        "nameTh": "นาย",
        "nameEn": "Mr.",
        "gender": "MALE"
    },
    "birthDate": "03/04/2015",
    "registerChannel": "MOBILE",
    "phone": null,
    "addresses": [],
    "cpOneCard": {
        "id": 33,
        "cardNumber": "0001000000000033",
        "cardLevel": {
            "id": 1,
            "name": "Normal"
        },
        "expiryDate": "28/05/2016"
    }
}
```

### Request
`GET https://api.cpone-dev.com/customers`

### Query Parameters
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
HEAD | Authorization | String | access token from [Authentication](#authentication)

## Get Profile Image
> Request Get Profile Image

```shell
curl https://api.cpone-dev.com/customers/image
  -X GET
  -H "Authorization: bearer {access_token}"
```

### Request
`GET https://api.cpone-dev.com/customers/image`

### Query Parameters
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
HEAD | Authorization | String | access token from [Authentication](#authentication)

## Upload Profile Image
> Request Upload Profile Image

```shell
curl https://api.cpone-dev.com/customers/image/upload
  -X POST
  -H "Authorization: bearer {access_token}"
  -F "file=@{file}"
```

### Request
`POST https://api.cpone-dev.com/customers/image/upload`

### Query Parameters
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
HEAD | Authorization | String | access token from [Authentication](#authentication)
POST | file | File | image file for upload

# Forgot Password
## Find Mobile
## Verify OTP
## Change Password

## Update Email Validation
> Request Update Email Validation

```shell
curl https://api.cpone-dev.com/pre-update-email/
  -X POST
  -H "Authorization: bearer {access_token}"
  -d '{
		"email" : "a@a.com",
		"password" : "1234"
	}'
```

> Response



### Request
`POST https://api.cpone-dev.com/pre-update-email/`

### Query Parameters
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
HEAD | Content-Type | String | Fix value to "application/json"
POST | email | String | 
POST | password | String | 
