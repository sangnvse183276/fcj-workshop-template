---
title: "Blog 1"
date: "2025-09-09T19:53:52+07:00"
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---
{{% notice warning %}}
⚠️ **Note:** The information below is for reference purposes only. Please **do not copy verbatim** for your report, including this warning.
{{% /notice %}}

Unlock generative AI capabilities with DataRobot from AWS Marketplace
by Shun Mao, Luke Shulman, and Nathaniel Daly on 20 DEC 2024 in Amazon Bedrock, Amazon Machine Learning, Amazon SageMaker, Amazon SageMaker Autopilot, Amazon Titan, AWS Marketplace, Generative AI, Intermediate (200) Permalink  Share
Generative AI has been a central topic in the technology space since late 2022. However, with the introduction of many more new large language models (LLMs) and the identification of issues such as hallucination, limited context window length, prompt engineering, and cost, the generative AI community has realized that more features and functionalities should be added to use LLMs safely and efficiently in an enterprise environment.

These combined complexities have made it challenging for enterprises and organizations to quickly embrace generative AI. Such challenges include lacking generative AI expertise and staff, having no framework to evaluate different models, lacking model deployment mechanisms, not knowing how to implement guardrails and monitoring for LLMs or how to combine traditional predictive AI with generative AI, and more. Overall, enterprises and organizations need a consolidated tool that can tackle these challenges while requiring minimal AI expertise and an affordable budget.

DataRobot, an AWS Partner and AWS Marketplace seller, provides a solution to address these challenges. DataRobot is a complete AI lifecycle platform that offers both predictive and generative AI capabilities with a low-code no-code (LCNC) design to help enterprises and organizations deliver business value and drive innovation with AI at a faster pace. DataRobot has achieved AWS Competencies in ML, data and analytics, and financial services, and holds the AWS Service Ready Specialization for Amazon SageMaker. DataRobot offers various deployment types, including multi-tenant software as a service (SaaS) built on AWS, single-tenant SaaS, and Amazon Virtual Cloud (Amazon VPC) deployment to meet the requirements of different companies and industries.

This post is going to introduce the overall architecture of DataRobot AI Platform and also demonstrate how you can build a GenAI application, from LLM selection, prompt testing and model evaluation to Retrieval Augmented Generation (RAG), LLM monitoring and guardrails. Everything has been combined into one unified DataRobot AI platform with a streamlined user experience.

Solution overview
DataRobot’s SaaS platform is built entirely on AWS with a modernized Kubernetes design, providing customers with robust, scalable, and trustworthy AI solutions. AI projects start with data ingestion, where DataRobot provides secure integrations to a wide selection of data sources, such as Amazon S3, Amazon Athena, and Amazon Redshift, as well as data stores from other providers like Snowflake. The following diagram shows the high-level architecture of the solution.

Overall architecture diagram of DataRobot’s SaaS
Figure 1: Overall architecture diagram of DataRobot’s SaaS

For predictive AI, you can use DataRobot to store, view, transform, and analyze your data with minimal data science knowledge in just a few clicks. These capabilities are backed by a powerful data processing engine. After data preparation, DataRobot uses its expertise in AutoML, which runs parallel ML training jobs on multiple selected high-quality ML models and all necessary feature processing steps automatically. Trained models are ranked in an integrated leaderboard with detailed information about each model, such as accuracy, feature importance map, receiver operating characteristic (ROC) curve, processing recipes, and prediction explanations. You can deploy your models within DataRobot or to other platforms, such as Amazon SageMaker or Snowflake, within minutes after selecting the best model.

For generative AI, DataRobot provides an LLM playground, a space where you can create and interact with LLM blueprints using different leading LLMs, including Anthropic’s Claude in Amazon Bedrock, and Amazon Titan models. The playground has integrated preselected vector databases to let customers to build chat or RAG applications without deep ML expertise. Different LLM blueprints can be created and compared side by side for prompt testing. Various preselected LLM evaluation metrics and custom metrics can be chosen and deployed to monitor the performance of LLMs, which is crucial for enterprise and organizational LLM adoption. After testing the LLM blueprint and deciding on the prompt and metrics, customers can move it into deployment for production.

For both predictive and generative AI, DataRobot equips the models with monitoring tools that are quick to set up. The platform can monitor many preselected metrics as well as custom-designed metrics, such as service health, latency, token size, error rate, and cost. For generative AI, DataRobot provides guardrails to help prevent prompt injection, sentiment and toxicity classification, personal identifiable information (PII) detection, and more.

In the following sections, we demonstrate the major steps on how you can easily build a predictive and generative AI application in DataRobot.

In the walkthrough, you learn how to:

Connect to data in Amazon S3 and create a data wrangling recipe to prepare the data
Build a predictive model within DataRobot and deploy it to Amazon SageMaker
Create an LLM blueprint that combines Anthropic’s Claude in Amazon Bedrock with grounding data
Evaluate and optimize the blueprint against metrics such as Recall-Oriented Understudy for Gisting Evaluation (ROUGE), faithfulness, and confidence
Package the LLM blueprint with guardrails to maintain safety and performance
Launch an AI app that can predict NBO and automatically generate email outreach
Prerequisites
Before getting started, make sure you have the following prerequisites:

An AWS account with access to Amazon Bedrock models
A DataRobot account. DataRobot can be purchased through AWS Marketplace. You can also visit the DataRobot site to request a free trial.
Solution walkthrough: Build a predictive and generative AI application powered by Anthropic’s Claude models in DataRobot
The use case we demonstrate here is to create a next best offer (NBO) email campaign where the goal is to proactively reach out to customers likely to churn and provide them with an offer that will help retain them as customers.

We use a predictive model to recommend the NBO for each customer and then use generative AI to customize the email for each customer.

Step 1: Connect the data source in Amazon S3
In DataRobot Workbench UI, we can start a new Use Case and add NBO data by connecting to an Amazon S3 bucket. The NBO data is prepared in-house based on the public IBM telco customer churn dataset.
Make changes to this dataset by adding another text-based column named “customer plan” and changing the prediction target from Churn Value to Next Best Offer. This change turns the prediction to be a multi-class classification problem. This was derived by applying some common-sense business rules to the reason codes from the original data. Meanwhile, we can create new columns to track how long customers have been on the phone with customer service, providing a key feature for our prediction.
Use DataRobot’s data wrangler to create a wrangling recipe with a sample of data and then apply it to the full dataset.
Add input data from Amazon S3 in DataRobot UI
Figure 2: Add input data from Amazon S3 in DataRobot UI

Step 2: Create a predictive model for the NBO
Once the data preparation is done, we can train a predictive model to predict which type of offer is best suited for a customer in order to avoid churning. To do that, we follow these steps:

In DataRobot Workbench UI, start an experiment for model training.
For the multiclass type, select Offers as the prediction target.
Run Autopilot Register to train a few ML models. Training will take place automatically with preprocessing steps designed uniquely for each different model. All the processing recipes can be viewed in the UI, shown as blueprint, so customers can view what’s really happening before the actual model training. This is shown in the following screenshot.
Blueprint for modeling and processing recipes
Figure 3: Blueprint for modeling and processing recipes

These recipes can finish in minutes given the small size of the tested datasets. When you deploy the model, you can directly deploy it within DataRobot without worrying about the underlining infrastructure. You also have the option to deploy it into Amazon SageMaker with one-click deployment, as shown in the following screenshot. This provides great flexibility for choosing deployment infrastructure.

SageMaker one-click model deployment within DataRobot]
Figure 4: SageMaker one-click model deployment within DataRobot

Step 3: Create the LLM blueprint
Once we have finished deploying the predictive model, we can build the generative AI part of the application, which is a RAG setup. Several market leading LLMs are already available in the DataRobot’s LLM playground, such as Anthropic’s Claude from Amazon Bedrock and the Amazon Titan model, as well as models from other providers, giving customers a great choice in selecting the right model for their applications.

Navigate to the LLM playground from DataRobot Workbench and create an LLM blueprint by picking the Claude 3 model as the LLM from the drop-down list. After the model has been selected, several LLM related parameters can be adjusted to tune the results, such as Max completion tokens, Temperature and Token selection probability cutoff.
On the same page, vector databases and system prompts can be configured to work with the LLM. At this time, users can try different combinations of LLM, chunking strategy, and prompting strategy to derive an optimal result.
Users can build multiple blueprints and compare them against different metrics such as ROUGE, confidence, and faithfulness. The data we used to send to the vector database is a collection of five internal plan documents discussing various details of the cell phone plans.
The following screenshot shows the LLM playground UI.

DataRobot LLM playground UI
Figure 5: DataRobot LLM playground UI

Step 4: Set up LLM guardrails
Once the LLM blueprint has been created and tested, choose the LLM blueprint actions and then choose Send to model workshop.
In the model workshop, adjust the runtime environment variables as needed. The Evaluation and moderation section contains metrics that you can pick to evaluate the model performance and safety over time. DataRobot provides some of the ready-to-use metrics to get started, such as PII detection, sentiment analysis, toxicity, and more. In addition, you can design your own custom metrics based on your unique business logic.
After you complete all the configurations, you can test the model or create new versions. DataRobot recommends testing it before deployment.
Next, choose Register model, provide the registered model or version details, and then choose Register model again to add the LLM to the Registry. The registered model version opens in the Model directory, which contains the Deploy button for users to quickly deploy the model.
DataRobot model workshop UI
Figure 6: DataRobot model workshop UI

LLM evaluation metrics available in DataRobot
Figure 7: LLM evaluation metrics available in DataRobot

Step 5: LLM deployment options
As in the predictive model, you can deploy your LLM models within DataRobot or into other third-party platforms, such as Amazon SageMaker or Amazon Elastic Kubernetes Service (Amazon EKS). Here we use DataRobot one-click deployment to deploy the model to Amazon SageMaker. Once deployed, we can monitor the performance of both the generative and predictive portions of the app. You can create custom metrics like latency, return on investment (ROI), or readability, which can be viewed under the same pane of glass, no matter whether those models are built in DataRobot, on AWS, or elsewhere. This is shown in the following screenshot.

Metrics monitoring dashboard
Figure 8: Metrics monitoring dashboard

Step 6: Host application in DataRobot
With the predictive and generative models deployed, we can build a web application by utilizing both models and host the application within DataRobot. DataRobot supports hosting custom applications in a variety of frameworks, such as Streamlit, Shiny and Flask. For detailed information on hosting custom applications in DataRobot, please refer to the Create custom applications article in the DataRobot documentation. Here, as an example we use python to build a simple web application with Streamlit. The interface of the application is shown in figure 9. The application picks a customer by name and predicts whether the customer will need a certain type of offer or not to avoid churn. The result of this part is derived from the response of the predictive model we deployed. If it determines the customer needs an offer, the app will leverage the generative model we deployed previously to generate an example email campaign with a purposely curated offer based on the customer’s unique situation. After that, the marketing team can send the email to the customer.

Example application that combines both predictive and generative AI
Figure 9: Example application that combines both predictive and generative AI

Cleanup
To clean up the resources created in this walk-through, follow these steps:

On the AWS console under the SageMaker panel, remove the SageMaker deployments by deleting the SageMaker endpoints and endpoint configurations.
In the DataRobot UI, remove all DataRobot deployments.
There are no additional consumption costs for the DataRobot LLM playground or predictive experiments.

Conclusion
DataRobot is a comprehensive AI platform for teams to derive values from AI at faster speed. For companies and organizations of different sizes, DataRobot can help you build and deliver end-to-end generative and predictive AI solutions for your business, offering choice, flexibility, and top-of-the-line components. With the collaboration and tight integrations between DataRobot and AWS, customers can also build their applications by combining the capabilities of the two. To get started with DataRobot, visit

AWS Marketplace. To learn more examples of how DataRobot can help you in the generative AI space, refer to the DataRobot GenAI Delivered demos.

About Authors

Shun Mao
Shun Mao is a senior partner solutions architect in the artificial intelligence and machine learning (AI/ML) independent software vendor (ISV) partner team at Amazon Web Services. He has years of experience in data science, analytics, AI, and cloud across different industries, including oil and gas and pharmaceuticals. At AWS, he is helping strategic AI/ML partners to build novel products and solutions to bring business value to customers. Outside of work, he enjoys fishing, traveling, and playing ping-pong.


Nathaniel Daly
Nathaniel Daly is a principal product manager at DataRobot focusing on the development of predictive and generative AI solutions. He’s focused on bringing advances in data science to users such that they can use this value to solve real world business problems.


Luke Shulman
Luke Shulman is a lead data scientist at DataRobot. Luke has over 12 years of experience in data analytics and data science. Prior to joining DataRobot, Luke led implementations and was a director on the product management team at Arcadia.io, the leading healthcare SaaS analytics platform and at N1Health. At DataRobot, Luke is working with a number of Fortune 100 companies using DataRobot. He is also an active contributor to the DrX extensions to the DataRobot API client focusing on model evaluation and MLFlow integration. An avid champion of data science, Luke has also contributed to projects across the data science ecosystem including Bokeh, Altair, and Zebras.js.
