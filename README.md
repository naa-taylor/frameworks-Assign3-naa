# frameworks-Assign3-naa
 Documentation for Taylor'd Occasions Project

Project Overview
Taylor'd Occasions is a web application designed for an event decor company that specializes in creating unforgettable moments for clients. The website provides an elegant and interactive user experience where potential customers can explore services, view event images, and request quotes for services. The project was built using **Next.js** for the frontend and **Strapi** as a headless CMS for backend content management.

Key Features
1. **Homepage with Dynamic Carousel:**
-	The homepage showcases a carousel of images managed via the Strapi CMS.
-	The carousel dynamically fetches data from Strapi, allowing easy updates of images and captions without requiring code changes.
2. **Services Page:**
-	Displays a list of services offered by the company, including wedding decor, birthday setups, and balloon decor.
-	Data is managed dynamically through Strapi’s content collections.
3. **"Get a Quote" Form:**
-	A form allows users to submit their details, including name, email, selected service, and a custom message.
-	Intended to use a serverless function to process form submissions and store the data in Strapi’s `Quotes` collection.

Ideal Functionality
The project was designed with the following intentions:

1. **Serverless Functionality:**
-	To handle form submissions dynamically using a serverless function in Next.js.
-	The function was meant to interact with Strapi's REST API to save form data into the `Quotes` collection.
2. **Asynchronous Operations:**
-	To process form submissions asynchronously, providing users with immediate feedback on success or failure of the submission.
3. **Dynamic Content Handling:**
-	Fetching and displaying images, services, and other content dynamically from Strapi collections.
4. **User Feedback:**
-	Displaying success or error messages based on the result of the serverless function and API communication.
Challenges Encountered
While the website functions correctly in several aspects, the integration of the "Get a Quote" form with Strapi’s `Quotes` collection faced technical challenges:

1. **Authorization Issues:**
-	The Strapi API token configuration caused issues with authentication, resulting in `401 Unauthorized` and `400 Bad Request` errors during form submission.  
2. **Payload Structure:**
-	Ensuring the payload sent to Strapi matched the expected structure was complex, and debugging required additional time.
3. **Debugging Serverless Function:**
-	Managing the flow between the client-side form, serverless function, and Strapi API required extensive debugging, which was not fully resolved within the timeline.
Scope Changes from Lab 1/2
Originally, the project focused on creating a static services page and carousel. The scope shifted to integrating dynamic features like the "Get a Quote" form and serverless functionality. This shift aligned with Assignment 3’s requirements but added significant complexity to the project.

## Maintenance Guidelines
To ensure the continued success of this project, follow these guidelines:

### Content Management
1. **Strapi Collections:**
-	Use the Strapi admin panel to add or update images, services, and carousel content.
-	Ensure that proper permissions are set for any new collections or changes to API access.

2. **Quotes Collection:**
-	Periodically review submissions in the `Quotes` collection via the Strapi admin panel.
-	Verify API token configurations and permissions if any issues arise.

### Debugging and Testing
1. **Serverless Functions:**
-	Use tools like Postman or cURL to test Strapi API endpoints independently.
-	Log serverless function errors to a monitoring service for easier debugging.

2. **Form Submissions:**
-	Validate form inputs thoroughly on both the client and server sides to prevent issues.
-	Log submission data and API responses for troubleshooting.

### Deployment and Updates
1. **Environment Variables:**
-	Securely manage sensitive data like the Strapi API token using environment variables.
-	Regularly update tokens and configuration files.

2. **Testing Before Deployment:**
-	Test the entire application locally and on staging environments before deploying to production.
-	Focus on testing serverless functions and API integrations thoroughly.

### Improvements for Future Iterations
1. **Form Submission Workflow:**
-	Investigate and resolve the `400 Bad Request` and `401 Unauthorized` errors.
-	Ensure that the serverless function correctly communicates with the Strapi API.

2. **Enhanced User Feedback:**
-	Implement loaders or spinners to improve the user experience during asynchronous operations.

3. **Extend Features:**
-	Add email notifications for both users and administrators upon successful form submission.
-	Implement client-side validation to reduce API errors caused by invalid inputs.

4. **Use GraphQL:**
-	Consider switching to GraphQL queries for more efficient and structured data fetching from Strapi.

## Conclusion
Although the integration of form submissions with Strapi’s API remains incomplete, the Taylor'd Occasions project successfully demonstrates the use of a headless CMS with a modern frontend framework. The foundational architecture is robust, and with additional debugging and iterations, the intended functionality can be fully realized.

