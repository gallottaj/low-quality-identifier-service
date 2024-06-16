

# Delete a photo

Use this operation to delete a photo resource. You need to retrieve the photo's id for this operation. Refer to [Show one photo](/show-one-photo.md) to get the photo id.

## URL

```shell

{DELETE} {base_url}/photos/{id}
```

## Params

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `id` | String | The unique identifier of the photo | 

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
    "file_name": "new_photo.jpg",
    "traits": {
        "blurriness": false,
        "faces": false,
        "subject_matter": "landscape",
        "similarity_check": false,
        "rating": 3
    },
    "action": "move_to:/archive",
    "id": "aab5"
  }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |