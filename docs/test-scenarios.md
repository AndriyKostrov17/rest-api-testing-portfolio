# API Test Scenarios

## Objective

Define positive, negative, and parameter-validation scenarios for REST API testing practice.

## 1. WordPress REST API

| **ID** | **Scenario** | **Expected Result** | **Status** |
| ------ | ----------------------------------------- | --------------------------------------------------------------------- | ---------- |
| WP-01 | Retrieve published posts | HTTP 200 and a JSON response | Planned |
| WP-02 | Retrieve pages | HTTP 200 and a JSON response | Executed: HTTP 200 received |
| WP-03 | Retrieve pages using pagination parameters | Page 1 and page 2 return different page records; pagination headers provide total items and pages | Executed: HTTP 200 received for pages 1 and 2 |
| WP-04 | Request a page beyond the available pagination range | API returns HTTP 400 with error code `rest_post_invalid_page_number` | Executed: HTTP 400 received for page 54; 53 pages available |

## 2. Swagger Petstore API

Endpoint: `GET /api/v3/pet/{petId}`

| ID | Scenario | Expected Result | Status |
|---|---|---|---|
| PET-01 | Retrieve an existing pet | HTTP 200 and pet data in JSON | Planned |
| PET-02 | Retrieve a non-existent pet | HTTP 404 Not Found | Executed: 404 received for pet ID 123 |
| PET-03 | Use an invalid pet ID format | API handles the invalid parameter according to its specification | Planned |
| PET-04 | Check the response body for a missing pet | Response contains an appropriate not-found message | Executed: `Pet not found` |

## Execution Notes

Scenarios marked **Planned** have not been confirmed as executed. Actual results are recorded only for requests that were performed and whose responses were observed.

## Scope

This document covers learning exercises using the public WordPress REST API and Swagger Petstore API. The two APIs are separate test environments.
