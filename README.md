## Endpoint
### `GET /`

  - **Description:** Retrieve tasks
  - **URL:** [https://nodemongo-1.onrender.com/tasks/](https://nodemongo-1.onrender.com/tasks/)
  - **Response:**
    ```json
    {
      "status": 200,
      "data": [
          {
              "_id": "66d0e9810608edfbc37fc924",
              "title": "wqrrte",
              "description": "dcxcz",
              "isCompleted": false,
              "updatedAt": "2024-09-05T10:06:05.031Z"
          },
          {
              "_id": "66d98c8d699230fe3f629294",
              "title": "ХПІ",
              "description": "ХYZ",
              "isCompleted": false,
              "createdAt": "2024-09-05T10:48:45.991Z",
              "updatedAt": "2024-09-08T16:35:37.549Z",
              "__v": 0
          }
      ]
    }
    ```
### `GET /:id`

  - **Description:** Restrieve task by id
  - **URL:** [https://nodemongo-1.onrender.com/tasks/:id](https://nodemongo-1.onrender.com/tasks/:id) (use id from db)
  - **Response:**
     ```json
     {
      "status": 200,
      "data": {
          "_id": "66d98c8d699230fe3f629294",
          "title": "ХПІ",
          "description": "ХYZ",
          "isCompleted": false,
          "createdAt": "2024-09-05T10:48:45.991Z",
          "updatedAt": "2024-09-08T16:35:37.549Z",
          "__v": 0
      }
    }
    ```
### `POST /`

  - **Description:** Add new task
  - **URL:** [https://nodemongo-1.onrender.com/tasks/](https://nodemongo-1.onrender.com/tasks/)
  - **Request body:**
    ```json
    {
      "title":"Wash car",
      "description":"With all your wish",
      "isCompleted":"false"
    }
    ```
  - **Response:**
     ```json
     {
      "status": 201,
      "message": "Task successfully created",
      "data": {
          "title": "Wash car",
          "description": "With all your wish",
          "isCompleted": false,
          "_id": "66ddebeef2448906717415d0",
          "createdAt": "2024-09-08T18:24:46.821Z",
          "updatedAt": "2024-09-08T18:24:46.821Z",
          "__v": 0
      }
    }
    ```
### `PUT /`

  - **Description:** Change task by id
  - **URL:** [https://nodemongo-1.onrender.com/tasks/:id](https://nodemongo-1.onrender.com/tasks/:id) (use id from db)
  - **Request body:**
    ```json
    {
      "title":"Wash car",
      "description":"You can do it in less then 30 min",
      "isCompleted":"true"
    }
    ```
  - **Response:**
     ```json
     {
      "status": 200,
      "message": "Task successfully updated",
      "data": {
          "_id": "66ddebeef2448906717415d0",
          "title": "Wash car",
          "description": "You can do it in less then 30 min",
          "isCompleted": true,
          "createdAt": "2024-09-08T18:24:46.821Z",
          "updatedAt": "2024-09-08T18:26:04.854Z",
          "__v": 0
      }
    }
    ```
### `DELETE /`
  - **Description:** Delete task by id
  - **URL:** [https://nodemongo-1.onrender.com/tasks/:id](https://nodemongo-1.onrender.com/tasks/:id) (use id from db)
  - **Response:**
     ```json
     {
    "status": 204
    }
    ```
