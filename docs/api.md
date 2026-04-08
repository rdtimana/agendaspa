# REST API Documentation

## Authentication
- **Endpoint:** `/api/auth`
- **Method:** `POST`
- **Description:** Authenticate users and retrieve a token.
  - **Request Body:**
    - `username`: string - the username of the user.
    - `password`: string - the password of the user.
  - **Response:**
    - `200 OK`
      - `token`: string - JWT token for subsequent requests.

## Appointments
- **Endpoint:** `/api/appointments`
- **Method:** `GET`
- **Description:** Retrieve a list of appointments.
  - **Response:**
    - `200 OK`
      - `appointments`: array of appointment objects.

### Create an Appointment
- **Endpoint:** `/api/appointments`
- **Method:** `POST`
- **Description:** Create a new appointment.
  - **Request Body:**
    - `date`: string - the date of the appointment.
    - `time`: string - the time of the appointment.
    - `serviceId`: string - the ID of the service.
  - **Response:**
    - `201 Created`
      - `appointment`: appointment object.

## Services
- **Endpoint:** `/api/services`
- **Method:** `GET`
- **Description:** Retrieve a list of available services.
  - **Response:**
    - `200 OK`
      - `services`: array of service objects.