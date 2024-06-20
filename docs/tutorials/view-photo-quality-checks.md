---
layout: post
---

# Tutorial: View photo quality check

In this tutorial, you'll learn the operations needed to view the photo quality check results. The photo quality check results include the `traits`, which are the undesireable traits detected in the photo, and an `action` which indicates how to handle the photo.

Expect this tutorial to take about 15 minutes to complete.

## Before you start

Make sure you've completed the [Before you start a tutorial](before-you-start-a-tutorial) topic on the development system you'll use for the tutorial.

## Retreive user id

Viewing a specific photo requires knowing the user's id.

To retrieve a user id:

1. Make sure your local service is running, or start it by using this command, if it's not.

    ```shell
    cd <your-github-workspace>/low-quality-identifier-service/api
    json-server -w low-quality-identifier-service-source.json
    ```

1. Open the Postman app on your desktop.
1. In the Postman app, create a new request with these values:
    * **METHOD**: GET
    * **URL**: `{{base_url}}/users`
    * **Headers**:`Content-Type: application/json`
    * **Parameters**: `email`
    Enter the user's email address in the parameter value.

1. In the Postman app, choose **Send** to make the request.
1. Watch for the response body, which should look something like this. Note that the names should be the same as you used in your **Request body** and the response should include the user's `id`. You will need this `id` value in the next step.

    ```json
    [
        {
            "last_name": "Doe",
            "first_name": "John",
            "email": "j.doe@example.com",
            "id": "1"
        }
    ]
    ```
## Retreive a photo to see its traits

1. Make sure your local service is running, or start it by using this command, if it's not.

    ```shell
    cd <your-github-workspace>/low-quality-identifier-service/api
    json-server -w low-quality-identifier-service-source.json
    ```

1. Open the Postman app on your desktop.
1. In the Postman app, create a new request with these values:

    * **Method**: Get
    * **Authorization**: Basic Auth (`username`/`password`)
    * **URL**: `{base_url}/photos`
    * **Headers**:`Content-Type: application/json`
    * **Parameters**: `user_id`
    Enter the user's id in the parameter value.

1. In the Postman app, choose **Send** to make the request.
1. Watch for the response body, which should look something like this. The response body will show all photos that belong to the user. 

Note the `trait` and `action` values to understand the undesirable traits that have been detected and how to handle the photo.

    ```jsonon
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
        }
    ]
    ```
