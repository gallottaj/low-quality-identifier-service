---
layout: post
---

# Add a new photo

Use this operation to create a new photo resource.

## URL

```shell

{POST} {base_url}/photos
```

## Params

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `file_name` | String | The name of the photo file | 
| `traits.blurriness` | Boolean | Indicates if the photo is blurry | 
| `traits.faces` | Boolean | Indicates if the photo contains faces |
| `traits.subject_matter` | String | Description of the subject of the photo | 
| `traits.similarity_check` | Boolean | Indicates the similiary of the photo | 
| `traits.rating` | Number | Quality rating of the photo |
| `action` | String | Specifies the action to take on the photo |   

## Request headers

This request does not use any authorization. The endpoint is available to all tasks and applications.

| Header name | Description | Required | Values |
| -------------- | ------ | ------------ |------------ |
| Content-Type | The format of the data to be posted. | Optional | application/json. Default value.  |
| Accept | The format of the data to be returned. | Optional | application/json. Default value. |


## Request body

```js
[
    {
      "file_name": "new_photo.jpg",
      "traits": {
        "blurriness": true,
        "faces": true,
        "subject_matter": "landscape",
        "similarity_check": false,
        "rating": 3
      },
      "action": "move_to:/archive"
    }
]
```

## Response body

The following example shows the response. 

```js
[
  {
    "id": "aab5",
    "file_name": "new_photo.jpg",
    "traits": {
        "blurriness": true,
        "faces": true,
        "subject_matter": "landscape",
        "similarity_check": false,
        "rating": 3
    },
    "action": "move_to:/archive"
  }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 201 | Created | The request has been fulfilled and resulted in a new resource being created. |
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |