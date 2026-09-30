# API Testing

API testing was performed on the EchoGPT Chat API using Postman to verify authentication, request validation, input handling, and response behavior.

## Test Case Summary

| Test ID | Scenario | Expected Result | Actual Result | Status |
|---|---|---|---|---|
| API-TC-001 | Valid authenticated request | API should process a valid request successfully | API returned `success: true` with generated content | **PASS** |
| API-TC-002 | No authentication | API should reject an unauthenticated request | API returned HTTP `401 Unauthorized` | **PASS** |
| API-TC-003 | Empty `message` | API should reject the empty input or return a clear validation response | API returned `success: true` and generated a response | **PASS** |
| API-TC-004 | Missing `message` field | API should return a clear client-side validation error | API returned HTTP `500` instead of a validation error | **FAIL** |
| API-TC-005 | Unsupported/restricted model | API should reject an unsupported model or return a clear error | API handled the request without an unexpected server failure | **PASS** |
| API-TC-006 | Long message | API should process the input or return a clear input-limit error | API returned `success: true` and generated a response | **PASS** |
| API-TC-007 | Missing `chatId` | API should reject the request if the field is required, or process it if optional | API successfully generated a response | **PASS** |
| API-TC-008 | Missing `messageId` | API should reject the request if the field is required, or process it if optional | API successfully generated a response | **PASS** |
| API-TC-009 | Invalid `chatId` format | API should validate the identifier or process it without an unexpected server failure | API returned `success: true` and generated a response | **PASS** |
| API-TC-010 | Invalid `stream` data type | API should return a validation error for the incorrect data type | Request was blocked by HTTP `429` quota limit before validation could be assessed | **BLOCKED** |

## Test Summary

| Result | Count |
|---|---:|
| Total Test Cases | 10 |
| Passed | 8 |
| Failed | 1 |
| Blocked | 1 |

## Key Finding

**API-TC-004** identified an API validation issue.

When the `message` field was completely omitted from the request body, the API returned **HTTP 500 Internal Server Error** instead of a clear client-side validation response.

The testing also showed that removing `chatId` or `messageId` did not prevent the tested requests from being processed. This indicates that these fields were not required for the specific requests tested.

> **Note:** The results for `chatId` and `messageId` are limited to the tested request and do not establish their behavior for every API endpoint or scenario.

## Testing Limitation

Further validation testing was stopped after the API returned **HTTP 429 Too Many Requests** because the available message quota had been reached.

Therefore, **API-TC-010** could not determine how the API handles an incorrect `stream` data type.

## Tools

- **Postman** — API request execution and response validation
- **EchoGPT Chat API** — System under test
