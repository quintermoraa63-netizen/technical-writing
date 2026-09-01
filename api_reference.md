# API Reference: Create a Task

## HTTP Method and Endpoint

**Method:** POST

**Endpoint:** `/api/v1/projects/{projectId}/tasks`

## Description

This endpoint allows an authenticated user to create a new task in a project management application. Each task requires a title, an assignee, a due date, and a priority. The description is optional.

## Path Parameter

| Name      | Type   | Required | Description                                                  |
| --------- | ------ | -------- | ------------------------------------------------------------ |
| projectId | string | Yes      | The unique ID of the project where the task will be created. |

## Request Body Parameters

| Name        | Type   | Required | Description                                                         |
| ----------- | ------ | -------- | ------------------------------------------------------------------- |
| title       | string | Yes      | The name of the task.                                               |
| description | string | No       | Additional information about the task.                              |
| assigneeId  | string | Yes      | The unique ID of the user assigned to the task.                     |
| dueDate     | string | Yes      | The date when the task is due, using YYYY-MM-DD format.             |
| priority    | string | Yes      | The priority of the task. Accepted values are low, medium, or high. |

## Request Headers

| Header        | Required | Description                                        |
| ------------- | -------- | -------------------------------------------------- |
| Authorization | Yes      | A Bearer token used to authenticate the user.      |
| Content-Type  | Yes      | Specifies that the request body is in JSON format. |

## Example Request

```http
POST /api/v1/projects/proj_1024/tasks
Authorization: Bearer your-access-token
Content-Type: application/json
```

## Example Request Body

```json
{
  "title": "Prepare project presentation",
  "description": "Create and review the final presentation slides.",
  "assigneeId": "usr_2048",
  "dueDate": "2026-09-15",
  "priority": "high"
}
```

## Response Codes

| Status Code               | Description                                                        |
| ------------------------- | ------------------------------------------------------------------ |
| 201 Created               | The task was successfully created.                                 |
| 400 Bad Request           | The request contains invalid or missing information.               |
| 401 Unauthorized          | Authentication is missing or the access token is invalid.          |
| 403 Forbidden             | The user does not have permission to create a task in the project. |
| 404 Not Found             | The specified project or assignee could not be found.              |
| 409 Conflict              | The task conflicts with an existing resource or project rule.      |
| 422 Unprocessable Entity  | The request is valid JSON, but one or more values fail validation. |
| 500 Internal Server Error | An unexpected server error occurred.                               |

## Successful Response

**Status:** 201 Created

```json
{
  "id": "task_7832",
  "projectId": "proj_1024",
  "title": "Prepare project presentation",
  "description": "Create and review the final presentation slides.",
  "assigneeId": "usr_2048",
  "dueDate": "2026-09-15",
  "priority": "high",
  "status": "pending",
  "createdAt": "2026-09-01T18:30:00Z"
}

