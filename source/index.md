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
        "cardRule": {
        	"nameEng": "Normal",
        	"nameTh": "ธรรมดา"
      	},
        "expiryDate": "25/06/2015",
      	"accumulateAmount": 0,
      	"maxAccumulateAmount": 20000
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
        	"cardRule": {
        		"nameEng": "Normal",
        		"nameTh": "ธรรมดา"
      		},
        	"expiryDate": "25/06/2015",
      		"accumulateAmount": 0,
      		"maxAccumulateAmount": 20000
	    },
	    "optionCards": [ ],
	    "accumulatePoint": 0,
	    "accumulatePointExpireDate": "31/12/2015",
	    "accumulatePurchase": 0,
	    "profileImagePath": "http://localhost:8080/customers/image"
	},
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

#### Note
- Case login from offline ที่ไม่ได้ กด forgot password
	{
		"violations": [
			{
				"code": "REQ-10064",
				"field": "getCustomer.account",
				"message": "Update email/password is required"
			}
		],
		"error": "Validation Failure"
	}
- Case มี email แต่ไม่ได้ forgot password
	{
		"violations": [
			{
				"code": "undefined",
				"field": "getCustomer.account",
				"message": "cpo123@mailinator.com"
			},
			{
				"code": "REQ-10084",
				"field": "getCustomer.account",
				"message": "Please change password"
			}
		],
		"error": "Validation Failure"
	}
- Case forgot password  ไม่มี email
	{
		"violations": [
			{
				"code": "undefined",
				"field": "getCustomer.account",
				"message": ""
			},
			{
				"code": "REQ-10164",
				"field": "getCustomer.account",
				"message": "Update email is required"
			}
		],
		"error": "Validation Failure"
	}

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
	    	"addressType" : "ID_CARD_ADDRESS",
	    	"sameIDCardAddress":true
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
	"addressType": "ID_CARD_ADDRESS",
	"sameIDCardAddress":true
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
POST | sameIDCardAddress | boolean | cannot be null

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

## Points History
> Request Get Points History

```shell
curl https://api.cpone-dev.com/customers/points-history?page=1
  -X GET
  -H "Authorization: bearer {access_token}"
```

> Response

```json
{"content":[
	{
      	  "point": 10,
      	  "source": "POS",
      	  "createdDate": "24/06/2015 07:45",
      	  "type": "EARN",
      	  "bu": "CPF",
      	  "rewardNameTh": "Gold status is 500 points for 200 baht discount coupon at Chester's.",
      	  "rewardNameEn": "",
      	  "redeemDate": "20/10/2015 20:17",
      	  "useDate": "20/10/2015 20:17"
    	}
	],
	"last": true,
	"totalPages": 2,
	"totalElements": 21,
	"size": 20,
	"number": 1,
	"sort": null,
	"first": false,
	"numberOfElements": 1
}
```

### Request
`GET https://api.cpone-dev.com/customers/points-history?page={pageIndex}`

### Query Parameters
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
GET | page | Number | page - 1

#### Note
- ค่าของ page ที่ส่งจะเท่ากับ pageที่ต้องการ - 1, เช่น จะแสดง page ที่ 1 จะต้องส่งค่า 0 ไป
- Default page size จะเป็น 20
- จาก response ตัวอย่าง จะเป็นข้อมูลของ page ที่2 มีข้อมูล 1 record(records ที่ 21) 
- ค่าของ source  มีดังนี้"RECEIPT", "POS"
- ค่าของ type มีดังนี้ "REDEEM", "EARN"

## Get Inbox
> Request Get Inbox

```shell
curl https://api.cpone-dev.com/inboxs/customer
  -X GET
  -H "Authorization: bearer {access_token}"
```

> Response

```json
{
  "hasNext": false,
  "size": 20,
  "content": [
    {
      "id": 4,
      "title": "โปรโมชั่น 7-eleven (7-11 เซเว่น อีเลฟเว่น) ประจำเดือนกันยายน 2558",
      "sentDate": "21/10/2015 17:56:07"
    }
  ],
  "hasPrevious": false,
  "number": 0,
  "sort": null,
  "last": true,
  "hasContent": true,
  "totalElements": 1,
  "first": true,
  "totalPages": 1,
  "numberOfElements": 1
}
```

### Request
`GET https://api.cpone-dev.com/inboxs/customer`

## Get Inbox Detail
> Request Get Inbox Detail

```shell
curl https://api.cpone-dev.com/inboxs/3
  -X GET
  -H "Authorization: bearer {access_token}"
```

> Response

```json
{
  "id": 3,
  "title": "โปรโมชั่น Central/ZEN The1Card X-Treme แต้มกระจุย… ช้อปกระจาย",
  "detail": "The 1 Card แลกรับส่วนลด สูงสุด 40%",
  "sentDate": "01/10/2015 15:09:11",
  "hasRead": true,
  "imageUrl": "https://api.cpone-dev.com/inboxs/image/3"
}
```

### Request
`GET https://api.cpone-dev.com/inboxs/{inboxId}`

### Query Parameters
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
GET | inboxId | Number | Inbox ID


# Forgot Password
## Find Mobile
> Request Find Mobile

```shell
curl https://api.cpone-dev.com/forgotpassword/0812345678/findmobile
  -X GET
```

> Response
{
  "mobile": "0830734686"
}

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

# Redeem
> Request Redeem

```shell
curl https://backoffice.cpone-dev.com/redeem/1
  -X GET
```
> Response

```json
{"id":1,"title":"Test Redeem","startDate":"2015-07-07","endDate":null,"point":500,"limit":{"id":1,"limitType":"DAY","limit":1},"available":100,"specialPackages":[{"id":1,"name":"Chester's Extra"},{"id":1,"name":"Chester's Extra"}],"redeemChannels":[{"id":1,"name":"ใช้สิทธิทันที"}],"cardRules":[{"id":1,"nameEng":"Normal","nameTh":"ธรรมดา","requestPurchaseAccumulate":0,"startDate":"2015-07-07","requestStartDate":"07/07/2015","endDate":null,"requestEndDate":null,"requestState":"APPROVE","cardRuleHistories":[{"id":1,"doActionUser":{"id":1,"login":"admin","firstName":"Admin","lastName":"TomatoJuice","email":"admin@cpone.com","activated":true,"department":{"id":"DEV","name":"Software Development"},"enabled":true,"fullName":"Admin TomatoJuice","username":"admin","accountNonExpired":true,"accountNonLocked":true,"credentialsNonExpired":true},"actionDate":"07/07/2015","action":"CREATE","message":"First Card"}],"imageURL":null}],"giftTypes":[{"id":1,"name":"คูปองเงินสด"}],"dayPredicates":[{"id":"MON"},{"id":"TUE"},{"id":"WED"},{"id":"THU"},{"id":"FRI"},{"id":"SAT"},{"id":"SUN"}],"timePeriod":{"id":1,"startTime":"13:42:16","endTime":"13:42:16"}}
```

### Request
`GET https://backoffice.cpone-dev.com/redeem/{redeemId}`

### Query Parameters
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
GET | redeemId | Number |

# All Redeems
> Request All Redeems

```shell
curl https://backoffice.cpone-dev.com/redeems
  -X GET
```
> Response

```json
[{"id":1,"title":"Test Redeem","startDate":"14/07/2015","requestStartDate":"14/07/2015","endDate":null,"requestEndDate":null,"state":"APPROVE","requestState":"APPROVE","point":500,"limit":{"id":1,"limitType":"DAY","limit":1},"available":100,"specialPackages":[{"id":1,"name":"Chester's Extra"}],"redeemChannels":[{"id":1,"name":"ใช้สิทธิทันที"}],"cardRules":[{"id":50,"nameEng":"CP Normal","nameTh":"สฃ"}],"giftTypes":[{"id":1,"name":"คูปองเงินสด"}],"dayPredicates":[{"id":"FRI"},{"id":"MON"},{"id":"SAT"},{"id":"SUN"},{"id":"THU"},{"id":"TUE"},{"id":"WED"}],"timePeriod":{"id":1,"startTime":"18:14:55","endTime":"18:14:55"}},{"id":2,"title":"Test Redeem 2","startDate":"15/07/2015","requestStartDate":"15/07/2015","endDate":null,"requestEndDate":null,"state":"APPROVE","requestState":"APPROVE","point":500,"limit":{"id":1,"limitType":"DAY","limit":1},"available":100,"specialPackages":[{"id":1,"name":"Chester's Extra"}],"redeemChannels":[{"id":1,"name":"ใช้สิทธิทันที"}],"cardRules":[{"id":50,"nameEng":"CP Normal","nameTh":"สฃ"}],"giftTypes":[{"id":1,"name":"คูปองเงินสด"}],"dayPredicates":[{"id":"FRI"},{"id":"MON"},{"id":"SAT"},{"id":"SUN"},{"id":"THU"},{"id":"TUE"},{"id":"WED"}],"timePeriod":{"id":1,"startTime":"18:14:55","endTime":"18:14:55"}}]
```

### Request
`https://backoffice.cpone-dev.com/redeems`

# Redeem Now
> Request Redeem Now

```shell
curl https://api.cpone-dev.com/redeem-now/1
  -X POST
  -H "Authorization: bearer {access_token}"
```
> Response

```json
{
  "rewardCode": "1234567890",
  "timeOut": "300"
}
```

### Request
`https://api.cpone-dev.com/redeem-now/{id}`

### Query Parameters
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
HEAD | Authorization | String | access token from Authentication
POST | id | String | redeem id

#### Note
- Validate example
 {
  "violations": [
    {
      "code": "undefined",
      "field": "redeemNow.reward",
      "message": "may not be null"
    }
  ],
  "error": "Validation Failure"
}

# BzB
## BZB Point (Customer)
> Get BZB Point (Customer)

```shell
curl https://api.cpone-dev.com/api/log/points?type=all&month=2015-09-01
  -X GET
  -H "Authorization: bearer {access_token}"
```

> Response

```json
[{
    "RowKey": "SmoxbXkM_boBfoxck4soPS3pGlMJAvdPV",
    "UserId": "1021823449",
    "Info": {
      "receiveId": "",
      "receiveNo": "",
      "transactionId": "",
      "tranChannel": "",
      "companyId": "",
      "userLevel": "",
      "spending": "",
      "saleChannel": "",
      "day": "",
      "date": "",
      "time": ""
    },
    "Detail": "/api/auth/login",
    "Points": 1,
    "Type": "trace",
    "Timestamp": 1442825483
  },
  {
    "RowKey": "Smp2INE1rzBjRzPRcgyodl8RTd4OzQqI-",
    "UserId": "1021823449",
    "Info": {
      "receiveId": "",
      "receiveNo": "",
      "transactionId": "",
      "tranChannel": "",
      "companyId": "",
      "userLevel": "",
      "spending": "",
      "saleChannel": "",
      "day": "",
      "date": "",
      "time": ""
    },
    "Detail": "/api/auth/login",
    "Points": 1,
    "Type": "trace",
    "Timestamp": 1442200418
  }]
```

### Request
`GET https://api.cpone-dev.com/api/log/points?type={type}&month={month}`

### Query Parameters
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
GET | type | String | Accept: all,earn,burn
GET | month | String | Month and Year to get data in YYYY-MM-DD format.

<aside class="notice">
This will see Point that user get/use (earn/burn) point based on "type" parameter.
</aside>
[API DOC](https://drive.google.com/file/d/0B8jMf5mkjyAdOVFaNV8wTEZPVWc/view?pli=1)

## BZB Redeem (Customer)
> Get BZB Redeem (Customer)

```shell
curl https://api.cpone-dev.com/api/campaign/64735/redeem
  -X POST
  -H "Authorization: bearer {access_token}"
```

> Response

```json
[{
  "CampaignId": 64735,
  "ItemNumber": 14,
  "Serial": "NNGJGUR",
  "AgencyId": 104442,
  "CatId": 900610,
  "Name": "test status publish",
  "NextRedeemDate": null,
  "CurrentDate": 1443190626,
  "PrivilegeMessage": null,
  "RedeemCount": 8,
  "UseCount": 0,
  "Qty": 86,
  "IsConditionPass": true,
  "ConditionAlert": null,
  "IsNotAutoUse": false,
  "PointType": null
}]
```

### Request
`GET https://api.cpone-dev.com/api/campaign/{campaignId}/redeem`

### Query Parameters
TYPE | Params | Value | Detail
---- | ------ | ----- | ------
POST | campaignId | String | Campaign id (e.g. 64735)

<aside class="notice">
This function will be called on campaign redemption. Please note that it will not be used for Type-Buy Campaign.
</aside>
