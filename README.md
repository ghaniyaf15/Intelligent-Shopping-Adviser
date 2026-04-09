# Intelligent-Shopping-Adviser
Making project for giving advise in Shopping by using AI Agent

Project Report:
1. Introduction
The Intelligent Shopping Advisor is an AI-powered system designed to assist users in selecting optimal products based on their preferences, constraints, and budget. The system simulates real-world decision-making using a multi-agent architecture built with LangGraph.
It allows users to input natural language queries such as:
•	“Best smartphone under 100,000 PKR” 
•	“Laptop for gaming and programming” 
The system processes these queries and returns personalized product recommendations with explanations.
This project integrates Natural Language Processing (NLP), Retrieval-Augmented Generation (RAG), and multi-agent reasoning to deliver an intelligent and user-friendly shopping experience. 
2. Objectives
The main objectives of this project are:
•	To design a multi-agent AI system for recommendation tasks 
•	To implement workflow orchestration using LangGraph 
•	To process natural language queries into structured preferences 
•	To retrieve and rank products using data-driven logic 
•	To provide explainable AI-based recommendations 
•	To evaluate system performance using test cases and edge scenarios 
3. System Overview
The system consists of a frontend interface and a backend AI engine.
Key Functionalities
•	Natural language query understanding 
•	Preference extraction (budget, category, features) 
•	Product retrieval from database 
•	Product comparison and scoring 
•	Recommendation generation with justification 
•	Voice input and speech output 
4. System Architecture
The architecture follows a multi-agent pipeline using LangGraph, where each agent performs a specific task.
Architecture Components
1.	User Interface (React Frontend) 
o	Accepts user queries (text + voice) 
o	Displays recommendations 
2.	Backend API (FastAPI) 
o	Handles requests and responses 
o	Connects frontend with AI workflow 
3.	LangGraph Workflow 
o	Controls execution of agents 
o	Maintains state between steps 
4.	MongoDB Database 
o	Stores product dataset 
o	Enables efficient retrieval 
Workflow Pipeline
 5. Multi-Agent System Design
The system implements four core agents:
5.1 Preference Agent
Purpose: Extract structured data from user input
Functions:
•	Detects: 
o	Budget 
o	Product category 
o	Preferences (battery, performance, camera, etc.) 
•	Converts natural language → structured constraints 
5.2 Product Retrieval Agent
Purpose: Fetch relevant products
Functions:
•	Queries MongoDB database 
•	Filters products based on: 
o	Budget 
o	Category 
•	Returns candidate products 
5.3 Comparison Agent
Purpose: Evaluate and rank products
Evaluation Criteria:
•	Price 
•	Rating 
•	Battery 
•	Storage 
•	Camera 
•	Performance 
Output:
•	Scored and ranked product list 
5.4 Recommendation Agent
Purpose: Generate final recommendations
Functions:
•	Selects top 3–5 products 
•	Provides: 
o	Justification 
o	Feature highlights 
•	Ensures explainability 
6. Data Management
6.1 Data Source
•	Local dataset (data.json) 
•	Stored in MongoDB 
6.2 Database
•	Database: intelligent_shopping_advisor 
•	Collection: products 
6.3 Data Fields
•	Name 
•	Category 
•	Price 
•	Battery 
•	Performance 
•	Rating 
•	Camera 
•	Storage 
6.4 Data Pipeline
•	JSON dataset → MongoDB using seeding script 
•	Backend retrieves data dynamically 
7. Technology Stack
Backend
•	Python 3.10+ 
•	FastAPI 
•	LangGraph 
•	MongoDB 
Frontend
•	React 
•	Vite 
•	Axios 
Optional Enhancements
•	Voice Recognition APIs 
•	Text-to-Speech 
8. Implementation Phases
Phase 1: Basic System
•	Static dataset 
•	Simple preference extraction 
•	Basic recommendations 
Phase 2: Multi-Agent Integration
•	Implemented all agents 
•	Connected via LangGraph 
Phase 3: Data Enhancement
•	MongoDB integration 
•	Improved retrieval 
Phase 4: Advanced Features
•	Voice input/output 
•	Better reasoning and scoring 
9. API Design
Endpoints
•	GET /health → Check system status 
•	POST /recommend → Text-based recommendations 
•	POST /recommend/voice → Voice-based input 
10. User Interaction Flow
1.	User enters query 
2.	Query sent to backend 
3.	LangGraph executes agents sequentially 
4.	Recommendations generated 
5.	Results displayed on UI 
11. Testing and Evaluation
11.1 Test Dataset
•	50+ test queries 
•	Includes edge cases: 
o	Missing budget 
o	Conflicting preferences 
11.2 Evaluation Metrics
•	Accuracy 
•	Relevance 
•	Response time 
11.3 Testing Script
•	test_agent_flow.py validates pipeline 
12. Results
The system successfully:
•	Handles diverse natural language queries 
•	Produces accurate and relevant recommendations 
•	Provides explainable outputs 
•	Maintains fast response time 
13. Ethical Considerations
13.1 Data Privacy
•	No personal data stored 
•	Only query-based processing 
13.2 Bias
•	Recommendations depend on dataset quality 
•	Bias minimized through balanced data 
13.3 Limitations
•	Static dataset may become outdated 
•	LLM interpretation may not always be perfect 
13.4 Risks
•	Incorrect recommendations due to: 
o	Missing data 
o	Ambiguous queries 
14. Limitations
•	No real-time API integration (optional) 
•	Limited dataset size 
•	No user personalization history 
•	Dependent on query clarity 
15. Future Enhancements
•	Integration with Amazon/eBay APIs 
•	Real-time price updates 
•	Personalized user profiles 
•	Advanced vector search (FAISS/Pinecone) 
•	Improved ranking using ML models 
16. Deployment
Frontend
•	Hosted on Netlify 
Backend
•	Hosted on Render 
Database
•	MongoDB (local) 
17. Conclusion
The Intelligent Shopping Advisor demonstrates the practical application of multi-agent AI systems in real-world decision-making. By combining LangGraph orchestration, NLP, and data-driven ranking, the system provides accurate and explainable product recommendations.
This project successfully meets all assignment requirements and showcases the power of Generative AI in intelligent recommendation systems.
 
 
Project Video:
https://drive.google.com/file/d/1al-WNljngawRC6TebOM69doZPZFqH9m-/view?usp=sharing=sharing



