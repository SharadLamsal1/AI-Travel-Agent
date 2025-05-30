# AI-Travel-Agent

## RAG Agent Based Chatbot to ask queries on trekking destinations and make bookings.

#### Features:
1) QA on information about trekking destinations in the dataset, sample was created consisting of destinations like Langtang, Ama Yangri, ABC, Shey Phoksundo, etc.
2) Conversational booking. User can express intention to make a booking with the chatbot, and it will ask for necessary inputs and make the booking.

**Example prompts**: "Can you tell me about Ama Yangri Trek?", "Can you provide me an itinerary for Shey Phoksundo Trek?", "What is the best time to do this trek?", "Help me make a booking"

The chatbot uses an agent that has two tools at its disposal.
1) **RAG tool** -> to answer queries on trekking destinations
2) **Booking tool** -> to make bookings.

Based on the user query, the chatbot invokes one of these two tools. 

If the rag tool is invoked, it makes a vector search in the chromadb database and returns the answer. If the booking tool is invoked, the chatbot asks for name, destination and date in a humanly manner within the conversation. Once it gets all the details, the booking tool executes a sql query to the postgresql database and booking is confirmed. 

Bookings can be viewed in the bookings section of the web app.

The following tools have been used in the application:

**LLMs**  - GPT 4o mini via AzureOpenAI as the main model, Gemini 1.5 flash for resolving query with chat history.

**Embeddings** - "text-embedding-3-small" via AzureOpenAI Embeddings

**Databases** - ChromaDB for vector database, PostgreSQL to store booking related information.

**Major Libraries** - Langchain for chatbot, Streamlit for UI

**Screenshots**

![image](https://github.com/user-attachments/assets/6d347d91-b44f-451a-96ae-fb12c453f71c)

![image](https://github.com/user-attachments/assets/474d9007-013f-46fb-833b-5f272aafe5f3)

![image](https://github.com/user-attachments/assets/4e35c684-8d98-4e33-ad88-2ad24d7f6040)

![image](https://github.com/user-attachments/assets/b3e36402-ca90-4ea9-9325-4124e23fee31)

![image](https://github.com/user-attachments/assets/7b1587af-8a9b-45d5-9a96-8a27d7e273c8)







