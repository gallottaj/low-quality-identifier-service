

# Tutorial: Add a new photo

In this tutorial, you learn the operations needed to
add a new photo.

Expect this tutorial to take about 15 minutes to complete.

## Before you start

Make sure you've completed the [Before you start a tutorial](before-you-start-a-tutorial) topic on the development system you'll use for the tutorial.

## Add a new photo

Adding a new photo to the service requires that you add (`POST`) the details of a new [`photo`](../api/photo) resource to the service.

To add a new photo:

1. Make sure your local service is running, or start it by using this command, if it's not.

    ```shell
    cd <your-github-workspace>/low-quality-identifier-service/api
    json-server -w low-quality-identifier-service-source.json
    ```

1. Open the Postman app on your desktop.
1. In the Postman app, create a new request with these values:

    * **Method**: POST
    * **Authorization**: Basic Auth (`username`/`password`)
    * **URL**: `{base_url}/photos`
    * **Headers**:`Content-Type: application/json`
    * **Request body**:
        
    You can change the values of each property as you'd like.

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

1. In the Postman app, choose **Send** to make the request.
1. Watch for the response body, which should look something like this. Note that the names should be the same as you used in your **Request body** and the response should include the new photo's `id`.

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

After doing this tutorial in Postman, you might like to repeat it in
your favorite programming language. To do this, adapt the values from
the tutorial to the properties and arguments that the language uses to
make REST API calls.