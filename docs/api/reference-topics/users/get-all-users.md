

# Get all users

Returns all users of the service.

## URL

```shell

{GET} {base_url}/users
```

<!-- ## Authorization -->


## Request headers

| Header name | Description | Required | Values |
| -------------- | ------ | ------------ |------------ |
| Content-Type | The format of the data to be posted. | Optional | application/json. Default value.  |
| Accept | The format of the data to be returned. | Optional | application/json. Default value. |

## Return body

The following example shows the response. 

    ```js
    [
        {
            "last_name": "Smith",
            "first_name": "Ferdinand",
            "email": "f.smith@example.com",
            "id": 1
        },
        {
            "last_name": "Jones",
            "first_name": "Jill",
            "email": "j.jones@example.com",
            "id": 2
        }
    ```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |