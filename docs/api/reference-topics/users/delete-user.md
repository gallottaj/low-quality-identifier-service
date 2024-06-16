---
layout: post
---

# Delete a user

Use this operation to delete a user resource. You need to retrieve the user's id for this operation. Refer to [Read one user](/read-one-user.md) to get the user id.

## URL

```shell

{DELETE} {base_url}/users/{id}
```

## Params

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `id` | String | The unique identifier of the user | 

## Request headers

This request does not use any authorization. The endpoint is available to all tasks and applications.

| Header name | Description | Required | Values |
| -------------- | ------ | ------------ |------------ |
| Content-Type | The format of the data to be posted. | Optional | application/json. Default value.  |
| Accept | The format of the data to be returned. | Optional | application/json. Default value. |


## Request body

None

## Return body

The following example shows the response. 

```js
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
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |