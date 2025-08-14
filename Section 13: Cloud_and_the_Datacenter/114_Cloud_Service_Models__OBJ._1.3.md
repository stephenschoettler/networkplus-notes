## 💡 Cloud Service Models (OBJ 1.3)

This section covers cloud service models, which represent different levels of responsibility shared between the cloud provider and the user. Think of it as a "stack" where each layer builds upon the one below it.
**Key Takeaway:**
- **SaaS:** You use the application.
- **PaaS:** You build your application on their platform.
- **IaaS:** You manage your own operating system and applications on their infrastructure.
- The further down the stack you go (from SaaS to IaaS), the more control you have, but also the more responsibility you bear.

✅ **On-Premise vs. Hosted Solutions**
- **On-Premise:** Organization owns and manages all hardware, software, and facilities. Offers high control but is costly and requires significant personnel.
- **Hosted (Cloud):** A third-party service provider owns and manages the underlying infrastructure, offering services in a multi-tenancy environment. Reduces cost and administrative overhead but requires careful consideration of security, redundancy, and data location.

✅ **The Three Main Cloud Service Models**
- **1. SaaS (Software as a Service):**
  - **What it provides:** The provider manages everything: hardware, software, operating system, middleware, runtime, data, and the application itself.
  - **User Responsibility:** Users only interact with the application via a web browser or client.
  - **Analogy:** Like a fully prepared meal delivered to your door.
  - **Examples:** Office 365, Google Workspace (Docs, Sheets), TurboTax, QuickBooks Online, Salesforce.
- **2. PaaS (Platform as a Service):**
  - **What it provides:** The provider manages the hardware, operating system, middleware, and runtime environment.
  - **User Responsibility:** Users are responsible for developing and deploying their own applications/code and managing their data.
  - **Analogy:** Like a fully equipped kitchen with ingredients; you cook the meal.
  - **Examples:** AWS Elastic Beanstalk, Google App Engine, Heroku. Ideal for developers who want to focus on coding without managing the underlying infrastructure.
- **3. IaaS (Infrastructure as a Service):**
  - **What it provides:** The provider manages the fundamental computing infrastructure: networking, storage, servers (physical and virtualized), and virtualization layer.
  - **User Responsibility:** Users are responsible for installing and managing the operating system, middleware, runtime, applications, and data.
  - **Analogy:** Like an empty kitchen with utilities; you bring everything else (appliances, ingredients, cook).
  - **Examples:** Amazon EC2, Microsoft Azure Virtual Machines, Google Compute Engine. Offers the most control over the infrastructure.