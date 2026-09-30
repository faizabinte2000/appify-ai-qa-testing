
# API-BUG-001 — Missing `message` Field Returns HTTP 500

| Field | Details |
|---|---|
| **Bug ID** | API-BUG-001 |
| **Severity** | Major |
| **Priority** | Medium |
| **Component** | Chat API |
| **Type** | API Validation / Error Handling |
| **Test Case** | API-TC-004 |

## Description

The Chat API returns **HTTP 500 Internal Server Error** when the `message` field is completely omitted from the request body.

The request is malformed because the expected input field is missing, but the API responds with a server-side error instead of a clear client-side validation response.

## Steps to Reproduce

1. Authenticate with a valid account.
2. Send a valid Chat API request.
3. Remove the `message` field from the JSON request body.
4. Send the request.
5. Observe the HTTP response.

## Expected Result

The API should reject the malformed request with an appropriate **4xx client error**, such as `400 Bad Request`, and provide a clear validation message indicating that `message` is required.

## Actual Result

The API returned:

```text
HTTP 500 Internal Server Error
