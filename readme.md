Overview
Event Manager is a Python-based application built with FastAPI, designed to manage user profiles. It features email verification, password management, and social media integration. The project uses PostgreSQL for the database and employs JWT tokens for secure authentication. Automated testing is implemented with Pytest.

Features
User Registration & Authentication:
Provides JWT token-based login with role-based access control for roles like ADMIN and MANAGER.

Email Verification:
Requires users to verify their email for registration, leveraging services like Mailtrap for testing.

Profile Management:
Allows users to update profile details, including nickname, profile picture URL, and social media links.

Password Validation:
Enforces strong password requirements during registration and updates.

Unique Username Validation:
Ensures that all usernames (nicknames) are unique.

Setup Instructions
Prerequisites:
Python 3.10 or higher
PostgreSQL
Docker (for a containerized setup)
Issues Resolved
JWT Token and Pytest Error:

Issue: Login authentication failed for ADMIN and MANAGER roles due to JWT token issues.
Solution: Adjusted JWT token generation and authentication logic for proper handling of user roles. Resolved Pytest errors to ensure smooth testing of authentication and email verification workflows.
Nickname Mismatch in Registration:

Issue: Discrepancy in handling nicknames during registration.
Solution: Fixed the logic to maintain consistency in nickname processing.
Password Validation:

Issue: The application lacked robust password validation.
Solution: Introduced rules for password strength to enhance security.
Unique Username Validation:

Issue: Duplicate usernames (nicknames) were allowed.
Solution: Enforced unique nickname validation during registration.
URL Validation:

Issue: Invalid URLs could be provided in fields like profile_picture_url, linkedin_profile_url, and github_profile_url.
Solution: Implemented URL validation to ensure all input URLs are correctly formatted.
Restricting Unverified Users:

Issue: Users with unverified emails could update profiles, posing security risks.
Solution: Added a restriction to allow profile updates only for users with verified emails.
Outcomes
This assignment provided significant learning experiences in both technical and collaborative aspects of building secure and scalable APIs.

Technical Skills:

Gained hands-on experience with FastAPI, particularly in developing and managing RESTful APIs with authentication and role-based access control.
Strengthened knowledge of OAuth2 with Password Flow and JWT token implementation for secure API communication.
Utilized SQLAlchemy for efficient asynchronous database operations, enhancing CRUD performance.
Applied HATEOAS principles to improve API usability by providing dynamic navigational links.
Challenges Overcome:

Addressed complex issues like restricting unverified email users and managing multiple user roles, requiring careful testing and refinement of business logic.
Improved password validation and ensured data integrity through unique nickname enforcement.
Collaboration:

Emphasized the importance of robust documentation and consistent schema design to facilitate seamless teamwork and communication.
This assignment deepened my understanding of API development, highlighting the importance of balancing security, usability, and maintainability. It also underscored the need for effective automated testing and enhanced exception handling for better error messages. Overall, it was a valuable hands-on experience in addressing real-world challenges while solidifying foundational skills for future API projects.

![Docker Hub  Image](https://github.com/user-attachments/assets/866e5183-2d59-484d-9476-24a611425621)




