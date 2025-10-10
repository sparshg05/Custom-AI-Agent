# Omni AI Agent Documentation

## 🌟 Overview
Omni is not just another chatbot—it's an autonomous AI agent that can:  

🔍 Search the web in real-time using Tavily API  
🎬 Provide movie recommendations using TMDB API  
🧠 Make intelligent decisions about which tools to use  
🔗 Chain multiple tools together for complex queries  
💾 Maintain persistent conversation history  
🔄 Adapt its strategy based on results  

What Makes It Special?  
Unlike traditional chatbots that simply respond to questions, Omni uses LangGraph's ReAct pattern to:  

1. Reason about the user's query  
2. Decide which tools to use autonomously  
3. Act by calling appropriate APIs  
4. Observe the results  
5. Repeat if more information is needed  

This creates a truly autonomous agent that can handle complex, multi-step tasks without hardcoded logic.  

## ✨ Key Features
🤖 Autonomous Tool Selection  
• AI automatically decides which tool to use based on query intent  
• No hardcoded if-else logic—pure emergent behavior from LLM reasoning  
• Supports chaining multiple tools for complex queries  

🔍 Web Search Integration (Tavily)  
• Real-time web search capabilities  
• Retrieves up to 3 relevant results per query  
• Provides sourced, up-to-date information  

🎬 Movie Intelligence (TMDB)  
• 7 specialized movie tools:  
 • Search movies by title  
 • Get detailed movie information (cast, crew, budget, ratings)  
 • Browse popular movies  
 • Discover top-rated films  
 • See trending movies (daily/weekly)  
 • Get personalized recommendations  
 • Explore movies by genre  

💬 Conversation Management  
• Persistent conversation threads using MongoDB  
• Auto-generated conversation titles using AI  
• Full conversation history with search functionality  
• Edit, delete, and organize conversations  
• Load previous conversations seamlessly  

🎨 Modern UI/UX  
• Responsive React frontend with dark/light themes  
• Smooth animations and loading states  
• Mobile-friendly design  
• Collapsible sidebar for conversation management  
• Real-time typing indicators  

## 🛠️ Tech Stack
Frontend-  
• React 19.1.1 - UI framework  
• Axios - HTTP client  
• CSS3 - Styling with custom properties  
• React Context - State management  

Backend-  
• Node.js / Bun - JavaScript runtime  
• Express 5.1.0 - Web framework  
• MongoDB 8.1.0 - Database  
• Mongoose - ODM for MongoDB  

AI/ML Stack-  
• LangChain Core 0.3.75 - LLM orchestration  
• LangGraph 0.4.9 - Agent workflow management  
• ChatGroq - LLM provider (openai/gpt-oss-120b)  
• Tavily 0.1.5 - Web search tool  
• Zod - Schema validation  

External APIs-  
• Tavily Search API - Real-time web search  
• TMDB API - Movie database (1M+ movies)  
• GROQ API - Language model inference  

## How to Test the Project
1. Prerequisites-  
//Install Bun if not already installed  
curl -fsSL https://bun.sh/install | bash  


2. Project Setup-  
//Clone the repository  
git clone <repository-url>  
cd custom-ai-agent

  //Install dependencies  
  bun install  


4. Environment Setup  
Create a .env file with necessary API keys:  
GROQ_API_KEY=your_groq_api_key  
TAVILY_API_KEY=your_tavily_api_key  


5. Running the Application  
bun run index.js  

6. Testing the Chat  
Start typing messages after the "User:" prompt  
Ask questions that might require web searches  
Type "exit" to end the session  


## Project Structure
custom-ai-agent/  
├── index.js        # Main application file  
├── package.json    # Project dependencies  
├── .env           # Environment variables (not in repo)  
└── README.md      # Project documentation


![langgraph_visualization](https://github.com/user-attachments/assets/7f81ba4e-afd9-438b-bd70-84b6c9357d02)
