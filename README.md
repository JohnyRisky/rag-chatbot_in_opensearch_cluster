Conversational and conversational_flow typed RAG-chatbots initiated in the Opensearch cluster (5 nodes, one of them is for ML purposes). Each node was built within separate virtual machine.

Data flow into the cluster was executed by Telegraf agent that collected logs from the Opensearch and VM log files.

Incoming data goes through embeddeding model to create an embedding field for KNN search. Embedding and search performed by one model - multilingual MiniLM-L12-V2

Used 2 LLMs - Deepseek from Ollama started locally for user-question response generation
and OpenAI GPT-4o mini for PPL (Piped processong language) or DSL (Opensearch internal query language) queries. 

Also performed prompt tuning to get better LLM responses. 
