---
title: API Reference

search: true
---

# Master Data

## All Titles
> Request Get All Titles

```shell
curl https://api.cpone-dev.com/public/titles
  -X GET
```

> Response

```json
[ {
  "id" : 1,
  "nameTh" : "นาย",
  "nameEn" : "Mr.",
  "gender" : "MALE"
}, {
  "id" : 2,
  "nameTh" : "นาง",
  "nameEn" : "Mrs.",
  "gender" : "FEMALE"
}, {
  "id" : 3,
  "nameTh" : "นางสาว",
  "nameEn" : "Ms.",
  "gender" : "FEMALE"
}, {
  "id" : 4,
  "nameTh" : "เด็กชาย",
  "nameEn" : "Mstr.",
  "gender" : "MALE"
}, {
  "id" : 5,
  "nameTh" : "เด็กหญิง",
  "nameEn" : "Miss",
  "gender" : "FEMALE"
} ]
```

### Request
`GET https://api.cpone-dev.com/public/titles`

## Title
> Request Get Title by ID

```shell
curl https://api.cpone-dev.com/public/titles/1
  -X GET
```

> Response

```json
{
  "id" : 1,
  "nameTh" : "นาย",
  "nameEn" : "Mr.",
  "gender" : "MALE"
}
```

### Request
`GET https://api.cpone-dev.com/public/titles/{id}`

### Query Parameters
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
PATH | id | Number | The title id.

## All Provinces
> Request Get All Provinces

```shell
curl https://api.cpone-dev.com/public/provinces
  -X GET
```

> Response

```json
[ {
  "id" : 1,
  "name" : "กรุงเทพฯ"
}, {
  "id" : 2,
  "name" : "นครปฐม"
} ]
```

### Request
`GET https://api.cpone-dev.com/public/provinces`

<aside class="notice">
All Provinces sort by name
</aside>

## Province
> Request Get Province by ID

```shell
curl https://api.cpone-dev.com/public/provinces/1
  -X GET
```

> Response

```json
{
  "id" : 1,
  "name" : "กรุงเทพฯ"
}
```

### Request
`GET https://api.cpone-dev.com/public/provinces/{id}`

### Query Parameters
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
PATH | id | Number | The province id.

## All Districts in Province
> Request Get All Districts by Province ID

```shell
curl https://api.cpone-dev.com/public/provinces/1/districts
  -X GET
```

> Response

```json
[ {
  "id" : 1,
  "name" : "ดินแดง"
}, {
  "id" : 2,
  "name" : "ห้วยขวาง"
} ]
```

### Request
`GET https://api.cpone-dev.com/public/provinces/{id}/districts`

### Query Parameters
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
PATH | id | Number | The province id.

<aside class="notice">
All Districts sort by name
</aside>

## All Districts
> Request Get All Districts

```shell
curl https://api.cpone-dev.com/public/districts
  -X GET
```

> Response

```json
[ {
  "id" : 1,
  "name" : "ดินแดง"
}, {
  "id" : 3,
  "name" : "พุทธมณฑล"
}, {
  "id" : 4,
  "name" : "สามพราน"
}, {
  "id" : 2,
  "name" : "ห้วยขวาง"
} ]
```

### Request
`GET https://api.cpone-dev.com/public/districts`

<aside class="notice">
All Districts sort by name
</aside>

## District
> Request Get District by ID

```shell
curl https://api.cpone-dev.com/public/districts/1
  -X GET
```

> Response

```json
{
  "id" : 1,
  "name" : "ดินแดง"
}
```

### Request
`GET https://api.cpone-dev.com/public/districts/{id}`

### Query Parameters
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
PATH | id | Number | The district id.

## All Sub-Districts in District
> Request Get All Sub-Districts by District ID

```shell
curl https://api.cpone-dev.com/public/districts/1/subdistricts
  -X GET
```

> Response

```json
[ {
  "id" : 1,
  "name" : "ดินแดง",
  "postCode" : "10400"
} ]
```

### Request
`GET https://api.cpone-dev.com/public/districts/{id}/subdistricts`

### Query Parameters
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
PATH | id | Number | The district id.

<aside class="notice">
All Sub-Districts sort by name
</aside>

## All Sub-Districts
> Request Get All Sub-Districts

```shell
curl https://api.cpone-dev.com/public/subdistricts
  -X GET
```

> Response

```json
[ {
  "id" : 17,
  "name" : "กระทุ่มล้ม",
  "postCode" : "73220"
}, {
  "id" : 20,
  "name" : "คลองจินดา",
  "postCode" : "73110"
}, {
  "id" : 6,
  "name" : "คลองโยง",
  "postCode" : "73170"
}, {
  "id" : 18,
  "name" : "คลองใหม่",
  "postCode" : "73110"
}, {
  "id" : 1,
  "name" : "ดินแดง",
  "postCode" : "10400"
}, {
  "id" : 19,
  "name" : "ตลาดจินดา",
  "postCode" : "73110"
}, {
  "id" : 9,
  "name" : "ทรงคนอง",
  "postCode" : "73210"
}, {
  "id" : 8,
  "name" : "ท่าข้าม",
  "postCode" : "73110"
}, {
  "id" : 16,
  "name" : "ท่าตลาด",
  "postCode" : "73110"
}, {
  "id" : 11,
  "name" : "บางกระทึก",
  "postCode" : "73210"
}, {
  "id" : 3,
  "name" : "บางกะปิ",
  "postCode" : "10310"
}, {
  "id" : 14,
  "name" : "บางช้าง",
  "postCode" : "73110"
}, {
  "id" : 12,
  "name" : "บางเตย",
  "postCode" : "73210"
}, {
  "id" : 22,
  "name" : "บ้านใหม่",
  "postCode" : "73110"
}, {
  "id" : 7,
  "name" : "มหาสวัสดิ์",
  "postCode" : "73170"
}, {
  "id" : 21,
  "name" : "ยายชา",
  "postCode" : "73110"
}, {
  "id" : 5,
  "name" : "ศาลายา",
  "postCode" : "73170"
}, {
  "id" : 13,
  "name" : "สามพราน",
  "postCode" : "73110"
}, {
  "id" : 4,
  "name" : "สามเสนนอก",
  "postCode" : "10310"
}, {
  "id" : 10,
  "name" : "หอมเกร็ด",
  "postCode" : "73110"
}, {
  "id" : 2,
  "name" : "ห้วยขวาง",
  "postCode" : "10310"
}, {
  "id" : 23,
  "name" : "อ้อมใหญ่",
  "postCode" : "73160"
}, {
  "id" : 15,
  "name" : "ไร่ขิง",
  "postCode" : "73210"
} ]
```

### Request
`GET https://api.cpone-dev.com/public/subdistricts`

<aside class="notice">
All Sub-Districts sort by name
</aside>

## Sub-District
> Request Get Sub-District by ID

```shell
curl https://api.cpone-dev.com/public/subdistricts/1
  -X GET
```

> Response

```json
{
  "id" : 1,
  "name" : "ดินแดง",
  "postCode" : "10400"
}
```

### Request
`GET https://api.cpone-dev.com/public/subdistricts/{id}`

### Query Parameters
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
PATH | id | Number | The sub-district id.

# Authentication

## Get Token
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

## Refresh Token

> Request Refresh Token

```shell
curl {client_id}:{client_secret}@https://api.cpone-dev.com/oauth/token 
  -X POST
  -d grant_type=refresh_token 
  -d refresh_token={refresh_token} 
```

> Response

```json
{
    "access_token": "31a3f8dd-4727-4215-9d8d-659393f698e8",
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
POST | grant_type | String | Fix value to "refresh_token"
POST | refresh_token | String | refresh_token value get from [Get Token](#get-token)

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
HEAD | Authorization | String | Access token from [Authentication](#authentication)

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
POST | mobile | String | Numeric 10 digits.

### Response
#### Error Example
{
  "violations" : [ {
    "code" : "SIZ-10070",
    "field" : "request.mobile",
    "message" : "จำนวนตัวเลขเบอร์โทรศัพท์ไม่ถูกต้อง (10 หลัก)"
  } ],
  "error" : "Validation Failure"
}

# Customer

## Register Validation

> Request Send Register Data

```shell
curl https://api.cpone-dev.com/customers/pre-register
  -X POST
  -H "Content-Type: application/json"
  -d '{
         "otpNumber" : "{otpNumber}",
         "thaiId" : "3670301396484",
         "email" : "megaspeed@example.com",
         "mobile" : "0879630303",
         "password" : "123456",
         "firstName" : "กุ๊ก",
         "lastName" : "กิ๊ก",
         "birthDate" : "03/04/2015",
         "registerChannel" : "MOBILE",
         "title" : {
            "id" : 1
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
POST | thaiId | String | Numeric 13 digits.
POST | email | String | *Optional parameter.<br/>Standard email format.<br/>Max 100 characters.
POST | mobile | String | Numeric 10 digits.
POST | password | String | Allowed characters: A-Z, a-z, 0-9
POST | firstName | String | Thai or English characters.<br/>Max 50 characters.
POST | lastName | String | Thai or English characters.<br/>Max 50 characters.
POST | birthDate | Date | Format: dd/MM/yyyy
POST | registerChannel | String | Accept: MOBILE, WEB, CALL
POST | title | Object | See: Title Object table.

### Title Object
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
POST | id | Number | 1=Mr. 2=Mrs. 3=Ms. 4=Mstr. 5=Miss

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
POST | thaiId | String | Numeric 13 digits.
POST | email | String | *Optional parameter.<br/>Standard email format.<br/>Max 100 characters.
POST | mobile | String | Numeric 10 digits.
POST | password | String | Allowed characters: A-Z, a-z, 0-9
POST | firstName | String | Thai or English characters.<br/>Max 50 characters.
POST | lastName | String | Thai or English characters.<br/>Max 50 characters.
POST | birthDate | Date | Format: dd/MM/yyyy
POST | registerChannel | String | Accept: MOBILE,WEB,CALL
POST | title | Object | See: Title Object table.

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
	"customer": {
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
	        "expiryDate": "28/05/2016",
	        "accumulateAmount": 0,
	        "maxAccumulateAmount": 0
	    },
	    "optionCards": [ ],
	    "points": [ ],
	    "accumulatePoint": 0,
	    "accumulatePointExpireDate": "31/12/2015",
	    "accumulatePurchase": 0,
	    "profileImagePath": "http://localhost:8080/customers/image"
	},
	"point": 999999,
	"coupon": 999,
	"notificationCount": 999,
	"lastUpdatedRedeem": "17/06/2015 09:29:09",
	"lastUpdatedGift": "17/06/2015 09:29:09",
	"giftCount": 999
}
```

### Request
`GET https://api.cpone-dev.com/customers`

### Query Parameters
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
HEAD | Authorization | String | Access token from [Authentication](#authentication)

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
HEAD | Authorization | String | Access token from [Authentication](#authentication)

## Update Profile
> Request Update Profile

```shell
curl https://api.cpone-dev.com/update-profile
  -X POST
  -H "Authorization: bearer {access_token}"
  -H "Content-Type: application/json"
  -d '{
		"firstName" : "กุ๊ก",
		"lastName" : "กิ๊ก",
		"birthDate" : "12/03/2015",
		"phone" : "021234567",
		"title" : {
      			"id" : 2
   		}
	}'
```

> Response


### Request
`POST https://api.cpone-dev.com/update-profile`

### Query Parameters
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
HEAD | Authorization | String | Access token from [Authentication](#authentication)
HEAD | Content-Type | String | Fix value to "application/json"
POST | firstName | String | Thai or English characters.<br/>Max 50 characters.
POST | lastName | String | Thai or English characters.<br/>Max 50 characters.
POST | birthDate | Date | Format: dd/MM/yyyy
POST | phone | String | Max 20 digits.
POST | title | Object | See: Title Object table.

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
HEAD | Authorization | String | Access token from [Authentication](#authentication)
POST | file | File | Max file size 3 MB<br/>Allowed extension: ".png", ".jpg", ".jpeg"

## Update Password
> Request Update Password

```shell
curl https://api.cpone-dev.com/update-password
  -X POST
  -H "Authorization: bearer {access_token}"
  -H "Content-Type: application/json"
  -d '{
		"oldPassword" : "password",
		"newPassword" : "newpassword"
	}'
```

> Response


### Request
`POST https://api.cpone-dev.com/update-password`

### Query Parameters
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
HEAD | Authorization | String | Access token from [Authentication](#authentication)
HEAD | Content-Type | String | Fix value to "application/json"
POST | oldPassword | String |
POST | newPassword | String | Must not be closely similar to a previously used password.<br/>Allowed characters: A-Z, a-z, 0-9

## Update Address
> Request Update Address

```shell
curl https://api.cpone-dev.com/update-address
  -X POST
  -H "Authorization: bearer {access_token}"
  -H "Content-Type: application/json"
  -d '{
	    	"houseNo" : "11/12",
	    	"villageNo" : "8",
	    	"buildingVillage" : "ตึก AIA Capital Center",
	    	"laneAlley" : "รัชดาซอย 4",
	    	"road" : "ถนนรัชดาภิเษก",
	    	"provinceId" : 1,
	    	"districtId" : 1,
	    	"subDistrictId" : 1,
	    	"postCode" : "76543",
	    	"addressType" : "ID_CARD_ADDRESS"
	}'
```

> Response

```json
{
	"id": 4,
	"houseNo": "11/12",
	"villageNo": "8",
	"buildingVillage": "ตึก AIA Capital Center",
	"laneAlley": "รัชดาซอย 4",
	"road": "ถนนรัชดาภิเษก",
	"province": {
		"id": 1,
		"name": "กรุงเทพฯ"
	},
	"district": {
		"id": 1,
		"name": "ดินแดง"
	},
	"subDistrict": {
		"id": 1,
		"name": "ดินแดง",
		"postCode": "10400"
	},
	"postCode": "76543",
	"addressType": "ID_CARD_ADDRESS"
}
```

### Request
`POST https://api.cpone-dev.com/update-address`

### Query Parameters
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
HEAD | Authorization | String | Access token from [Authentication](#authentication)
HEAD | Content-Type | String | Fix value to "application/json"
POST | houseNo | String | Required.<br/>Max 10 characters.
POST | villageNo | String | Max 10 characters.
POST | buildingVillage | String | Max 50 characters.
POST | laneAlley | String | Max 50 characters.
POST | road | String | Max 50 characters.
POST | provinceId | Number | Required.
POST | districtId | Number | Required.
POST | subDistrictId | Number | Required.
POST | postCode | String | Required.<br/>Numeric 5 digits.
POST | addressType | String | Required.<br/>Accept: ID_CARD_ADDRESS, SHIPPING_ADDRESS

## Update Email Validation
> Request Update Email Validation

```shell
curl https://api.cpone-dev.com/pre-update-email-only
  -X POST
  -H "Authorization: bearer {access_token}"
  -H "Content-Type: application/json"
  -d '{
		"email" : "a@a.com"
	}'
```

> Response


### Request
`POST https://api.cpone-dev.com/pre-update-email-only`

### Query Parameters
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
HEAD | Content-Type | String | Fix value to "application/json"
POST | email | String | 

## Update Email
> Request Update Email

```shell
curl https://api.cpone-dev.com/update-email-only
  -X POST
  -H "Authorization: bearer {access_token}"
  -H "Content-Type: application/json"
  -d '{
		"email" : "a@a.com"
	}'
```

> Response


### Request
`POST https://api.cpone-dev.com/update-email-only`

### Query Parameters
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
HEAD | Content-Type | String | Fix value to "application/json"
POST | email | String | 

## Update Mobile Number
> Request Update Mobile Number

```shell
curl https://api.cpone-dev.com/update-mobile
  -X POST
  -H "Authorization: bearer {access_token}"
  -H "Content-Type: application/json"
  -d '{
		"mobile" : "0822222222",
		"otpNumber" : "192150"
	}'
```

> Response


### Request
`POST https://api.cpone-dev.com/update-mobile`

### Query Parameters
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
HEAD | Content-Type | String | Fix value to "application/json"
POST | mobile | String | Numeric 10 digits.
POST | otpNumber | String | [Send OTP](#send-otp)

## Update Email/Password via Offline Channel Validation
> Request Update Email/Password via Offline Channel Validation

```shell
curl https://api.cpone-dev.com/pre-email-password
  -X POST
  -H "Authorization: bearer {access_token}"
  -H "Content-Type: application/json"
  -d '{
		"email" : "a@a.com",
		"password" : "password"
	}'
```

> Response


### Request
`POST https://api.cpone-dev.com/pre-email-password`

### Query Parameters
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
HEAD | Content-Type | String | Fix value to "application/json"
POST | email | String | 
POST | password | String | 

## Update Email/Password via Offline Channel
> Request Update Email/Password via Offline Channel

```shell
curl https://api.cpone-dev.com/update-email-password
  -X POST
  -H "Authorization: bearer {access_token}"
  -H "Content-Type: application/json"
  -d '{
		"email" : "a@a.com",
		"password" : "password"
	}'
```

> Response


### Request
`POST https://api.cpone-dev.com/update-email-password`

### Query Parameters
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
HEAD | Content-Type | String | Fix value to "application/json"
POST | email | String | 
POST | password | String | 

## Points-History
> Request Get Points-History

```shell
curl https://api.cpone-dev.com/customers/points-history?page=0
  -X GET
  -H "Authorization: bearer {access_token}"
```

> Response

```json
{"content":[
	{"id":{"companyId":1,"storeId":1,"customerId":1,"transactionId":1},"point":99,"store":{"id":1,"name":"Default Store","shortName":null,"address1":null,"address2":null,"province":null,"district":null,"postCode":null,"telephone":null,"company":{"id":1,"name":"CP Freshmart","store":[]}},"source":"POS"},
	{"id":{"companyId":1,"storeId":1,"customerId":1,"transactionId":2},"point":88,"store":{"id":1,"name":"Default Store","shortName":null,"address1":null,"address2":null,"province":null,"district":null,"postCode":null,"telephone":null,"company":{"id":1,"name":"CP Freshmart","store":[]}},"source":"POS"},
	{"id":{"companyId":1,"storeId":1,"customerId":1,"transactionId":3},"point":77,"store":{"id":1,"name":"Default Store","shortName":null,"address1":null,"address2":null,"province":null,"district":null,"postCode":null,"telephone":null,"company":{"id":1,"name":"CP Freshmart","store":[]}},"source":"POS"}],
	"totalPages":1,"totalElements":3,"last":true,"size":20,"number":0,"first":true,"sort":null,"numberOfElements":3}
```

### Request
`GET https://api.cpone-dev.com/customers/points-history?page={pageIndex}

### Query Parameters
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
GET | page | Number | page - 1

#### Note
- ค่าของ page ที่ส่งจะเท่ากับ pageที่ต้องการ - 1, เช่น จะแสดง page ที่ 1 จะต้องส่งค่า 0 ไป
- Default page size จะเป็น 20

# Forgot Password
## Find Mobile
> Request Find Mobile

```shell
curl https://api.cpone-dev.com/forgotpassword/0812345678/findmobile
  -X GET
```

> Response
0812345678

### Request
`GET https://api.cpone-dev.com/forgotpassword/{cponeId}/findmobile`

### Query Parameters
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
PATH | cponeId | String |

## Verify OTP
> Request Verify OTP

```shell
curl https://api.cpone-dev.com/forgotpassword/verifyotp
  -X POST
  -H "Content-Type: application/json"   
  -d '{ 		   
		"mobile" : "{mobile number from find mobile}",
		"otpNumber" : "{otp number}" 		
	}'
```

> Response

### Request
`POST https://api.cpone-dev.com/forgotpassword/verifyotp`

### Query Parameters
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
HEAD | Content-Type | String | Fix value to "application/json"
POST | mobile | Number |
POST | otpNumber | Number |

## Change Password
> Request Change Password

```shell
curl https://api.cpone-dev.com/forgotpassword/changepassword/
  -X POST
  -H "Content-Type: application/json"   
  -d '{
		"mobile" : "{mobile number}",
		"otpNumber" : "{opt number}",
		"password" : "{new password}"
	}'
```

> Response

### Request
`POST https://api.cpone-dev.com/forgotpassword/changepassword/`

### Query Parameters
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
HEAD | Content-Type | String | Fix value to "application/json"
POST | mobile | Number |
POST | otpNumber | Number |
POST | password | String |

# Upload Receipt Image
> Request Upload Receipt Image

```shell
curl https://api.cpone-dev.com/upload-receipt
  -X POST
  -H "Authorization: bearer {access_token}"
  -F "file=@{file}"
```

### Request
`POST https://api.cpone-dev.com/upload-receipt`

### Query Parameters
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
HEAD | Authorization | String | access token from [Authentication](#authentication)
POST | file | File | Max file size 3 MB<br/>Allowed extension: ".png", ".jpg", ".jpeg"
