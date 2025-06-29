# CloudSecurity_Recommendation_Chatbot

**1. Overview**
It will be an interactive chatbot powered by GenAI open source models which will analyze the respective AWS or Azure Account, collect all the security logs, network configs, VM configs and other resource configs.
Based on collected data, it will respond to user queries for example if user prompts to list all the VMs which has public IP exposed to internet, it will list down specific VM details. Another example could be – list all the security group where port 22 is allowed, this will list down the security group details along with the associated VMs, Network, etc.

**2. Core Components**
Below are the vital components required for deployment of Cloud Security Recommendation Agent -
Cloud - Azure subscription where application will be deployed
Virtual Machine - GPU VM for backend and CPU VM for frontend
GenAI model - OpenSource models from HuggingFace
Storage – Azure Cosmos DB for MongoDB
Vector store - FAISS

**3. Technology Stack**
Backend –
Program- Python, Langchain
Cloud Data Access – Boto3 (AWS SDK)
LLM – mistralai/Mistral-7B-Instruct
Embedding Model – sentence-transformers/all-MiniLM-L6-v2
Langchain Tools – Agents, Document Loaders, RetrieverChain
 
Frontend –
Tool - Gradio
Program- Angular.js, HTML,
Style - CSS,
Design - Figma

**4. Folder Structure**
genai_securityrecommendation chat-bot/
main_chatbot_notebook.ipynb #Main Colab notebook for orchestration
config.py     #Configuration settings (AWS region, data paths, LLM
aws_data_collector.py  #Functions to interact with AWS APIs and collect
data_processor.py    # Functions to transform raw AWS data into vector
vector_store_manager.py  #Handles vector store creation and loading
llm_model_loader.py    # Loads the open-source LLM from HuggingFace 
chatbot_logic.py      # Contains the LangChain conversational chain
.env # For storing sensitive AWS credentials (NOT committed to Git)
