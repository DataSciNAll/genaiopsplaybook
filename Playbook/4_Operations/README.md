<h1 style="text-align: center;">GenAIOps Playbook</h1>
<h4 style="text-align: center;">GenAIOps playbook of crowd-source materials to deploy your Gen AI apps to production</h4>
<br></br>

![Operations Phase](/docs/Ops.jpg)

<br></br>
# OPERATIONS
The Operations phase is all about deploying your Generative AI applications to production and keeping the lights while minimizing the risks.Think of it like launching a new product - you've tested it thoroughly, and now it's time to get it out there!

Repeatability is crucial for long-term success and setup of Continuous Integration/Continuous Deployment (CI/CD) will automate this process and enable an Agile workflow.  Risk mitigation and meeting your SLAs require monitoring your application while it is live and online.  You need to keep a close eye on how it's performing and how users are interacting with it. 

Lastly, a feedback loop should be developed in the application where you can capture Q&A pairs and have end users crowd-source ground truth data.  This feedback can be good to test our your application and develop assets like adding data sources or Fine-tuning your data.

<br></br>
## Deployment pipelines in CI/CD Repos
CI/CD deployment pipelines and setting up change control procedures are necessary prior to launch to production.  The CI/CD tools can leverage Azure DevOps or Github Actions.  Additionally, we will want to build into the workflow our evaluation routines so we can summarize the results and include it in the approval workflow for pull requests.

1. [CI/CD Deployment pipelines](https://learn.microsoft.com/en-us/azure/machine-learning/prompt-flow/how-to-end-to-end-azure-devops-with-prompt-flow?view=azureml-api-2)
1. [CI/CD Accelerator](https://github.com/Azure/GenAIOps)
1. [GenAIOps reference architecture](https://github.com/Azure/GenAIOps/blob/main/media/reference_architecture.png)
1. [CI/CD Code Sample](https://microsoft.github.io/llmops-workshop/labs/lesson_05/lab05.html)
1. [GenAIOps Maturity](https://learn.microsoft.com/en-us/azure/machine-learning/prompt-flow/concept-llmops-maturity?view=azureml-api-2)
1. [GenAIOps Roles & Responsibilities](https://github.com/Azure/GenAIOps/blob/main/documentation/project_roles.md)


<br></br>
## Monitoring
Online evaluations of the Generative AI application and monitoring its performance will ensure you mitigate risks of the application.  Additionally, you will have traceability across the application to run a root cause analysis on what caused different issues with your end-users.

1. [Monitoring across application lifecycle](https://learn.microsoft.com/en-us/microsoft-cloud/dev/copilot/isv/Observability-for-AI)
1. [Monitoring Slides](https://aka.ms/ragdeepdive/monitoring/slides)
1. [Online evaluation in production](https://learn.microsoft.com/en-us/azure/ai-studio/how-to/online-evaluation)
1. [Prevent Model Decay](https://learn.microsoft.com/en-us/azure/well-architected/ai/test#prevent-model-decay)
1. [Monitoring with App Insights](https://azure.github.io/Cloud-Native/30-days-of-ia-2024/deploy-with-aca#4--monitoring-with-app-insights)
1. [OpenTelemetry](https://learn.microsoft.com/en-us/azure/azure-monitor/app/opentelemetry-enable?tabs=python)
1. [Online Evaluation Cloud Schedule](https://github.com/Azure-Samples/azureai-samples/blob/main/scenarios/evaluate/Supported_Evaluation_Targets/Evaluate_Online/Evaluate_Online.ipynb)


<br></br>
## Development Review Boards
Standards, best practices and change control should be lead by an independent team from the end-users or developers.  This is typically lead by a Center of Excellence or Governance teams.  The purpose of this review board will ensure you have consistency across applications and standards.

1. [AI Governance](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/scenarios/ai/govern)
1. [AI Change Control](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/scenarios/ai/manage)
1. [Reponsible AI Transparency Report](https://cdn-dynmedia-1.microsoft.com/is/content/microsoftcorp/microsoft/final/en-us/microsoft-brand/documents/responsible-aI-transparency-report-2024.pdf)
1. [Production Checklist](https://github.com/Azure-Samples/azure-search-openai-demo/blob/main/docs/productionizing.md#rag-chat-productionizing-the-app)

<br></br>
## Blue/Green Deployments
Coming Soon......