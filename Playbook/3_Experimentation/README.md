<h1 style="text-align: center;">GenAIOps Playbook</h1>
<h4 style="text-align: center;">GenAIOps playbook of crowd-source materials to deploy your Gen AI apps to production</h4>
<br></br>

![Experimentation Phase](/docs/Test.jpg)

<br></br>
# EXPERIMENTATION/TESTING
The Experimentation phase is where developers and business users work together to achieve two goals; optimize the application for both performance [System Testing] and ensure a great user experience [User Acceptance Testing (UAT)]  A best practice you must adopt is scaling your AI testing workbench to automate execution and evaluation of these test cases.  You will have many iterations/permutations of test scenarios due to the need in System Testing to iterate over different models, parameters, prompt techniques, indexing and data sources.  Developers will leverage tools like VS Code and the CLI to execute and review their experiments while busines users will leverage AI Foundry to audit and select the optimal configuration.

<br></br>
## Test Case Development

A Golden Data Set will be your list of Question & Answer pairs for your GenAI Application.  In early rounds of testing this data set is human generated based on typical questions an end-user might ask of the application.  The number of test cases is light in System testing but as we move into UAT testing we'll need to expand the data set to be more representative of the questions asked by users to mimic production questions.  There are tools like RAGAS available that will help you generate these type of questions.

Additionally, we will have different evaluation scenarios that we should conduct in System and UAT testing as milestones for governance teams to review prior to deployment to production.  These evaluations scenarios are; Quality, Safety, RAI, Conversational and Adversarial.

1. [RAG Evaluation Overview](https://github.com/Azure-Samples/ai-rag-chat-evaluator?tab=readme-ov-file#evaluating-a-rag-chat-app)
1. [Model Evaluation Overview](https://azure.github.io/Cloud-Native/30-days-of-ia-2024/evaluate-with-ai)
1. [RAG Deep Dive Evaluation Webinar](https://developer.microsoft.com/en-us/reactor/events/24578/)
1. [Code samples for eval scripts](https://github.com/Azure-Samples/azureai-samples/tree/main/scenarios/evaluate#objective)
1. [RAGAS Q&A Text Genration](https://docs.ragas.io/en/latest/concepts/test_data_generation/rag/#relationship-builder)
1. [Q&A Generation with Azure Search Index](https://github.com/Azure-Samples/azureai-samples/tree/main/scenarios/evaluate/Simulators/Simulate_Context-Relevant_Data/Simulate_From_Azure_Search_Index)
1. [Synthetic Data Generation with Hugging face](https://huggingface.co/blog/synthetic-data-generator)
1. [Evaluation Framework in Foundry](https://learn.microsoft.com/en-us/azure/ai-studio/how-to/evaluate-generative-ai-app)
1. [Evaluatoin Frameowrk in SDK](https://learn.microsoft.com/en-us/azure/ai-studio/how-to/develop/evaluate-sdk?source=recommendations)
1. [Test Scenarios & Metrics](https://medium.com/data-science-at-microsoft/evaluating-llm-based-chatbots-a-comprehensive-guide-to-performance-metrics-9c2388556d3e)


<br></br>
## System Testing
The goal of system testing is to iterate over the different permutations of test case scenarios to pick the optimal configuration for your application.  The test case scenarios are quality, safety, RAI, conversational and adversarial.  For each scenario, you will execute a set of test scripts to determine performance of the application for different configurations; models, data sources, indexes, Prompting, prompt techniques, model parameters and orchestrators.  A key factor in system testing is the automation of test scripts and evaluations.  A manual human review of every iteration will be time consuming and inconsistent.  In this phase for us to scale, we need to automate the evaluation of the test results thru LLM models or an AI Judge.

### Quality Model Evaluation
1. [Quality Evaluators/Metrics](https://learn.microsoft.com/en-us/azure/ai-studio/concepts/evaluation-metrics-built-in?tabs=warning#generation-quality-metrics)
1. [AI Foundry Evaluation Workflow](https://learn.microsoft.com/en-us/azure/ai-studio/how-to/flow-bulk-test-evaluation)
1. [Quality Sample Notbook](https://github.com/Azure-Samples/azureai-samples/blob/main/scenarios/evaluate/Supported_Evaluation_Metrics/AI_Judge_Evaluators_Quality/AI_Judge_Evaluators_Quality.ipynb)

1. [Custom Evaluators](https://github.com/realmanisingh/azure-ai-foundry-custom-evaluation)
1. [AI Foundry Evaluation Tools](https://learn.microsoft.com/en-us/azure/ai-studio/how-to/evaluate-results)
1. [Evaluation slides](https://aka.ms/ragdeepdive/evaluation/slides)

### Safety Model Evaluation
1. [Risk & Safety Overview](https://techcommunity.microsoft.com/blog/aiplatformblog/introducing-ai-assisted-risk-and-safety-evaluations-in-azure-ai-foundry/4098595)
1. [Risk and Safety Evaluators/Metrics](https://learn.microsoft.com/en-us/azure/ai-studio/concepts/evaluation-metrics-built-in?tabs=warning#risk-and-safety-evaluators)
1. [Risk & Safety Sample code](https://github.com/Azure-Samples/rag-data-openai-python-promptflow/blob/main/src/evaluation/evaluatesafetyrisks.py)

### Conversational Evaluations
1. [Conversational Single/Multi-turn](https://learn.microsoft.com/en-us/azure/ai-studio/concepts/evaluation-metrics-built-in?tabs=warning#conversation-single-turn-and-multi-turn)
1. [Conversational Simulations](https://learn.microsoft.com/en-us/azure/ai-studio/how-to/develop/simulator-interaction-data#generate-synthetic-data-and-simulate-non-adversarial-tasks)
1. [Conversational Sample Notebook](https://github.com/Azure-Samples/azureai-samples/blob/main/scenarios/evaluate/Simulators/Simulate_Context-Relevant_Data/Simulate_From_Conversation_Starter/Simulate_From_Conversation_Starter.ipynb)


### Adversarial Evaluations
1. [Adversarial Conversations Simulate](https://learn.microsoft.com/en-us/azure/ai-studio/how-to/develop/simulator-interaction-data#generate-adversarial-simulations-for-safety-evaluation)
1. [Adversarial Sample Notebook](https://github.com/Azure-Samples/azureai-samples/blob/main/scenarios/evaluate/Simulators/Simulate_Adversarial_Data/Simulate_Adversarial.ipynb)
1. [Jailbreak Simulations](https://learn.microsoft.com/en-us/azure/ai-studio/how-to/develop/simulator-interaction-data#simulating-jailbreak-attacks)
1. [Jailbreak sample code](https://github.com/Azure-Samples/azureai-samples/blob/main/scenarios/evaluate/Supported_Evaluation_Metrics/AI_Judge_Evaluators_Safety_Risks/AI_Judge_Evaluators_Safety_Risks_Text.ipynb)

### RAI Evaluations
1. [Responsible AI Foundry Overview](https://learn.microsoft.com/en-us/azure/ai-studio/responsible-use-of-ai-overview)
1. [Content Filters](https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/content-filters)
1. [Blocklists](https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/use-blocklists?tabs=api)
1. [RAI Workshops](https://github.com/Azure-Samples/RAI-workshops?tab=readme-ov-file)

### Performance Tuning/Cost Optimization
1. [Cost Estimation](https://azure.github.io/Cloud-Native/60DaysOfIA/managing-the-cost-of-intelligent-apps)

### Application Testing
1. Generate test scripts for your Application Functionality

<br></br>
## UAT Testing
User Acceptance Testing (UAT) is where the application code and configuration is locked into the optimal settings and test teams are reviewing test results to ensure optimal experience for the end-user.  This will require UAT team to generate a test case list that is representative of the questions that will be in production.  Business users should think thru all the different types of questions and build out categories and ensure you have sufficient coverage in each to know 
what to expect when a user asks a question from the system.  The system is stocastic and there is never the perfect response (Boolean: True/False).  In this round you are ensuring these responses are acceptable to your end-user community and Governance teams over time will develop these standards
In System test we iterate on all the different test scenarios during this round we will ensure we have exhaustive test cases so we are ready for production.

### Testing Objectives
1. [End-to-end test procedures](https://learn.microsoft.com/en-us/azure/well-architected/ai/test)
1. Repeat all system test scripts on Golden Data Set

### Observability (Debugging)
1. [Continuous Monitoring of Generative AI Applications](https://techcommunity.microsoft.com/blog/aiplatformblog/continuously-monitor-your-genai-application-with-azure-ai-foundry-and-azure-moni/4303450)
1. [Tracing in AI Foundry](https://learn.microsoft.com/en-us/azure/ai-studio/how-to/develop/visualize-traces)
1. [Tracing in Azure AI Foundry SDK](https://learn.microsoft.com/en-us/azure/ai-studio/concepts/trace)
1. [Tracing in AppInsights](https://learn.microsoft.com/en-us/azure/ai-studio/how-to/develop/trace-production-sdk#view-tracing-data-in-application-insights)

### Load/Stress Testing
1. [Load Testing Guidance](https://techcommunity.microsoft.com/blog/azure-ai-services-blog/load-testing-rag-based-generative-ai-applications/4086993)
1. [Azure OpenAI Demo Load Testing sample code](https://github.com/Azure-Samples/azure-search-openai-demo/blob/main/docs/productionizing.md#load-testing)
1. [Azure Load Testing](https://github.com/Azure/GPT-RAG/blob/main/docs/LOAD_TESTING.md)
1. [Locust Load Testing tool](https://learn.microsoft.com/en-us/azure/load-testing/quickstart-create-run-load-test-with-locust?tabs=portal)
1. [Scale TPM with API management](https://learn.microsoft.com/en-us/azure/developer/python/get-started-app-chat-scaling-with-azure-api-management?tabs=github-codespaces%2Cinitial-deployment)

### Red Teaming
1. [Red Teaming Guidelines](https://learn.microsoft.com/en-us/azure/ai-services/openai/concepts/red-teaming)
1. [Red Teaming Executive Summary](https://www.microsoft.com/en-us/security/blog/2025/01/13/3-takeaways-from-red-teaming-100-generative-ai-products/)
1. [Red Teaming Whitepaper](https://airedteamwhitepapers.blob.core.windows.net/lessonswhitepaper/MS_AIRT_Lessons_eBook.pdf)
1. [Red Teaming Best Practices](https://news.microsoft.com/source/features/ai/red-teams-think-like-hackers-to-help-keep-ai-safe/)
1. [RAI Automation tools](https://azure.github.io/PyRIT/)

### A/B Testing
1. [A/B Testing for AI applications](https://learn.microsoft.com/en-us/azure/ai-studio/concepts/a-b-experimentation)