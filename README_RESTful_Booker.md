# RESTful Booker – API Testing

A Postman collection for practicing and validating REST API operations on the **RESTful Booker** booking service. The collection covers retrieving booking IDs and booking details, creating bookings, updating booking information, partially updating records, and deleting bookings.

## Project Overview

This project uses Postman to send HTTP requests to the RESTful Booker API and inspect the responses. It demonstrates the main CRUD operations through a single organized collection.

**Base URL:** `https://restful-booker.herokuapp.com`

## Tools & Technologies

- **Postman** – API request creation and execution
- **REST API** – HTTP-based client/server communication
- **JSON** – request payload format
- **HTTP methods** – GET, POST, PUT, PATCH, DELETE
- **Authentication** – Bearer Token and Basic Authentication (as configured in the collection)

## API Coverage

| # | Request | Method | Endpoint |
|---|---|---|---|
| 1 | `GetBookingIds` | `GET` | `/booking` or `/booking/{bookingId}` |
| 2 | `GetBooking` | `GET` | `/booking` or `/booking/{bookingId}` |
| 3 | `CreateBooking` | `POST` | `/booking` or `/booking/{bookingId}` |
| 4 | `UpdateBooking` | `PUT` | `/booking` or `/booking/{bookingId}` |
| 5 | `PartialUpdateBooking` | `PATCH` | `/booking` or `/booking/{bookingId}` |
| 6 | `DeleteBooking` | `DELETE` | `/booking` or `/booking/{bookingId}` |

### What Each Request Covers

- **GetBookingIds:** Retrieves the available booking IDs.
- **GetBooking:** Retrieves booking information using a booking ID. The collection configures Bearer Token authentication for this request.
- **CreateBooking:** Creates a new booking using a JSON request body containing guest details, price, deposit status, booking dates, and additional needs.
- **UpdateBooking:** Updates booking information for a specified booking ID using `PUT`.
- **PartialUpdateBooking:** Updates selected booking fields using `PATCH`. The collection configures Basic Authentication.
- **DeleteBooking:** Deletes a booking using its ID. The collection configures Basic Authentication.

## How to Import and Run

1. Download or clone this repository.
2. Open **Postman**.
3. Click **Import** and select `RESTFULL BOOKER.postman_collection.json`.
4. Open the imported **RESTFULL BOOKER** collection.
5. Check the base URL, booking IDs, request payloads, and authentication settings.
6. For Basic Authentication, provide the required password through the Postman variable configured for the collection.
7. Send requests individually and review the status code and response body.

## Repository Structure

```text
RESTful-Booker-API-Testing/
├── README.md
└── RESTFULL BOOKER.postman_collection.json
```

## Notes

- Booking IDs used in sample requests are examples. Replace them with valid IDs when required.
- The collection contains request definitions but no saved response examples; execution results depend on the API service and test data.
- This README describes the supplied Postman collection and does not claim that all requests have been executed or passed.

## Security

Before publishing the collection publicly, review it for credentials, tokens, personal data, and environment-specific values. Keep passwords and tokens in Postman environment variables or the Postman Vault; never commit real secrets to GitHub. Rotate any credential that has been exposed.

---

**Project:** RESTful Booker – API Testing  
**Collection Format:** Postman Collection v2.1
