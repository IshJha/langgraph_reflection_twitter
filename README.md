**LangGraph Twitter Enhancement Bot**
This project is a Twitter enhancement bot that utilizes LangChain and LangGraph to improve and critique Twitter posts. 
The bot operates by generating an initial tweet and then reflecting on it to provide recommendations or revisions for better engagement and virality.

**Features**
Tweet Generation: Automatically generates Twitter posts based on user input.
Reflection and Critique: Provides detailed feedback on generated tweets, including style, length, and virality recommendations.
LangGraph Integration: Uses a graph-based approach to determine the flow of operations between tweet generation and reflection.

**Requirements**
Python 3.x
langchain_core
langgraph
langchain_google_genai
dotenv
**Setup**
Clone the repository:
git clone https://github.com/IshJha/langgraph_reflexion_twitter.git
cd langgraph-twitter-bot
Install the required Python packages:

If using Pipfile:
pipenv install

**Set up environment variables:**
Create a .env file in the root directory and add your Google API key:
GOOGLE_API_KEY=<your-api-key>

Run the application:
python main.py
Project Structure
main.py: The entry point of the application. It sets up the message graph and invokes the tweet generation and reflection processes.
chains.py: Contains the logic for generating and reflecting on tweets using LangChain and Google Generative AI.
**Flow of the Project**
Tweet Generation:

The user provides an initial tweet.
The generate_chain is invoked to create an enhanced version of the tweet.
Reflection and Critique:

The reflect_chain is invoked to critique the generated tweet.
If the reflection conditions are met, the bot will generate another version of the tweet based on the critique.
Conditional Logic:

The project uses LangGraph to handle the flow between tweet generation and reflection.
If more than six messages are generated, the process ends; otherwise, the reflection process continues.
