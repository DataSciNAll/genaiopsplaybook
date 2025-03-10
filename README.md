<h1 style="text-align: center;">GenAIOps Playbook</h1>
<h4 style="text-align: center;">GenAIOps playbook of crowd-source materials to deploy your Gen AI apps to production</h4>
<br></br>


We are thrilled to share the best tools, guides, and insights on GenAIOps from our vibrant developer community. We hope that this blog can become your go-to playbook for mastering GenAIOps, offering a comprehensive workflow that you can leverage for seamless production deployments. We love to crowd-source this playbook and encourage you to share your top resources and suggestions via pull requests.  As a community, we can share our best practices, lessons learned and learing resources to build the future of Generative AI applications together.  In today's world, it is not the technology that is the most challenging rather the process and this is the key blocker we hope to overcome.

There will be four phases: Prototype, Development, Experimentation/Testing and Operations.  Here is a digram of this conceptual model and will leverage it as a Table of contents for developers.  This is not an industry or Microsoft standard for GenAIOps.
<br></br>



![GenAIOpsWorkflow diagram ](./docs/GenAIOps.jpg)

<br></br>
# TABLE OF CONTENTS
| **Prototype** |  **Development**  | **Experimentation** |  **Operations**  |
|---------------|-------------------|---------------------|------------------|
| [Business Use Case](./Playbook/1_Prototype/README.md#business-use-case) | [Gen AI Patterns](./Playbook/2_Development/README.md#gen-ai-architecture-patterns) | [Test Case Development](./Playbook/3_Experimentation/README.md#test-case-development) | [CI/CD](./Playbook/4_Operations/README.md#deployment-pipelines-in-cicd-repos)|
| [Model Benchmarks](./Playbook/1_Prototype/README.md#model-benchmarks) | [Prompt Engineering](./Playbook/2_Development/README.md#prompt-engineering)|[System Testing](./Playbook/3_Experimentation/README.md#system-testing) | [Monitoring](./Playbook/4_Operations/README.md#monitoring) |
| [Prompt Playground/Unit Testing](./Playbook/1_Prototype/README.md#prompt-playground-unit-testing) | [RAG](./Playbook/2_Development/README.md#rag) | [UAT Testing](./Playbook/3_Experimentation/README.md#uat-testing) | [Deployment Review Board](./Playbook/4_Operations/README.md#development-review-boards) |
| [Impact Assessment](./Playbook/1_Prototype/README.md#impact-analysis) (Responsible AI) | [Fine-tuning](./Playbook/2_Development/README.md#fine-tuning) || [Blue-Green Deployments](./Playbook/4_Operations/README.md#bluegreen-deployments)|
|  | [Orchestration](./Playbook/2_Development/README.md#orchestration) | ||
|  | [Application](./Playbook/2_Development/README.md#application) | ||


## DevOps Lifecycles
Before we dive in, let's define different DevOps lifecycles to help differentiate this one and integrate it into your existing workflows:

1.  <u>**DevOps**</u>: A set of practices that combines software development and IT operations to shorten the system development lifecycle and provide continuous delivery with high software quality.
2.  <u>**DataOps**</u>: A collaborative data management practice aimed at improving communication, integration, and automation of data flows between data managers and data consumers within an enterprise.
3.  <u>**MLOps**</u>: A set of practices that aim to deploy and maintain machine learning models in production reliably and efficiently.
4.  <u>**LLMOps**</u>: Specialized practices and workflows designed to streamline the development, deployment, and management of Large Language Models (LLMs) throughout their lifecycle.
5.  <u>**GenAIOps**</u>: A comprehensive set of practices, tools, and frameworks designed to manage the lifecycle of generative AI applications.

I've spent some time reflecting on and debating the difference between LLMOps and GenAIOps. Microsoft recently updated their literature to include GenAIOps workflows, a change from its past terminology of LLMOps. The difference here is subtle but important. There are two workflows: one for building Large Language Models (Foundation Models) and another for applications that use LLMs for inference to support their user community. This blog will focus on the latter.

The GenAIOps model contains all the necessary steps for building Generative AI applications. There are many more references for advanced topics like GraphRAG, multimodal, or Distillation, which will be covered in future blogs as they become more widely adopted and standardized. This workflow is the most common for building "Chat with your data" (Chatbot) applications.



## Contributors
A special thanks to these Cloud advocates who really accelerate our AI Innovations.  Pamela Fox, Nitya Narasimhan, Marlene Mhangami, Facundo Santiago, Farzad Sunavala, Cassie Breviu, Cedric Vidal, Dan Taylor, Rob Chambers, Meera Kuurup, Reza Bonyadi, Jennifer Marsman, Seth Juarez, Priya Vergadia, Apurva Mody, John Alexander, Casey Doyle, Govind Kamtamneni, Piyush Jain, Deepsha Menghani, Shimin Zhang, Paulo Lacerda and Lino Tadros.

### Sample Repos
1. [Contoso Creative Writer](https://github.com/Azure-Samples/contoso-creative-writer?tab=readme-ov-file)
1. [Contoso Creative Writer Langchain](https://github.com/Azure-Samples/contoso-creative-writer-langchain)
1. [RAG Notebook](https://github.com/Azure-Samples/rag-with-azure-ai-search-notebooks)
1. [RAG Chat Evaluator](https://github.com/Azure-Samples/ai-rag-chat-evaluator)
1. [Oberservability with Fitness Tracker](https://github.com/Azure/ai-foundry-workshop/blob/main/docs/2-notebooks/3-quality_attributes/1-Observability.ipynb)
1. [Dan Taylor AI Foundry Demo content](https://github.com/qubitron/aifoundry-demo)
1. [RAG Workshop](https://nitya.github.io/azure-ai-rag-workshop/)