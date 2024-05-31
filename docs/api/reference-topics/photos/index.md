---
layout: page
---
# `photo` resource

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
| `user_id` | string | The user's last name |
| `file_name` | string | The user's first name |
| `traits` | string | The user's email address |
| `traits.blurriness` | number | The user's unique record ID |
| `traits.faces` | number | The user's unique record ID |
| `traits.subject_matter` | number | The user's unique record ID |
| `traits.similarity_check` | number | The user's unique record ID |
| `traits.rating` | number | The user's unique record ID |
| `action.move_to` | number | The user's unique record ID |
| `action.id` | number | The user's unique record ID |


## Operations

The `user` resource supports these operations.

### READ (GET)

* [Get all users](users-get-all-users)
* [Get users by ID](users-get-user-by-id)

### CREATE (POST)

* [Create user](users-create-user)

### UPDATE (PUT)

* [Update user by ID](users-update-by-id)

### DELETE

* [Delete user by ID](users-delete-user-by-id)
