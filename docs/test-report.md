# API Testing Report

## 1. Overview

**Project:** REST API Testing Practice  
**Tools:** Postman, Swagger / OpenAPI  
**Test environments:** Public WordPress REST API and Swagger Petstore API

## 2. Executed Checks

| API                | Request                            | Actual Result                                                             | Outcome  |
| ------------------ | ---------------------------------- | ------------------------------------------------------------------------- | -------- |
| WordPress REST API | `GET /wp-json/wp/v2/pages?page=1`  | HTTP 200 OK; pagination headers: `X-WP-Total: 525`, `X-WP-TotalPages: 53` | Observed |
| WordPress REST API | `GET /wp-json/wp/v2/pages?page=2`  | HTTP 200 OK; returned page IDs differ from page 1                         | Observed |
| WordPress REST API | `GET /wp-json/wp/v2/pages?page=54` | HTTP 400 Bad Request; code: `rest_post_invalid_page_number`               | Observed |
| Swagger Petstore   | `GET /api/v3/pet/123`              | HTTP 404 Not Found; response body: `Pet not found`                        | Observed |

## 3. Findings

The request for pet ID `123` returned HTTP 404 with the message `Pet not found`.

This confirms the observed behavior for this particular request. It does not establish that all not-found or invalid-parameter cases behave correctly.

## 4. Planned Further Checks

- Retrieve an existing pet and validate the response structure.
- Compare actual responses with the API specification.
- Check invalid path parameter values.
- Verify response content types and required fields.
- Execute the planned WordPress API scenarios and record their actual results.

## 5. Limitations

- Only observed results are recorded as executed.
- Planned scenarios are not counted as completed tests.
- WordPress API exploration, Swagger Petstore testing, and PostgreSQL/Sakila practice use separate environments.
- No production load or stress testing is claimed.

## 6. Conclusion

The project documents API testing practice, scenario design, and observed response behavior. Further execution and result recording are needed to expand the evidence of testing coverage.
