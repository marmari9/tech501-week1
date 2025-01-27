## cloud
# Cloud Computing Documentation

## Table of Contents
- [Cloud Computing Documentation](#cloud-computing-documentation)
  - [Table of Contents](#table-of-contents)
  - [How to Identify Cloud Services](#how-to-identify-cloud-services)
  - [Differences Between On-Prem and Cloud](#differences-between-on-prem-and-cloud)
  - [Cloud Deployment Models](#cloud-deployment-models)
  - [Types of Cloud Services](#types-of-cloud-services)
  - [Advantages and Disadvantages of the Cloud](#advantages-and-disadvantages-of-the-cloud)
    - [Advantages:](#advantages)
    - [Disadvantages:](#disadvantages)
  - [OpEx vs CapEx](#opex-vs-capex)
  - [Is Migrating to the Cloud Always Cheaper?](#is-migrating-to-the-cloud-always-cheaper)
  - [Market Share Trends](#market-share-trends)
  - [Top Cloud Providers](#top-cloud-providers)
  - [Cloud Cost Considerations](#cloud-cost-considerations)
  - [4 Pillars of DevOps](#4-pillars-of-devops)
  - [Case Studies](#case-studies)
  - [Takeaways and Reflections](#takeaways-and-reflections)
  - [SSh(secure shell):](#sshsecure-shell)

---

## How to Identify Cloud Services
- Accessible via the internet.
- Scalable resources that can grow or shrink on demand.
- Pay-as-you-go pricing model.
- Hosted and maintained by a third-party provider.

---

## Differences Between On-Prem and Cloud
- **Ownership**: On-prem is fully owned, while the cloud is rented from a provider.
- **Cost Model**: On-prem uses capital expenses (**CapEx**), while the cloud is operational expenses (**OpEx**).
- **Scalability**: On-prem is hardware-limited, while the cloud is virtually unlimited.
- **Maintenance**: On-prem requires in-house management, while the cloud is maintained by the provider.
- **Flexibility**: On-prem has limited flexibility compared to the cloud.

---

## Cloud Deployment Models
1. **Private Cloud**: 
   - Exclusive to one organisation.
   - Offers more control and security but incurs higher costs.
2. **Public Cloud**: 
   - Shared infrastructure.
   - Cost-effective and scalable but offers less control.
3. **Hybrid Cloud**: 
   - A mix of private and public cloud models.
   - Provides flexibility but requires complex management.
4. **Multi-Cloud**: 
   - Utilises multiple providers.
   - Avoids vendor lock-in but increases complexity.

---

## Types of Cloud Services
- **IaaS (Infrastructure as a Service)**: 
  - Provides virtual machines, storage, and networks.  
  - Examples: AWS EC2, Google Compute.
- **PaaS (Platform as a Service)**: 
  - Offers managed runtime environments for development.  
  - Examples: AWS Elastic Beanstalk, Heroku.
- **SaaS (Software as a Service)**: 
  - Fully functional software delivered over the internet.  
  - Examples: Gmail, Dropbox.

---

## Advantages and Disadvantages of the Cloud

### Advantages:
- Cost-efficient with a pay-as-you-go model.
- Scalable and flexible resources.
- Reduced maintenance effort with managed services.
- Global availability and disaster recovery options.

### Disadvantages:
- Potential security and compliance risks.
- Internet dependency may lead to downtime risks.
- Long-term costs may exceed expectations without optimisation.
- Complexities in migrating legacy systems.

---

## OpEx vs CapEx
- **CapEx (Capital Expenses)**: 
  - Upfront investment in physical assets, used for on-premises systems.
- **OpEx (Operational Expenses)**: 
  - Ongoing costs for services or subscriptions, commonly used for cloud systems.

---

## Is Migrating to the Cloud Always Cheaper?
- Not always cheaper due to hidden costs like bandwidth and support.
- Cost savings depend on optimised resource usage and proper planning.
- staff costs, utility, compare to the cloud.
---

## Market Share Trends
- **Amazon Web Services (AWS)**: Leading with approximately 32% of the market.
- **Microsoft Azure**: Holds around 23% market share.
- **Google Cloud Platform (GCP)**: Accounts for roughly 10% of the market.

---

## Top Cloud Providers
1. **AWS**: 
   - Known for its wide range of services and global reach.
2. **Microsoft Azure**: 
   - Focuses on enterprise integration and hybrid solutions.
3. **Google Cloud Platform**: 
   - Excels in data analytics and AI/ML tools.

---

## Cloud Cost Considerations
Costs typically include:
- **Compute**: e.g., virtual machines like EC2.
- **Storage**: e.g., S3 buckets, Glacier archives.
- **Networking**: e.g., data transfer fees.
- **Support**: e.g., different levels of service agreements.

---

## 4 Pillars of DevOps
1. **Culture**: Encourages collaboration using shared cloud environments.
2. **Automation**: CI/CD pipelines integrated with cloud services streamline deployments.
3. **Measurement**: Tools like CloudWatch and Datadog enable real-time monitoring.
4. **Sharing**: Centralised repositories and shared environments support collaboration.

---

## Case Studies
1. **Netflix**: Migrated to AWS to scale its streaming platform globally.
2. **Coca-Cola**: Used Azure for efficient supply chain management.
3. **Spotify**: Leveraged Google Cloud for enhanced music analytics.

---

## Takeaways and Reflections
- Migrating to the cloud is not always cheaper, but the flexibility it provides is invaluable for scaling businesses.
- Understanding **OpEx** vs **CapEx** was a key takeaway for me, as it highlights the financial shifts businesses experience when transitioning to the cloud.
- Hybrid and multi-cloud strategies can provide balance but require careful planning.
- DevOps principles are essential for leveraging cloud automation effectively.

---

## SSh(secure shell):

- Used to sign into Azure account 
- how to generate a private key using bash on local drive?
    - 1- create a .ssh file (ssh-keygen -t rsa -b 4096 -C "youremailaddress")
    - 2- write the name (eg. tech501-maram-az-key) 
    - 3- Keep the private key secret and add your public key to the VM when created. 
  -  ssh -i ~/.ssh/tech501-maram-az-key adminuser@20.254.68.12
