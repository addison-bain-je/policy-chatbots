# policy-chatbots
Chatbots to answer employee questions, based on policy documents uploaded to SharePoint using RAG techniques

#Base architecture
#SharePoint
<br>SharePoint document repository to store text-based policy documents (e.g. .DOCX, .PDF)
<br>
#APIs via Postman
<br>1.  Create data source on Azure AI Search Service by linking to SP document repo
<br>2.  Add skillset key phraser extractor on Azure AI Search Service (optional)
<br>3.  Create Search Index (empty structure) on Azure AI Search
<br>4.  Create and run Search Indexer on Azure AI search (with scheduler for first-time)
<br>5.  Get Indexer status and check search index

<br>Finance SOP API Documentation
<br>
https://web.postman.co/workspace/2cc7da80-fdce-4284-8a32-22af6a60d5cf/documentation/34781301-acf61f11-fbcf-4259-80fa-d8d5b627ce52
<br>HR Policies API Documentation
<br>
https://web.postman.co/workspace/2cc7da80-fdce-4284-8a32-22af6a60d5cf/documentation/34781301-6141cc74-2cc6-4bcd-b967-edadb1c93e5c

<br>
<br>
#Azure AI Studio  
<br>6. In Azure AI Studio chatplayground, connect to Search Index and deployed Azure OpenAI model (GPT 4-32k or GPT4o
<br>7. Experiment with parameters (retrieval, strictness, top p)
<br>
#Azure WebApp
<br>8. Deploy directly to Azure WebApp for basic chatbot interface


