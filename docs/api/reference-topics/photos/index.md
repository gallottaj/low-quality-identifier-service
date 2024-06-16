---
layout: post
---

# Photo resource

Base endpoint:

```shell
{{base_url}}/photos
```

Contains information about the users of the service.

To add photos, the user must be added to the service first.

## Resource properties

Sample `photo` resource

```js
{
    "user_id": 1,
    "file_name": "vacation1.jpg",
    "traits": {
      "blurriness": true,
      "faces": true,
      "subject_matter": "landscape",
      "similarity_check": false,
      "rating": 3
    },
    "action": "move_to:/archive",
    "id": 1
  }
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `user_id` | string | The unique identifier of the user who owns the photo.  |
| `file_name` | string | The name of the photo file. |
| `traits` | string | The traits noted in the phoot. |
| `traits.blurriness` | boolean | Indicates if the photo is blurry. |
| `traits.faces` | boolean | Indicates if there are faces in the photo. |
| `traits.subject_matter` | string | The subject of what's in the photo. |
| `traits.similarity_check` | boolean | Indicates if the photo is similar to another photo. |
| `traits.rating` | number | The rating of the traits in the photo. |
| `action` | string | Indicates the actions to be taken based on the photo check. |
| `action.id` | string | The unique identifier of the action. |


<!-- ## Operations

The `user` resource supports these operations.

### READ (GET)

* [Get all users](users-get-all-users)
* [Get users by ID](users-get-user-by-id)

### CREATE (POST)

* [Create user](users-create-user)

### UPDATE (PUT)

* [Update user by ID](users-update-by-id)

### DELETE

* [Delete user by ID](users-delete-user-by-id) -->
