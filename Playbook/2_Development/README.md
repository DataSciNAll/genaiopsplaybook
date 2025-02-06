<h1 style="text-align: center;">GenAIOps Playbook</h1>
<h4 style="text-align: center;">GenAIOps playbook of crowd-source materials to deploy your Gen AI apps to production</h4>
<br></br>

![Development Phase](/docs/Dev.jpg)

<br></br>
# DEVELOPMENT
This playbook focuses on organizations building their own copilot applications in a code-first implementation.  These implmentation at Microsoft are typically called, "Custom copilots".  There are developer tools like Copilot Studio that empower citizen developers to build Generative AI applications.  These applications can have similar capabilties but are not fully extensible.  As we move into the development phase, we leverage application developers and potentially data scientists to build out the assets.  Application developers can do 80% of teh work since most of the work is API calls.  We will need the Application Developers to retrain to understand new development and testing frameworks but change management is a natural workflow.  20% of the time we will need Data Scientist and this happends when we want to Fine-tune our models and the level of model development might be too complex for them to build their own models.  This is natural but only occurs if your application groundedness is unacceptable and need to fine-tune it to improve performance.  This shouldn't be common so you won't need many data scientists rather many Application Developers.

<br></br>
## Gen AI Architecture Patterns
AI Foundations will be a critical pattern to study to fully understand the pre-requisites to building a Generative AI application.  We have five layers, infrastructure, data, AI, applications and security.  These foundations in a nutshell are typically designed as a set of microservices and leverage cloud scalers to help you scale them in production.

1. [AI Azure Services Diagram](https://devblogs.microsoft.com/all-things-azure/how-to-develop-ai-apps-and-agents-in-azure-a-visual-guide/)
2. [Azure OpenAI Design Decisions](https://learn.microsoft.com/en-us/azure/well-architected/service-guides/azure-openai)
3. [Azure OpenAI Landing Zone for Chat with your Data](https://learn.microsoft.com/en-us/azure/architecture/ai-ml/architecture/azure-openai-baseline-landing-zone)

<br></br>
## Prompt Engineering
Prompt engineering like creative writing or book writing is an art you need to master.  There are key concepts, techniques, design principles, structure and formatting you should follow for the model to fully understand your directions.  This section will help you realize these models are like young children and for full comprehension you need to be explicit and concise to ensure optimal performance.  A future topic will be cost optimzation to ensure your context windows are sufficient and not to verbose so you are not overpaying for the application.

1. [Fundamentals](https://github.com/microsoft/generative-ai-for-beginners/tree/main/04-prompt-engineering-fundamentals)
2. [Prompt Engineering](https://medium.com/data-science-at-microsoft/demystifying-the-art-of-writing-prompts-cb1bf8c55862)
3. [Prompt Engineering Techniques](https://www.promptingguide.ai/techniques)
4. [Prompt Design](https://arxiv.org/pdf/2401.14423)
5. [Chat Completions with GPT4 models](https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/chatgpt?tabs=python-new)

<br></br>
## RAG
LLM models are trained on data on the public internet and their published dates are typically more than 8 months old.  This means we need to ground our queries with current or enteprise data for the models to accurately answer the queries.  Retrieval Augmentation Generation (RAG) is an application pattern which passes into the LLM model the user question and context to help it answer the question.  This playbook shares multiple platforms that support RAG architectures and guidance on how to chunk your data for optimal information retrieval.  This is a key area of study which can help you improve the overall accuracy of your application.

### RAG Design Patterns
1. [Getting Started](https://learn.microsoft.com/en-us/azure/architecture/ai-ml/guide/rag/rag-solution-design-and-evaluation-guide)
2. Read full series of 6 articles after Getting started in table of contents; Preparation Phase, Chunking Phase, Chunk Enrichment phase,   embedding Phase, Information-retrieval phase and LLM end-to-end evaluation phase

### RAG with OpenAI on your Data
1. [Azure OpenAI on your Data user guide](https://learn.microsoft.com/en-us/azure/ai-services/openai/concepts/use-your-data?tabs=ai-search%2Ccopilot)

### RAG with Azure Search
1. [RAG Tutorial Series with Azure Search](https://learn.microsoft.com/en-us/azure/search/tutorial-rag-build-solution)
2. [RAG Capabilities in Azure Search](https://techcommunity.microsoft.com/blog/azure-ai-services-blog/prep-your-data-for-rag-with-azure-ai-search-content-layout-markdown-parsing--imp/4303538)
3. [Integrated Vectorization Guide](https://learn.microsoft.com/en-us/azure/search/vector-search-integrated-vectorization)
4. [Code Sample](https://github.com/Azure/azure-search-vector-samples/blob/main/demo-python/code/integrated-vectorization/azure-search-integrated-vectorization-sample.ipynb)
5. [Document Processing](https://farzzy.hashnode.dev/revolutionizing-document-ingestion-rag-with-docling-azure-ai-search-and-azure-openai)

### Data Chunking to Build your Own RAG
1. [Chunking Strategies Whiteboard](https://towardsdatascience.com/the-art-of-chunking-boosting-ai-performance-in-rag-architectures-acdbdb8bdc2b)
2. [Chunking Strategies Blog](https://medium.com/data-science-at-microsoft/theres-more-than-one-way-to-chunk-a-rag-34e17fb0c96a)
3. [Data Converter](https://github.com/microsoft/markitdown)
4. [Langchain chunking code sample](https://github.com/deepshamenghani/chunking_strategies_langchain)
5. [Best practices chunking tutorial](https://github.com/FullStackRetrieval-com/RetrievalTutorials/blob/main/tutorials/LevelsOfTextSplitting/5_Levels_Of_Text_Splitting.ipynb?source=post_page-----acdbdb8bdc2b--------------------------------)
6. [Document chunking with Document Intelligence](https://learn.microsoft.com/en-us/azure/ai-services/document-intelligence/concept/retrieval-augmented-generation?view=doc-intel-4.0.0)

### Vector Database
1. [Generative AI application with AI Search](https://github.com/Azure-Samples/azure-search-openai-demo)
2. [Generative AI application with CosmosDB](https://devblogs.microsoft.com/all-things-azure/how-to-build-chatgpt-like-enterprise-search-on-your-own-data/)
3. [Generative AI application with PostgresSQL for RAG](https://reactor.microsoft.com/en-us/reactor/events/23331/)

<br></br>
## Fine-tuning
INSERT Description here
1. [Beneifts of Fine-tuning](https://learn.microsoft.com/en-us/azure/ai-studio/concepts/fine-tuning-overview)
2. [FIne-tuning workflow](https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/fine-tuning?source=recommendations&tabs=azure-openai%2Cturbo%2Cpython-new&pivots=programming-language-studio)

<br></br>
## Orchestration
Insert Description Here

1. [Orchestration overview](https://medium.com/@mkochar/compounding-genai-success-why-orchestration-is-the-key-to-mastering-generative-ai-543a2952acfe)
2. [Orchestration environments](https://medium.com/data-science-at-microsoft/harnessing-the-power-of-large-language-models-a-comparative-overview-of-langchain-semantic-c21f5c19f93e)
3. [Promptflow](https://learn.microsoft.com/en-us/azure/machine-learning/concept-retrieval-augmented-generation?view=azureml-api-2)
4. [Prompty OVerview](https://prompty.ai/docs/getting-started/concepts) & [Prompty Runtime](https://pypi.org/project/prompty/)
5. [Semantic Kernel](https://github.com/microsoft/semantic-kernel)
6. [Langchain on Azure](https://learn.microsoft.com/en-us/azure/ai-studio/how-to/develop/langchain)
7. [Llamaindex on Azure](https://learn.microsoft.com/en-us/azure/ai-studio/how-to/develop/llama-index)
8. [Code Sample with Langchain](https://github.com/Azure-Samples/contoso-creative-writer-langchain)

<br></br>
## Application
Insert Description Here

1. [UX Best practices](https://learn.microsoft.com/en-us/microsoft-cloud/dev/copilot/isv/UX-Guidance)
2. [Contoso Real Estate Reference Architecture](https://techcommunity.microsoft.com/blog/appsonazureblog/announcing-contoso-real-estate-javascript-composable-application-reference-sampl/3827097)
3. [Contoso Real Estate Code Sample](https://github.com/Azure-Samples/contoso-real-estate)
4. [Develop with SK](https://learn.microsoft.com/en-us/azure/ai-studio/how-to/develop/semantic-kernel)
5. [Develop with langchain](https://learn.microsoft.com/en-us/azure/ai-studio/how-to/develop/langchain)
6. [AI Templates](https://learn.microsoft.com/en-us/azure/ai-studio/how-to/develop/ai-template-get-started?tabs=python)