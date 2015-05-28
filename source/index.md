---
title: API Reference

language_tabs:
  - Mobile/Web
  - POS

search: true
---

# Authentication

### Request

> Basic Authen

```shell
curl {client_id}:{client_secret}@https://api.cpone-dev.com/oauth/token 
  -d grant_type=password 
  -d username={username} 
  -d password={password}
```

> Authen Header

```shell
# base64 of client:secret = Y2xpZW50OnNlY3JldA==
curl https://api.cpone-dev.com/oauth/token 
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