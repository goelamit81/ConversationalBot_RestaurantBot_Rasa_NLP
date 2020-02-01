# ConversationalBot_RestaurantBot_Rasa_NLP

#### Problem Statement

An Indian startup named 'Foodie' wants to build a conversational bot (chatbot) which can help users discover restaurants across several Indian cities. You have been hired as the lead data scientist for creating this product.

 

The main purpose of the bot is to help users discover restaurants quickly and efficiently and to provide a good restaurant discovery experience.


#### Goals of this Project

In this project, you will build a chatbot for ‘Foodie’ and then deploy it on Slack. The folder with starter codes has already been shared with you in session-1. You need to accomplish the following in the project:

- NLU training: You can use rasa-nlu-trainer to create more training examples for entities and intents. Try using regex features and synonyms for extracting entities.

- Build actions for the bot. Read through the Zomato API documentation to extract the features such as the average price for two people and restaurant’s user rating. You also need to build an ‘action’ for sending emails from Python.

- Creating more stories: Use train_online.py file to create more stories. Refer to the sample conversational stories provided above.  Your bot will be evaluated on something similar to the test stories shared.

- Deployment (Optional): Deploy the model on Slack. You can create a new workspace or deploy it on an existing workspace (if you already use Slack).
