---
title: "Blog 3"
date: "2025-09-09T19:53:52+07:00"
weight: 1
chapter: false
pre: " <b> 3.3. </b> "
---
{{% notice warning %}}
⚠️ **Note:** The information below is for reference purposes only. Please **do not copy verbatim** for your report, including this warning.
{{% /notice %}}

Databricks modernizes healthcare data on AWS
by Venkat Viswanathan, Amandip Kaler, Harrison Holstein, and Vaishali Gohel on 13 MAY 2025 in Amazon AppFlow, Amazon Bedrock, Amazon EC2, Amazon Kinesis, Amazon Nova, Amazon Simple Storage Service (S3), Amazon Titan, AWS Database Migration Service, AWS Glue, AWS Identity and Access Management (IAM), AWS Key Management Service, AWS Marketplace, AWS PrivateLink, AWS Trainium, Graviton Permalink  Comments  Share
This post is co-written with Rebecca Nissan, Sr. Delivery Solutions Engineer, Healthcare and Life Sciences, Field Engineering, Databricks.

In today’s healthcare data-centric landscape, organizations face challenges (such as disparate data silos) across their electronic health records (EHRs), medical imaging, and other on-premises data warehouses. Healthcare data is growing at such a rapid rate that one study observed the healthcare industry is growing faster than other verticals and contributes approximately 30 percent of the world’s data volume today.

As a result, organizations need a secure and easy-to-use data platform in order to centralize and utilize the data efficiently. Databricks on Amazon Web Services (AWS) offers a unified data and analytics platform that breaks down these data silos and integrates the data engineering capabilities of Databricks with the secure and reliable infrastructure of AWS.

We will walk through how Databricks and AWS, together, can help address large data silos to transform personalized patient care through generative AI and machine learning.

Industry challenges driving cloud data platform adoption
The healthcare industry is rapidly evolving in how it manages and utilizes data. The industry is increasingly adopting modern data architectures in order to keep up with the quickly changing landscape.

Let’s explore some of healthcare’s current data challenges:

Digital transformation in healthcare is driven by a shift away from fee-for-service models to value-based care (VBC) and outcome-based payments. Patient medical history, medical imaging, wearable health information, genomics, and other medical research data play a key role in driving better outcomes for patients. However, the data needs for executing on VBC strategies surpass the capabilities of legacy technologies and require modernization to meet the demands of the business.
On-premises data silos result in managing petabytes of data across multiple segments of the organization, which may be locked in different healthcare data modalities.
Personalized engagement requires the centralizing of a patient’s data in order to allow for precision medicine based on a patient’s health history and requirements.
AI-powered innovations with slow adoption rates hinders the ability to leverage more advanced automation of clinical documentation, and enhanced diagnostic accuracy through AI-assisted imaging. The adoption of generative AI for administrative tasks and patient risk predictions would also benefit patient care.
These are driving factors for healthcare customers beginning to adopt modern data strategies in the cloud. The scale and speed of innovation in the cloud enables customers to scale resources for peak times when needed and down-scale when not needed, leading to cost efficiency in storage and compute. Consolidation of data silos also leads to a reduction in the duplication of data—providing a single source of truth.

Databricks for healthcare
In today’s data-driven healthcare landscape, organizations need robust, secure, and scalable solutions to transform vast amounts of healthcare data into actionable insights. The Data Intelligence Platform from Databricks revolutionizes how organizations can use their data to improve patient outcomes.

Databricks serves as a unified open analytics platform for building complete data use cases on a data lakehouse, a term that combines data warehousing and data lakes under one technology. Founded by the creators of Apache Spark, this architecture leverages the scalable nature of cloud technology for storage, data processing, and AI while adding the structure, data governance, and business intelligence experience of traditional data warehouses.

AWS collaborates with Databricks to bring the powerful data lakehouse platform of Databricks together with the comprehensive cloud infrastructure of AWS. This collaboration provides healthcare organizations with a secure, scalable, and compliant environment for their critical data workloads—enabling innovation to drive improvements to patient care.

Why Databricks on AWS
Figure 1: High level architecture of data sources and outcomes of Databricks on AWS

Figure 1: High level architecture of data sources and outcomes of Databricks on AWS

Databricks on AWS provides a platform to unify the diverse ecosystem of data silos including all EHR data, medical imaging, laboratory systems, revenue cycles, pharmaceuticals, supply chain, clinical decision support, and more. The decision to run Databricks on AWS represents a strategic choice for healthcare organizations that unlocks tremendous value. It can help with predicting disease onset in real time in inpatient settings, and measuring patient safety metrics (like fall fractures). It can facilitate closing gaps of care with preventative screenings (reducing the length of stay and improving care treatment plans), and optimize provider performance in bundled payment arrangements to name a few.

There are several compelling technological advantages of Databricks with AWS.

Availability and reliability

The foundation of these advantages lies in the AWS global infrastructure, offering the highest availability and resiliency in the industry. Databricks on AWS is available in 13 AWS Regions and multiple Availability Zones per Region. This means healthcare organizations can deploy Databricks workloads with confidence, confirming business continuity and meeting stringent regulatory requirements for data residency and disaster recovery.

Giving customers simplicity and flexibility for generative AI

While Databricks simplifies the architecture with a lakehouse and accelerates speed to value, AWS provides powerful and flexible tooling. These enable healthcare organizations with unparalleled capabilities to build cutting edge research using generative AI, medical imaging, genomics, autonomous medical coding, drug research and discovery, and personalized treatment plans.

Databricks Mosaic AI Gateway supports serving models across all clouds, including those available in Amazon Bedrock which provides access to a choice of leading foundation models (FMs) through a single API. This includes Amazon Titan and Amazon Nova models as well as those from leading AI companies like Anthropic, AI21 Labs, Meta and more. Together, Mosaic AI Gateway and Amazon Bedrock give customers the flexibility and choice to utilize the right model for their use-case leveraging the broad selection of models available in Amazon BedRock in addition to the other models supported by Mosaic AI Gateway.

Databricks Mosaic AI provides complete connectivity and transparency between data and AI, powered by its native integration with Unity Catalog’s observability tools which enable improved model accuracy and spending oversight.

Furthermore, leveraging AWS Trainium and Inferentia chips enables organizations to optimize both training and inference costs while maintaining high performance.

Maximized return on investment and cost optimization

Healthcare organizations can leverage AWS Graviton processors, which offer up to 40 percent better price performance compared to traditional x86-based instances. The ability to utilize Amazon EC2 Spot Instances for Databricks workloads can reduce compute costs by up to 90 percent compared to on-demand pricing.

Spot Instances on AWS provide a two-minute interruption notice before termination, helping customers balance fault tolerance with cost optimization. This cost efficiency extends to data storage through intelligent tiering between Amazon Simple Storage Service (Amazon S3) storage classes and integration with AWS cost management tools. Healthcare organizations can maintain control over their technology spending while scaling their analytics capabilities.

Adopting Databricks on AWS also accelerates time-to-insights compared to building and maintaining a custom data analytics platform. Custom solutions require dedicated platform engineers and architects to build and support ongoing operational maintenance activities (such as patching, cluster optimization, and managing data ingestion pipelines). With Databricks on AWS, organizations can re-focus their in-house expertise to extracting value from their data rather than maintaining complex data architectures.

Security and compliance

Security and compliance capabilities are paramount for healthcare organizations. Native integration with AWS security services, including AWS Key Management Service (AWS KMS) for encryption key management, AWS PrivateLink for secure network connectivity, and AWS Identity and Access Management (IAM) for granular access control, make it straightforward for healthcare organizations to maintain HIPAA compliance and protect sensitive patient data.

The Databricks platform’s support for the AWS shared responsibility model provides clear delineation of security obligations, streamlining compliance audits and risk management processes.

For customers getting started on AWS, we recommend exploring the AWS Landing Zone Accelerator (LZA) for Healthcare. This AWS open-source solution helps you quickly deploy a secure foundation aligned with AWS best practices, specific to the healthcare industry, to set you up for success.

The combination of these advantages makes Databricks on AWS a strategic choice for healthcare organizations. Whether implementing precision medicine initiatives, optimizing clinical trials, or improving operational efficiency. The platform provides the technical capabilities, security features, and economic benefits needed to drive healthcare innovation forward.

Unlock your healthcare data with Databricks on AWS
Figure 2: Databricks on AWS for Healthcare reference architecture

Figure 2: Databricks on AWS for Healthcare reference architecture

The Databricks on AWS for Healthcare reference architecture begins with a secure landing zone through the AWS Landing Zone Accelerator for Healthcare. This serves as the foundation for integrating diverse healthcare data sources, including electronic health records, medical imaging, and genomics research.

Data integration is achieved through multiple pathways, including Databricks tools such as Auto Loader, Lakeflow Connect, and Structured Streaming, as well as AWS services like AWS Database Migration Service (AWS DMS), Amazon AppFlow, AWS Glue, and Amazon Kinesis. These services allow for both batch and streaming data ingestion into a data lakehouse.

The data is stored in the lakehouse, which is backed by Amazon S3. Medallion architecture from Databricks is utilized for data transformation and curation. Finally, the processed data can be integrated with various services, including Amazon Bedrock, providing API access to industry-leading foundation and large language models.

Once you have filtered, cleaned, and augmented both your structured and unstructured data you have production data—ready to be delivered to downstream users and applications. Databricks customers can take advantage of Delta Sharing, an open-source approach to securely share live data from your lakehouse to any computing platform, analytics and AI.

Key benefits of Delta Sharing include open cross-platform sharing (avoiding vendor lock-in), the ability to share live data without replication, and centralized governance with Unity Catalog. Delta Sharing enables you to integrate data with your preferred business intelligence (BI) and analytics tools (including Amazon QuickSight). From there healthcare customers can build reports, visualizations, and applications that unlock insights from data that was previously locked in data silos.

Summary
The combination of Databricks and AWS represents a powerful solution for healthcare organizations looking to transform their data analytics capabilities. We explored how this partnership delivers the security, scalability, and sophisticated analytics capabilities needed to drive innovation in healthcare while maintaining regulatory compliance and cost efficiency.

The future of healthcare analytics is here, and it’s powered by Databricks on AWS. Join the growing community of healthcare organizations that are leveraging this powerful combination to improve patient outcomes, accelerate research, and unlock your data to drive innovation.

Connect with Databricks or an AWS Representative for live demos and discuss how we can support your journey to a modern data architecture.

Ready to accelerate your healthcare organization’s data initiatives? Here are some ways to get started:

Try a 14-day free trial of Databricks by utilizing the streamlined deployment experience through the AWS Marketplace
Browse the Databricks Healthcare & Life Sciences Solution Accelerators to get started quickly on common use-cases
Visit AWS for Healthcare & Life Sciences to learn more about healthcare specific solutions
TAGS: Databricks
Venkat Viswanathan
Venkat Viswanathan
Venkatavaradhan (Venkat) Viswanathan is a Senior Solutions Architect at Amazon Web Services. Venkat is a Technology Strategy Leader in Data, AI, ML, and Advanced Analytics. Venkat is a Global SME for Databricks and helps AWS customers design, build, secure, and optimize Databricks workloads on AWS.

Amandip Kaler
Amandip Kaler
Amandip Kaler is a solutions architect for Healthcare at Amazon Web Services (AWS). He has a degree in computer engineering and supports healthcare organizations to modernize and achieve their missions.

Harrison Holstein
Harrison Holstein
Harrison is a Senior Solutions Architect supporting Global AWS Public Sector Independent Software Vendor partners. He has been with AWS for 6 years and enjoys working with partners to deliver joint solutions that help customers modernize their data strategy while maintaining their security and compliance objectives.

Vaishali Gohel
Vaishali Gohel
Vaishali Gohel is a Solutions Architecture Leader at Amazon with over two decades of experience in transforming healthcare organizations through innovative cloud technology solutions. She's a strategic technology executive specializing in large-scale cloud migrations and advanced data strategies using AI, ML, and generative AI. Vaishali handles consistently delivering solutions that drive business growth, enhance patient care, and improve operational excellence.