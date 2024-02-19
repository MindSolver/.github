# MindSolver 👋

## Project Overview
This project aims to assist users in forming a consistent habit through diary writing, thereby having a positive impact on improving depression symptoms. Users experience small achievements through regular diary writing, contributing to emotional stability.

## Project Setup

<img width="649" alt="Untitled (14)" src="https://github.com/MindSolver/.github/assets/113033780/6fff6b8a-9ef1-4c88-8713-a5a4bc55977f">

South Korea has the highest prevalence rate of depression among OECD countries, a situation that has worsened due to COVID-19. The number of people suffering from depression has increased by about 30% over the past five years, exceeding 1 million. However, the social perception of depression in South Korea is poor, and only 30% of those affected actually receive treatment, resulting in a treatment rate of merely 11%. If depression is not adequately treated, it can make normal social life in schools or workplaces difficult, indicating that it is not just an individual issue but a significant problem that South Korea needs to address.

We have set our goal to address the 3rd United Nations Sustainable Development Goal, 'GOOD HEALTH AND WELL-BEING', by aiming to alleviate the early symptoms of depression. Depression, when diagnosed early, can have an 80% cure rate; however, if not addressed, it can significantly impact an individual's health. According to statistics from the Health Insurance Review & Assessment Service in South Korea, the highest prevalence and growth rates of depression are among teenagers and young adults in their 20s. Considering the accessibility and convenience of smartphones for teenagers and young adults, we have targeted students and young people in their teens and 20s in South Korea.

## Implementation
<img width="400" alt="스크린샷 2024-02-19 오후 9 02 25" src="https://github.com/MindSolver/.github/assets/92268965/d6e81330-b0fb-41e6-9dd0-933e0ae9c262">

Our team selected Flutter for the frontend of our solution. Flutter is used for cross-platform mobile app development, facilitating UI design and interaction with Firebase and backend servers. Firebase serves to store user account information and data. The backend server is utilized for pre-processing and post-processing in the GPT API calling process and uses Server-Side Events (SSE) to deliver real-time responses to the frontend.

The backend, hosted on AWS EC2, manages requests and user data to produce personalized diary entries via a single API endpoint. It employs FastAPI for its efficiency and Python for integrating with GPT-4, processing inputs such as job, age, and daily experiences, ensuring scalable and responsive diary generation.

### Frontend
For the frontend, we chose Google's Flutter. As a cross-platform app development framework, Flutter uses the Dart language for UI design, making development highly intuitive and straightforward. Additionally, the Flutter package ecosystem is very active, making it easy to find the desired functionality and facilitating development.

### Backend
For the backend, we actively utilized Google's Firebase. For creating small-scale apps, we opted for a serverless approach instead of implementing a separate backend. This allows for quick adjustments without the need for backend communication, easily managed through the Firebase console.

### Machine Learning
In the process of making diaries from users' memo, I utilized the GPT-4 Turbo API. During this process, I also experimented with Google's language model, Gemini, and found that Gemini also showed satisfactory performance in diary generation from the perspective of 'diary creation'. However, from the user's perspective, for the implementation of asynchronous processing and customized diary creation for each user, using the GPT API proved to be more effective. Therefore, I ultimately chose to use the GPT API.

## Role
| ![채홍무](https://github.com/Hong-Mu.png) | ![남영진](https://github.com/NamisMe.png)   | ![전효정](https://github.com/junnie082.png) | ![최승훈](https://github.com/cshooon.png)  |
| :--------------------------------------------------------------: | :--------------------------------------------------------------: | :--------------------------------------------------------------: | :--------------------------------------------------------------: |
|            [👑채홍무👑](https://github.com/Hong-Mu)             |            [남영진](https://github.com/NamisMe)             |            [전효정](https://github.com/junnie082)             |            [최승훈](https://github.com/cshooon)             |
|                            Flutter & Firebase                             |                            FastAPI & GPT API                             |                            Flutter & Firebase                             |                            FastAPI & GPT API                             |
