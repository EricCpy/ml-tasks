# Exercise MLOps

## 1. What are the key principles of ml-ops?

MLOps has a set of principles which aim at managing the complete lifecycle of ML models. These principles, best practices and MLOps tools, ensure a transition from development to production models and strive to avoid technical debt in ML applications. These principles are Iterative-Incremental Development, Automation, Continuous Deployment, Versioning, Testing, Reproducibility, and Monitoring.

### Iterative-Incremental Development
MLOps follows an iterative-incremental development approach with a strong interconnection between the development phases. Starting with business and data understanding, during this process is for designing the software product, use-cases and prioritizing them. Next Model development and experimentation, this includes the implementation of Prototypes and Proof-Of-Concepts for various models and to identify the most suitable ML algorithms and models for the task. This should integrate with ML operations, which are using DevOps best practices for testing, versioning, CI/CD and monitoring. The goal of this is to deliver a stable ML product for production.

### Automation
The objective of this principle is to helper MLOps teams to automate depyloment of ML models into existing software systems or as separate components.  
There are three levels of automation, the lowest level of automation is to execute processes manual, this level is used during the experimental phase. The second level is to autmate these tasks into pipelines, these pipelines should trigger automatically to retrain the models when new data is available.
The last level is to create pipelines with no manual intervention, which also include automated testing and deployments to different environments.

### Continuous Deployment
Continuous Deployment in MLOps provides orchestration, logging, monitoring and notifications to ensure stability. The Continuous integration phase involves testing and validating code and components. Continuous deployment automatically deploys ML model prediction services when changes happen to training data or code. Continuous training and continuous monitoring focus on retraining ML models and redeploying them when new training data arrives, along with monitoring production data and model performance metrics.

### Versioning
To maintain consistency and track changes, version control systems should be used for ML training scripts, models and datasets. This should also include classic processes like code reviews for every new ML model specification. Additionally experiments and different models should be tracked in dedicated branches.

### Testing
MLOps integrates different types of tests for features, data, model development and ML infrastructure. Features and data tests should include schema validation and evaluate if new data can be used for a ML model. Tests for reliable model development include ML training verification, loss metric calculations, business requirement, fairness, bias and inclusion testing. This can be done with unit tests. ML infrastructure tests ensure reproducibility and minimize non-determinism. This can be done with stress-tests on ML APIs and integration tests which are regularly triggered for the entire ML pipeline.

### Reproducibility
Every phase in the MLOps process should yield identical results given the same input. This is crucial for reproducibility. This principle guarantees consistency and traceability across the ML lifecycle.

### Monitoring
Monitoring involves tracking model performance, detecting dependency changes, alerting on false data schemas, assessing model stability, monitoring if models are up to date with the newest data and evaluating computational performance and alerting on significant slow downs in the ML Pipelines.  
This principle can help MLOps teams to establish a robust workflow. It helps the team to keep track of the effectivnes of models and to maintain machine learning models in production environments.


## 2. What is model governance in the context of ml-ops and what would be the key points if you explain this to a CEO?
In machine learning and MLOps, model governance is the important for ensuring adherence to legal requirements and the overall success of ML models. When integrated with MLOps, it acts as a guiding framework for compliance and ethical considerations.  
MLOps and model governance are intertwined with MLOps serving as a DevOps for ML models. While MLOps speeds up model deployment, building and testing, model governance ensures control, legal compliance, interaction tracking and comprehensive data documentation.  
Aligning models with legal requirements, driven by the risk category of the AI is a challenge. Model governance can help us not only to ensure compliance but also guarantees the quality of the whole ML system. It covers reproducibility, validation, continuous monitoring of our models and security considerations such as authentication and access control for data and models.  
The integration of model governance and into MLOps depends on the strength of regulations and the number of models and machine learning products. In scenarios with many models and strict regulations, both are equally important. As the number of models or regulations decreases, the relative importance adjusts accordingly. But even with just a few models and minimal regulations, model governance remains a good practice to ensure the quality of our ML products.  
Recognizing the relationship between MLOps and model governance is crucial to have successful models. Together they form a robust foundation for compliance, quality and other legal requirements for the deployment of ML models in production environments.


## 3. As we had a CI/CD lecture: what is the connection between ml-ops and CI/CD?!
MLOps and CI/CD share the same objective, to streamline the development and deployment lifecycle. While CI/CD traditionally focuses on code integration, testing and deployment, ML-Ops extends these practices to machine learning models. Machine learning projects demand a set of specific requirements, from model training and validation to the deployment of ML pipelines.

### Connections

#### Automation
Both MLOps and CI/CD prioritize automation to reduce manual interventions, minimize errors and accelerate the overall development and deployment process. In CI/CD, automated testing and deployment pipelines ensure fast and reliable releases. Similarly ML-Ops employs automation for model training, testing and deployment, to ensure reproducibility and accelerate ML workflows.

#### Continuous Deployment
CI/CD aims to for the continuous delivery of software deployments to production environments. In MLOps this translates to the continuous deployment of machine learning models. Both help with a fast adaptation of changes, allowing us to stay responsive.

#### Versioning
Version control is a shared principle between CI/CD and MLOps. CI/CD relies on version control systems like git to keep track of code changes and ensure backups to old releases. In MLOps versioning extends beyond code to ML models and training data. This guarantees transparency, reproducibility and effective collaboration among developers.

### Differences
#### Deployments
In CI/CD the primary focus is on deployment of artifacts and packages. In MLOps the scope extends to ML models, datasets and with models associated metadata.

#### Testing
While traditional CI/CD testing involves unit tests and integration tests for code, MLOps adds new layers. Testing ML models includes not only code validation but also assessing model performance, data quality and compliance of business objectives.

## 4. Describe the MLOps infrastructure stack in two paragraphs!
The MLOps infrastructure stack includes planning costs, ensuring business impact and designing systems for reproducibility, reliability and efficiency. It addresses critical components like data sources, model registries, CI/CD for MLOps and continuous monitoring. The MLOps stack is essential for effective MLOps.

Data sources and data versioning are important for estimating costs for data acquisition, storage and processing. Data analysis and experiment management focus on translating business objectives into  experiments and implementing proof of concepts. The feature store and workflow components streamline feature engineering for ML model development. DevOps infrastructure needs to provide an inventory of tools, helping with versioning, collaborations and pipelines. ML pipeline orchestration adds continuous training to the standard CI/CD, ensuring up to date model releases. Model versioning is essential in the model evaluation phase to know which model delivered which results. ML model, data and system monitoring are crucial components for a working ML system and help to maintain model quality and monitor metrics. The metadata store is for managing specific ML model metadata. Launching ML softare solutions goes through three satges of ML maturity, a tactical, strategic and transformational phase. Overall the amount of MLOps practices and infrastructure components will depend on the organization’s ML maturity.
