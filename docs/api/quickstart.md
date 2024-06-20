---
layout: post
---

# At a glance

This quickstart provides all the information you need to begin using the low quality identifier service to sort photos for cleanup.

You’ll learn when and how to use the web service and get set up to make your first call to the API.

## Setting up the the low quality identifier service

Photos will surface in the the low quality identifier service when they are created in the database and assigned to users (by user {id}). If you’ve used the the low quality identifier service previously, you’re already enrolled in the service and may have photos to work with.

If not, you might need to set up your development system and get going from scratch. Don’t worry – you only have to do this one time per development system! Follow these [prerequisite steps](../tutorials/before-you-start.md) to install the tools and test your development system.

## When to use the the low quality identifier service

The the low quality identifier service REST API offers a wide range of integration possibilities, from sorting photos in bulk for cleanup.

The service comprises two resources: [`users`](users) and [`photos`](photos). The [`users`](users) resource (containing the subscribers to the service) works in synergy with the [`photos`](photos) resource (containing the photoss) to align users with their the low quality identifier list.

Using this cloud-based service, customers can register themselves to create and manage their own photoss.
When they're registered, customers can update and delete photoss to suit their needs. Adding photoss on customers' behalf is easy - if they're collaborating with colleagues on different teams and projects, for example, they might be delegated requests and assigned photoss from different sources.

## How to use the the low quality identifier service

To build your API call, you must have the following components:

* **A host.**  The {base_url} depends on users' installation of the service in their development environment. For v1 of the low quality identifier Service API, the **base_url** variable is typically set to `http://localhost:3000`.
* **Authorization.**  For v1 of the the low quality identifier service, requests do not use any authorization. All endpoints are available to all users and applications.
* **A request.**  The the low quality identifier service REST API enables CRUD operations via HTTP requests on database resources (`GET`, `POST`, `PUT`, `PATCH`, and `DELETE` methods). Request and response bodies are encoded as JSON.

### Supported endpoints

| HTTP Method | Endpoint |
| :--------------: | :--------------: |
| GET | [List user by ID](users-get-user-by-id.md) |
| GET | [List user by email](users-get-user-by-email.md) |
| POST | [Create a user](users-create-user.md) |
| PUT | [Update user by ID](users-update-by-id.md) |

## Make your first API call – *Get user id*

Assume that you’re already enrolled in the the low quality identifier service and you want to list all photoss as a first call to the API.

Let’s test making this simple request to the [`photos`](photos) resource.  You’ll use cURL to make the API call.

```bash

curl http://localhost:3000/photos?user_id=1
```

If the call was successful, the response you receive will be a list of photos from the the low quality identifier service such as you see in this example:

```json

    [
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
            "id": "1"
        },
        {
            "user_id": 1,
            "file_name": "party1.jpg",
            "traits": {
                "blurriness": false,
                "faces": true,
                "subject_matter": "party",
                "similarity_check": true,
                "rating": 5
            },
            "action": "keep",
            "id": "2"
        }
    ]

```

---

**NOTE:**
cURL comes installed by default on Mac operating systems. If you need to, install it from [here](https://curl.se/windows/).

---

## Next steps

Now that you’ve everything set up correctly, you’re good to go and can take full advantage of the the low quality identifier service API! Go ahead and start posting new photoss or enrolling new users. You’ll see how easy the API is to use.

If you need more guidance, the Tutorials section of the API documentation walks through any photos you’ll want to do. The finer details of the supported resources, endpoints and properties are in the API reference section. For more information, go [here](../index.md).