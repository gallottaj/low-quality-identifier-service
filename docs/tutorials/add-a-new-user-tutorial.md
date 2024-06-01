---
layout: page
---

# Tutorial: Add a new user

In this tutorial, you learn the operations needed to
add a new user.

Expect this tutorial to take about 15 minutes to complete.

## Before you start

Make sure you've completed the [Before you start a tutorial](before-you-start-a-tutorial) topic on the development system you'll use for the tutorial.

## Add a new user

Adding a new user to the service requires that you add (`POST`) the details of a new [`user`](../api/user) resource to the service.

To add a new user:

1. Make sure your local service is running, or start it by using this command, if it's not.

    ```shell
    cd <your-github-workspace>/low-quality-identifier-service/api
    json-server -w low-quality-identifier-service-source.json
    ```

1. Open the Postman app on your desktop.
1. In the Postman app, create a new request with these values:
    * **METHOD**: POST
    * **URL**: `{{base_url}}/users`
    * **Headers**:`Content-Type: application/json`
    * **Request body**:
        You can change the values of each property as you'd like.

        ```js
        [
            {
            "last_name": "Doe",
            "first_name": "John",
            "email": "j.doe@example.com",
            }
        ]
        ```

1. In the Postman app, choose **Send** to make the request.
1. Watch for the response body, which should look something like this. Note that the names should be the same as you used in your **Request body** and the response should include the new user's `id`.

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

After doing this tutorial in Postman, you might like to repeat it in
your favorite programming language. To do this, adapt the values from
the tutorial to the properties and arguments that the language uses to
make REST API calls.
