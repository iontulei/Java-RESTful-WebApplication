# NoteBridge API Documentation

## General Information
- **Methods:** `POST` and `PUT` consume a `JSON` object with all the details.

---

## Booking

- **GET /booking**  
  Retrieves all bookings.

- **POST /booking**  
  Inserts a new `Booking` along with `Payment` and `Notification`.

- **GET /booking/count**  
  Retrieves the total number of bookings.

- **GET /booking/{id}**  
  Retrieves a booking by its ID.

- **GET /booking/student/{id}**  
  Retrieves bookings by student ID.

- **GET /booking/lesson/{id}**  
  Retrieves bookings by lesson ID.

- **GET /booking/schedule/{id}**  
  Retrieves bookings by schedule ID.

- **GET /booking/count/{id}**  
  Retrieves the number of past bookings for a given student ID.

- **POST /booking/finished/{id}**  
  Marks the booking with the given ID as finished.

- **POST /booking/canceled/{id}**  
  Marks the booking with the given ID as canceled.

- **DELETE /booking/{id}**  
  Deletes a booking by its ID.

---

## Instrument

- **GET /instruments**  
  Retrieves all instruments.

- **GET /instruments/{id}**  
  Retrieves an instrument by its ID.

- **GET /instruments/count**  
  Retrieves the total count of instruments.

- **GET /instruments/student/{id}**  
  Retrieves all instruments learned by a student with the given ID.

- **POST /instruments**  
  Adds a new instrument.

- **PUT /instruments**  
  Updates an instrument.

- **DELETE /instruments/{id}**  
  Deletes an instrument by its ID.

---

## Lesson

- **GET /lessons**  
  Retrieves all lessons.

- **GET /lessons/{id}**  
  Retrieves a lesson by its ID.

- **GET /lessons/count**  
  Retrieves the total number of lessons.

- **GET /lessons/student/{id}**  
  Retrieves all lessons of the student.

- **GET /lessons/student/count/{id}**  
  Retrieves the lesson count for a student.

- **GET /lessons/teacher/{id}**  
  Retrieves all lessons of the teacher.

- **PUT /lessons**  
  Updates a lesson with a new lesson object.

- **POST /lessons**  
  Adds a lesson, consumes JSON.

- **POST /lessons**  
  Adds a lesson, consumes type application form.
  - **Parameters:**
    - `lessonPrice`
    - `lessonInstrument`
    - `lessonLevel`
    - `lessonDescription`
    - `lessonTitle`

- **DELETE /lessons/{id}**  
  Deletes a lesson by its ID.

- **GET /lessons/search**  
  Searches for lessons by filtering the following parameters:
  - **Query Parameters:**
    - `lessonOffset`
    - `lessonInstrumentId`
    - `lessonSkillId`
    - `lessonRating`
    - `lessonLocation`
    - `lessonAvailability`
    - `lessonType`

---

## Messages

- **GET /message/participant/{id}**  
  Retrieves all messages where the sender ID or the receiver ID is `{id}`.

- **POST /message**  
  Adds a new message.

---

## Notification

- **POST /notification**  
  Adds a new notification.

- **GET /notification/{id}**  
  Retrieves a notification by its ID.

- **GET /notification/user/id**  
  Retrieves notifications for a user by their ID.

- **GET /notification/count**  
  Retrieves the total number of notifications.

- **GET /notification/confirm/{id}**  
  Confirms a notification by its ID.

- **DELETE /notification/{id}**  
  Deletes a notification by its ID.

---

## Payment

- Payments are added along with the booking.

- **PUT /payment/{id}**  
  Updates payment status to "paid" with the current timestamp.

---

## Review

- **GET /reviews**  
  Retrieves all reviews.

- **GET /reviews/teacher/{id}**  
  Retrieves all reviews for a teacher by their ID.

- **GET /reviews/count/{id}**  
  Retrieves the count of reviews for a teacher by their ID.

- **GET /reviews/has-review-from/{lessonId}/studentId**  
  Retrieves the count of reviews written by a student for a given lesson.

- **POST /reviews**  
  Adds a new review, consumes type application form.
  - **Parameters:**
    - `addMark`
    - `reviewComment`
    - `teacherId`
    - `studentId`
    - `lessonId`

- **DELETE /reviews/{lessonId}/{studentId}**  
  Deletes a review from a student for the given lesson.

---

## Skill

- **GET /skill**  
  Retrieves all skills.

- **GET /skill/{id}**  
  Retrieves a skill by its ID.

---

## Teacher Instruments

- **GET /teacher-instruments**  
  Retrieves all instruments of the teacher.

- **GET /teacher-instruments/{id}**  
  Retrieves all instruments of the teacher by their teacher ID.

- **GET /teacher-instruments/instrument/{id}**  
  Retrieves all instruments of the teacher by their instrument ID.

---

## Teacher Schedules
- **Note:** Schedule = Time slot

- **GET /schedule**  
  Retrieves all schedules.

- **GET /schedule/id**  
  Retrieves a schedule by its ID.

- **GET /schedule/count**  
  Retrieves the total schedule count.

- **GET /schedule/teacher/{id}**  
  Retrieves schedules by teacher ID.

- **GET /schedule/teacher/free/{id}**  
  Retrieves all free schedules by teacher ID.

- **POST /schedule**  
  Adds a schedule for a teacher.

- **DELETE /schedule/{id}**  
  Deletes a schedule by its ID.

---

## Teacher

- **GET /teachers**  
  Retrieves all teachers.

- **GET /teachers/{id}**  
  Retrieves a teacher by their ID.

- **GET /teachers/count**  
  Retrieves the total count of teachers.

- **GET /teachers/search**  
  Searches for teachers based on the following parameters:
  - **Query Parameters:**
    - `instrumentId`
    - `skillId`
    - `rating`
    - `online` (true/false)
    - `date` (format: YYYY-MM-DD)
  - **Example:** `/teachers/search?instrument-id=3&online=true&date=2023-01-29`

- **POST /teachers**  
  Adds a new teacher.

- **PUT /teachers**  
  Updates a teacher, consumes type multipart form data.
  - **Parameters:**
    - `editFullname`
    - `is_online`
    - `editCountry`
    - `editCity`
    - `editExperience`
    - `editZip`
    - `instrument`

- **DELETE /teachers/{id}**  
  Deletes a teacher by their ID.

---

## User

- **GET /users**  
  Retrieves all users.

- **GET /users/{id}**  
  Retrieves a user by their ID.

- **GET /users/count**  
  Retrieves the total count of users (students).

- **GET /users/count/city**  
  Retrieves the count of all unique cities.

- **GET /users/current**  
  Retrieves the current logged-in user.

- **GET /users/profile/{id}**  
  Retrieves profile details of a user by their ID.

- **GET /users/exists/{email}**  
  Checks if a user exists by the given email.

- **POST /users**  
  Creates a user, consumes JSON.

- **PUT /users**  
  Updates a user, consumes type multipart form data.
  - **Parameters:**
    - `editFullName`
    - `is_online`
    - `editCountry`
    - `editCity`
    - `editProfileImage`

- **PUT /users/description**  
  Updates the description of a user.

- **DELETE /users/{id}**  
  Deletes a user by their ID.

---

## Zip Code Coordinates

- **GET /zipcode-coordinates**  
  Retrieves all zip code coordinates.

- **GET /zipcode-coordinates/{zipcode}**  
  Retrieves coordinates by zip code.
