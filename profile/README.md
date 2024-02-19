# MindSolver 👋

## Project Overview
This project aims to assist users in forming a consistent habit through diary writing, thereby having a positive impact on improving depression symptoms. Users experience small achievements through regular diary writing, contributing to emotional stability.

## Project Setup

<img width="649" alt="Untitled (14)" src="https://github.com/MindSolver/.github/assets/113033780/6fff6b8a-9ef1-4c88-8713-a5a4bc55977f">

South Korea has the highest prevalence rate of depression among OECD countries, a situation that has worsened due to COVID-19. The number of people suffering from depression has increased by about 30% over the past five years, exceeding 1 million. However, the social perception of depression in South Korea is poor, and only 30% of those affected actually receive treatment, resulting in a treatment rate of merely 11%. If depression is not adequately treated, it can make normal social life in schools or workplaces difficult, indicating that it is not just an individual issue but a significant problem that South Korea needs to address.

We have set our goal to address the 3rd United Nations Sustainable Development Goal, 'GOOD HEALTH AND WELL-BEING', by aiming to alleviate the early symptoms of depression. Depression, when diagnosed early, can have an 80% cure rate; however, if not addressed, it can significantly impact an individual's health. According to statistics from the Health Insurance Review & Assessment Service in South Korea, the highest prevalence and growth rates of depression are among teenagers and young adults in their 20s. Considering the accessibility and convenience of smartphones for teenagers and young adults, we have targeted students and young people in their teens and 20s in South Korea.

## Implementation

Our team selected Flutter for the frontend of our solution. Flutter is used for cross-platform mobile app development, facilitating UI design and interaction with Firebase and backend servers. Firebase serves to store user account information and data. The backend server is utilized for pre-processing and post-processing in the GPT API calling process and uses Server-Side Events (SSE) to deliver real-time responses to the frontend.

The backend, hosted on AWS EC2, manages requests and user data to produce personalized diary entries via a single API endpoint. It employs FastAPI for its efficiency and Python for integrating with GPT-4, processing inputs such as job, age, and daily experiences, ensuring scalable and responsive diary generation.

### Frontend
For the frontend, we chose Google's Flutter. As a cross-platform app development framework, Flutter uses the Dart language for UI design, making development highly intuitive and straightforward. Additionally, the Flutter package ecosystem is very active, making it easy to find the desired functionality and facilitating development.

### Backend
For the backend, we actively utilized Google's Firebase. For creating small-scale apps, we opted for a serverless approach instead of implementing a separate backend. This allows for quick adjustments without the need for backend communication, easily managed through the Firebase console.

### Machine Learning
In the process of making diaries from users' memo, I utilized the GPT-4 Turbo API. During this process, I also experimented with Google's language model, Gemini, and found that Gemini also showed satisfactory performance in diary generation from the perspective of 'diary creation'. However, from the user's perspective, for the implementation of asynchronous processing and customized diary creation for each user, using the GPT API proved to be more effective. Therefore, I ultimately chose to use the GPT API.

## Feedback / Testing / Iteration

We received feedback from college students, who have experienced depressive symptoms, after using the application for about a week. One issue raised was the occasional lack of accuracy in diary entries, prompting us to upgrade the model from GPT-3.5 to GPT-4 for improved precision. Additionally, users expressed the need for visual statistical data on their written diaries, leading us to implement a statistics feature. A significant concern was the inability of the app to guide users towards professional help for appropriate treatment, which we addressed by providing connecting information about professional institutions.

Beyond the basic information received from the initial user input [age, gender, occupation], we attempted to create diaries by storing detailed information about the user, accumulated through their notes, in a database (DB) and setting a persona based on the user's information at the time of diary creation. We extracted embeddings from information (about their favorite foods, celebrities, and recent events, etc.). By storing this information in a Vector DB, we aimed to write more personalized diaries in detail. However, due to technical difficulties in managing a Vector DB for each user, we opted not to use the method of extracting embeddings to store in the vector DB. Instead, we used a method where we only take daily notes from the user and create a diary based on the events of their day.

## Success and Completion of Solution

We designed our solution, Mindsolver, to encourage regular emotional journaling and reflection, leveraging the convenience and accessibility of mobile technology.

Mindsolver was developed to facilitate the habit of journaling, offering features that ease the process of diary writing and encourage consistent engagement. Key features like notification services for reminders, diary auto-completion, and statistical feedback were implemented to enhance user experience and engagement.

To validate our solution's effectiveness, we utilized Google Forms to survey approximately 42 real users, targeting students in their teens and twenties facing various challenges. The survey aimed to measure the impact of Mindsolver on users' mental health through their satisfaction and the utility of its features.

From the survey, we collected the following quantifiable data:

Overall satisfaction with Mindsolver: 4.12 out of 5
Helpfulness of notification services for regular emotional recording: 4.22 out of 5
Assistance of diary auto-completion feature in diary writing: 4.33 out of 5
Contribution of diary writing through Mindsolver to achieving a sense of accomplishment: 4.29 out of 5
Usefulness of weekly/monthly statistics for reflection: 4.25 out of 5

The primary tool used to understand Mindsolver's impact was a detailed user survey conducted via Google Forms. This allowed us to gather direct feedback on the app's features and their effectiveness in enhancing users' mental health. 

## Scalability / Next Steps

MindSolver could partner with professional medical staff in the future to be used as a tool to check a patient's depression or mental state, or to be used in a practical professional healthcare system by further development.

In addition to being able to check the patient's condition recorded every day, medical staff can use the help of artificial intelligence to accurately and quickly analyze the patient's condition or refer to it as important confirmation data.

Through the app, users' conditions can be checked and analyzed, and communication with medical staff can be made easier.
Patients can be managed more efficiently from the perspective of medical staff by reducing unnecessary communication, such as skipping explaining their condition one by one.

Medical staff can communicate with patients through the app without having to meet face-to-face every time. Patients' mood and emotional changes, and the degree of depression can be checked and feedback or advice can be given through the app.

Patients will be able to get a prescription from a medical staff without going to the hospital in person. You don't have to make a meeting appointment with the medical staff and wait for your turn to come. Based on the basic analysis of artificial intelligence, you will be able to communicate non-face-to-face with medical staff and further improve the situation.

By integrating our solution with mobile applications and wearable devices, users can conveniently access the solution anytime and anywhere. With the mobile app, users can write diaries, and with wearable devices, they can record biometric information such as step count and heart rate, allowing them to easily include additional information with their diaries for comprehensive management. This enhancement in user convenience is expected to attract more users to the solution.

Currently, our solution provides simple statistics based on the number of diary entries. However, by applying recommendation algorithms using the big data accumulated from actual users, we can offer personalized services to them. For example, by analyzing users' diary contents and health information, we can recommend appropriate challenges based on their health status or emotional changes. Through this approach, users will be able to receive more effective assistance.
