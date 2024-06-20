---
layout: post
---

# Add a new user

Use this operation to create a new user.

## URL

```shell

{POST} {base_url}/users
```

## Params

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `last_name` | String | The user's last name | 
| `first_name` | String | The user's first name | 
| `email` | String | The user's email address | 



## Request headers

This request does not use any authorization. The endpoint is available to all tasks and applications.

| Header name | Description | Required | Values |
| -------------- | ------ | ------------ |------------ |
| Content-Type | The format of the data to be posted. | Optional | application/json. Default value.  |
| Accept | The format of the data to be returned. | Optional | application/json. Default value. |


## Request body

```json
[
    {
      "last_name": "Doe",
      "first_name": "John",
      "email": "j.doe@example.com",
    }
]
```

## Return body

The following example shows the response. 

```json
[
    {
      "last_name": "Doe",
      "first_name": "John",
      "email": "j.doe@example.com",
      "id": 1
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 201 | Created | The request has been fulfilled and resulted in a new resource being created. |
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |