<h1 style="text-align: center;">GenAIOps Playbook</h1>
<h4 style="text-align: center;">GenAIOps playbook of crowd-source materials to deploy your Gen AI apps to production</h4>
<br></br>

![Prototype Phase](/docs/Proto.jpg)

<br></br>
# PROTOTYPE
We need to shift our mindsets from the limitations of technology to focus on the potential of the technology with new AI Innovations.  In previous technology innovations developers needed to set expectations on the art of the possible and be in the driver seat to avoid projct overruns.  In today's application development project we need the business users in the driver's seat to fully understand the business processes, core competencies, business strategy and industry to learn where is the best places to apply this technology.  

In my opinion, the big change agent with LLMs is Natural Language Processing (NLP).  This empowers anyone in the organization to prototype and incubate their business ideas with Azure AI Foundry.  Business units just like with business plans are able to test out their hyptothesis, conduct financial analysis, test the limitations of the technology and conduct an impact analysis.  This should really help organization scale their adoption of the technology since the bottleneck will not be prototyping but downstream workflows.  This means the business will have total visiblity into their technology investment and can prioritize the winners and losers while developers build well designed cutting-edge Generative AI applications.

The biggest blocker is not the technology rather the process and with enough iterations it will become habit.

<br></br>
## Business Use Case

Every employee of an organization can become an expert in business planning.  A Design thinking mindset and Subject Matter Expertise in an industry or functional unit is all we need to get started.  The links will outline the tools, strategies and programs you can leverage to assess its business viability.



1. [Business Envision Workshop](https://learn.microsoft.com/en-us/microsoft-cloud/dev/copilot/isv/Business-Envisioning)
2. [Microsoft Generative AI Application Scenarios](https://learn.microsoft.com/en-us/microsoft-cloud/dev/copilot/isv/isv-extensibility-story?ns-enrollment-type=Collection&ns-enrollment-id=penzt16genw8jx)
3. [Go-to-Market (GTM) plans](https://learn.microsoft.com/en-us/microsoft-cloud/dev/copilot/isv/commercialization)

<br></br>
## Model Benchmarks
AI Foundry has a deep set of models in their model catalog.  We all realize there is no one model right for every job and we need to focus on the model candidates for our GenAI applications.  The Model Benchmarks in AI Foundry will help us determine those best candidates.  The benefit of model benchmarks is the ability to leverage public data to evaluate the best models and substitute the public data with your golden data set to sanity check your best model candidates.  It is our goal during the experimentation phase to leverage a more rigorous testing data set and methodology.  We will deploy these model candidates into our AI Foundry project for unit testing.

1. [Model Selection](https://techcommunity.microsoft.com/blog/aiplatformblog/the-future-of-ai-is-model-choice---from-structured-process-to-seamless-platform/4284091) (One Size Does Not Fit All)
2. [Model Benchmarks](https://techcommunity.microsoft.com/blog/aiplatformblog/compare-and-select-models-with-new-benchmarking-tools-in-azure-ai-foundry/4292308)
3. [Pick the right model for the job](https://developer.microsoft.com/en-us/reactor/events/23433/)

<br></br>
## Prompt Playground/ Unit Testing
Azure AI Foundry has a number of tools for developers, business users, data scientists and citizen developers to prototype a Gen AI application.  The tools are Azure AI Foundary portal, Github portal, VS Code, Codescape and Azure CLI.  In this phase, business users are able to leverage Azure AI Foundry Portal or Github to browse the model catalog, deploy their own models, augment the models with your data and work in the playground to determien feasibility of the application.  There are four steps that are required to setup the playground and start your unit testing; Azure AI Foundry access, setup of OpenAI on your Data, deploy models, unit test.

### Azure AI Foundry
1. [Portal](https://learn.microsoft.com/en-us/azure/ai-studio/concepts/architecture)
2. [VS Code](https://learn.microsoft.com/en-us/azure/ai-studio/how-to/develop/vscode)
3. [AI Toolkit for VS Code](https://techcommunity.microsoft.com/blog/azuredevcommunityblog/ai-toolkit-for-visual-studio-code-october-2024-update-highlights/4298718)
4. [SDK](https://techcommunity.microsoft.com/blog/aiplatformblog/ignite-2024-announcing-the-azure-ai-foundry-sdk/4295862)
5. [Prompt Playground](https://learn.microsoft.com/en-us/azure/ai-services/openai/use-your-data-quickstart?tabs=keyless%2Cjavascript-keyless%2Ctypescript-keyless%2Cpython-new&pivots=ai-foundry-portal#chat-playground)
6. [Manual Evaluation](AI Foundry Manual Evaluation)

### OpenAI on your Data
1. [Ground your data](https://techcommunity.microsoft.com/blog/azure-ai-services-blog/on-your-data-is-now-generally-available-in-azure-openai-service/4059514)


### Deploy Models
1. [Model Catalog](https://learn.microsoft.com/en-us/azure/machine-learning/concept-model-catalog?view=azureml-api-2)
2. [Deployment options](https://learn.microsoft.com/en-us/azure/ai-studio/concepts/deployments-overview#deploying-models)

### Unit Testing in playground
1. [Playground Evaluation](https://learn.microsoft.com/en-us/azure/ai-studio/how-to/evaluate-prompts-playground)
2. [Unit testing across models in VS Code](https://github.com/Azure-Samples/azureai-samples/blob/main/scenarios/evaluate/Supported_Evaluation_Targets/Evaluate_Base_Model_Endpoint/Evaluate_Base_Model_Endpoint.ipynb)

<br></br>
## Impact Analysis
Trustworthy AI (AKA Responsible AI) needs to be started at the beginning of hte application lifecycle.  This will prevent false starts or potential organization damage from unforseen circumstances.  Just like M&A activity requires a heavy focus on due diligence this same risk analysis and migration strategy needs to occur the the first stage called Imapct Assessment which should occur right before you start any design or development work.  This way you fully understand its impact on the end-users and determine if the investment of time and money will delight your customers.

1. [Trustworthy AI, Impact Assessment Overview](https://medium.com/data-science-at-microsoft/responsible-ai-in-action-part-2-complete-an-impact-assessment-9b792409e8dbv)
2. [Trustworthy AI, Impact Assessment Guidebook](https://blogs.microsoft.com/wp-content/uploads/prod/sites/5/2022/06/Microsoft-RAI-Impact-Assessment-Guide.pdf)
3. [Trustworthy AI, Impact Assessment Template](https://blogs.microsoft.com/wp-content/uploads/prod/sites/5/2022/06/Microsoft-RAI-Impact-Assessment-Template.pdf)
4. [Trustworthy AI, Blueprint Series](https://www.youtube.com/watch?v=cXmybztbvAM)