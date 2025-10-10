#  Agentic RAG Fitness Chatbot


##  Overview
The **Agentic RAG Fitness Chatbot** is an AI-powered application designed to provide **personalized fitness guidance** and **workout recommendations**.  
It leverages **Retrieval-Augmented Generation (RAG)**, **multi-agent systems**, and a **curated knowledge base** to deliver **context-aware** and **actionable fitness advice**.  

The chatbot focuses on **empowering beginners** with evidence-based recommendations, **real-time video demonstrations**, and **safety guidelines** to support safe and effective workouts.


---

## Architecture
The system is built with modular components working together to process and respond intelligently to user inputs:

1. **User Input**  
   Accepts user queries through a Streamlit-based chat interface.

2. **Query Refinement**  
   Transforms the raw input into an optimized query using an LLM-driven rewriting mechanism.

3. **Retrieval System**  
   - Encodes queries using **Sentence Transformers**  
   - Searches the **Pinecone Vector Database** for relevant fitness data  
   - Retrieves **video demonstrations** and **exercise transcripts**

4. **Response Generation**  
   Combines retrieved content using **GPT-4o** to produce clear, practical, and evidence-based responses.

5. **Video Recommendations**  
   Displays workout **thumbnails**, **titles**, and **links**, along with detailed transcripts for user reference.

6. **LangSmith Integration**  
   Monitors agent-level reasoning, tracks tool calls, and improves system reliability through analytics.




---

##  Installation

### Steps

```bash
# 1️⃣ Clone the repository
git clone https://github.com/pramod-zillella/AgenticRagChatbot.git
cd agentic-rag-fitness-chatbot

# 2️⃣ Install dependencies
pip install -r requirements.txt

# 3️⃣ Set up environment variables
# Create a .env file in the project directory and add:
OPENAI_API_KEY=your_openai_api_key
PINECONE_API_KEY=your_pinecone_api_key
LANGCHAIN_API_KEY_V2=your_langchain_api_key

# 4️⃣ Run the Streamlit application
streamlit run interface.py

