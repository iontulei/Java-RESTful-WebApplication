# NoteBridge - Web Application Project

**Module 4, Bachelor of Technical Computer Science, University of Twente**

**Date:** 01-07-2023

## Overview

This project is a web application developed as part of the Technical Computer Science program at the University of Twente. The website, built for a startup company called  [NoteBridge](https://nl.linkedin.com/company/note-bridge), aims to create a vibrant online music community. NoteBridge is dedicated to making music education accessible to everyone by connecting aspiring musicians with experienced teachers. Through this platform, musicians can find personalized and affordable music lessons while also fostering connections and collaborations within the music community.

## Project Description

The website leverages RESTful services written in Java, and follows modern web development practices. The main features of the website include:
- **User and Teacher Management:** Users can register, log in, and find music teachers based on various criteria such as instruments, skills, and availability.
- **Booking System:** A robust system that allows students to book lessons with teachers and manage their bookings.
- **Interactive Map:** A map feature with custom markers that allow users to find music teachers in their area. Clicking on a marker redirects the user to the teacher's profile page.
- **Notifications:** A notification system to keep users informed about their bookings, messages, and other important updates.
- **Security:** Standard security measures are implemented to protect user data and ensure a safe browsing experience.

## My Contribution

In this project, I was responsible for the following key components:

### Backend Development
- **Database Management:** Designed and managed the database schema, ensuring efficient data storage and retrieval.
- **RESTful Services:** Developed the backend services using Jersey (a framework for developing RESTful web services in Java). These services handle all the data operations for the website, such as user authentication, booking management, and lesson handling.

### Security Implementation
- **Input Sanitization:** Implemented input sanitization to protect against XSS (Cross-Site Scripting) and Command Injection attacks.
- **Password Security:** Enhanced security by hashing user passwords with salt and pepper before storing them in the database.
- **Overall Security Measures:** Ensured the application adhered to best practices in web security, minimizing potential vulnerabilities.
For a detailed overview of the API endpoints and their usage, please refer to the [API Documentation](API.md).

### Interactive Map
- **Custom Interactive Markers:** I developed an interactive map that allows you to find teachers in your area. The map can be filtered to display teachers with certain instruments and lesson types. Each teacher is represented by a marker that, when clicked, directs users to the corresponding teacher's profile page, making it easier for users to find and connect with teachers in their area.

## Teammate's Contribution

The frontend of the website, including the design, HTML, CSS, and JavaScript, was fully developed by my teammate, [Alexandru Verhovetchi](https://github.com/Alex-Verh). Alexandru's work ensured that the website not only functions smoothly but also provides a visually appealing and user-friendly experience.

## About NoteBridge

NoteBridge is a music community platform that connects musicians of all levels, providing opportunities for learning, teaching, and collaboration. Our mission is to bridge the gap between musicians, fostering an inclusive environment where everyone can share their passion for music. Whether you're an amateur, intermediate, or professional musician, NoteBridge offers you a platform to grow, connect, and thrive.

For more information, visit [NoteBridge on LinkedIn](https://nl.linkedin.com/company/note-bridge).
