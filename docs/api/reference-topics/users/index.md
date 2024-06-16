---
layout: page
title: User resource
---

Base endpoint:

```shell
{base_url}/users
```

Contains information about the users of the service.

To have photos in the service, the user must be added to the service first.

## Resource properties

Sample `user` resource:

```js
{
    "last_name": "Smith",
    "first_name": "Ferdinand",
    "email": "f.smith@example.com",
    "id": 1
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `last_name` | string | The user's last name. |
| `first_name` | string | The user's first name. |
| `email` | string | The user's email address. |
| `id` | string | The user's unique identifier. |

## Operations

The `user` resource supports these operations.

### READ (GET)

* [Get all users](get-all-users)
* [Get users by ID](show-one-user)

### CREATE (POST)

* [Create user](add-new-user)

### UPDATE (PUT)

* [Update user by ID](update-user)

### DELETE

* [Delete user by ID](delete-user)
