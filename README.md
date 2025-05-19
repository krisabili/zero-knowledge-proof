# Zero Knowledge Proof

## Installing

Install Node.js        
npm install react   
npm install node_modules

## Running the Website

To run in development mode, use `npm start`. While developing, the page will automatically reload when you make edits. 

This runs on [http://localhost:3000](http://localhost:3000)

For web debugging you can use `npm test`. Launches the website in interactive mode.

`npm run build` builds the app in the build folder. Puts react in production mode, optimizing the build for the best performance.

## Knowledge-based verification method flow
When a user creates an account to use Hypixel's "services", a quiz verification page is brought up. This quiz is used to determine if the user is 13 years old and over, or 12 years old and below. The quiz has 3 low, 3 medium, and 3 heavy "weighted" questions that do not require rigorous work. These weights are determined by the probability of correct identifying the user's age. Heavier weights means a high probability to correctly identify users over the age of 13. Low weights means a low probability to correctly identify users over the age of 13. Each question is timed to ensure they are answered in a timely manner; this is to prevent cheating via ChatGPT or googling. 

Once the user answers all 9 questions, if they received 75+ points, their account is classified as 13 and up or 12 and below. This classification is saved to the user's device similar to SSH (no implementation in the code at the moment). When a user tries to access Hypixel's services with a classification of 12 and below, they will be restricted from using them. On the contrary, with the classification of 13 and over, users will have the freedom to use them. For false negatives, users can contact Hypixel staff or try to override the classification by using their ID verification or some form of verification method as a fail safe. 

--------------------------------------------------------------------------------------------------------------------

## BELOW IS A MORE DETAILED READ ME THAT I WROTE. 
## THIS IS MORE ROBUST AND PROFESSIONAL
                                                          READ ME
OVERVIEW
The system evaluates users' mastery of information expected from 13-year-old students according to U.S. middle school academic standards. The system uses a brief interactive quiz to identify users as either younger or older than 13 years old for gaming platform access restrictions compliance.

Key Features:
      •	Curriculum-Aligned Content: The system pulls questions from a verified database, which matches the educational benchmarks for U.S. middle school students.
      •	Balanced Question Design: The question set spans three educational categories, which include Civic & Cultural understanding as well as Mathematical Reasoning and Scientific Knowledge.
      •	Randomized Question Sets: The randomized question sets feature prevents users from guessing and ensures quiz integrity is preserved.
      •	CAPTCHA-Inspired Interface: The CAPTCHA-inspired interface increases both unpredictability and user engagement.
      •	Time Limits: The timing constraints minimize mechanical guessing but preserve the fun aspect of the experience.

Use Case Scenario:
      1.	Upon signing up for the game platform, users receive a prompt to take the quiz.
      2.	The system generates a random selection of 9 questions from its database for users.
      3.	Based on the user's score:
          •	Score ≥ 75 points: Access is provided to users who score 75 points or higher as they are considered to be at least 13 years of age.
          •	Score < 75 points: Age restrictions prevent the user from proceeding because they scored less than 75 points.

Question Format & Weighting:
      The quiz measures difficulty level through the number of questions asked and calculates total points based on points assigned per question. 9 questions are assigned in three different weight categories.
      Difficulty Level	Number of Questions	Points per Question	Total points
          •	The total number of questions to be presented to the user is 9 in the following order:
          •	3 low-weight questions at 5 points each ---> Total: 15
          •	3 mid-weight questions at 10 points each ---> Total: 30
          •	3 high-weight questions at 20 points each ---> Total: 60
          •	To pass and be allowed into the game environment, a user must score at least 75 points.

Maximum Score: 105
Passing Score: 75

Example Questions:
      Civic & Cultural Comprehension
          •	What role does the U.S. Constitution serve?
          •	Identify a principal global faith.
      Mathematical Reasoning
          •	How do you calculate the area of a rectangle when its sides measure 3 units and 4 units?
          •	Solve for x: 2x + 5 = 15.
      Scientific Knowledge
          •	What causes the seasons to change?
          •	What is the boiling point of water?

Anti-Guessing Measures
      This system uses various strategies to prevent users from successfully completing the quiz through guessing alone.
          •	The question pool offers a large selection of randomized questions for each session.
          •	The system implements a CAPTCHA-like interface to achieve variation.
          •	Time constraints are used strategically to increase the quiz difficulty level.

Intended Usage
      This system provides a trustworthy and interactive user age verification solution for platforms that wish to avoid the collection of sensitive personal information. The system promotes responsible gaming approaches while maintaining strict adherence to digital     
      content age restrictions.



