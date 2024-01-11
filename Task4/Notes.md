# Notes MLOps
https://ml-ops.org/
## MLOps Principles
- best practices and tools to test, deploy, manage, monitor ML models in production
- strive to avoid technical debt in ml applications
### Iterative-Incremental Development
- MLOps includes, desingning the ml application, model development/experimentation, ml operations
- all phases are interconnected and can influence each other
1. business and data understanding, design the softwareproduct, define ML Use Cases and prioritze them
2. implement POC for different models and indentifiy, polish the suitable ML algorithm -> goal is to deliver a stable ML Product for production
3. use DevOps practices such as testing, versioning, CI/CD, monitoring and deliver developed Model to production
### Automation
- objective MLOps team is to automate deployment of ML models into core software system or as a separate component
- pipelines with no manual intervantion
- automated testing in pipelines  
3 Levels of automation:
1. manual process - experimental phase in which every ML workflow step gets exectued manually 
2. ML pipeline automation - automation of model training, trigger model retrain pipeline whenever new data is available
3. CI/CD pipeline automation - perform ML model deployments in production, build, test and deploy data, ml model and ml training pipeline components  
### Continuous Deployment
- provides orchestration, logging, monitoring and notifications to ensure that the ML models, code and data artifacts are stable
- CI - testing and validation code and components by adding testing and validating data and models
- CD - auto deploys the ML model prediction service when changes happen to training data or code
- CT - auto retrain ML models and re-deploy when new training data arrives
- CM - monitoring production data and model performance metrics
### Versioning
- use VCS for versioning of Ml training scripts, models and data sets
- use classic VCS processes for every new ML model specification like code reviews
- track experiments, different models etc in different dedicated branches 
### Testing
- different types of tests: tests for features and data, tests for model development and tests for ML infrastructure
#### Features and data tests
- data validation: automatic check for data and feature schemas
- importance tests to understand whether new features add a predictive power
  - compute correlation matrix
  - use subset of features
  - drop out unused features
- features and pipelines should be policy-compliant
- feature creation code should be tested by unit tests
#### Tests for reliable model development
- testing ml training, calc loss metrics, verify that algorithms make decisions aligned to business objective
- model staleness tests, stale = model doesnt include up to date data and doesnt satisfy the business requirements
- compare model performances
- validate performance of a model
- Fairness/Bias/Inclusion testing for model performance
- unit testing for ML model code
#### ML infrastructure test
- training a model should be reproducible, traing on the same data should produce same results
- minimize non-determinism in models
- stress testing of ML API and test algorithmic correctness with unit tests
- whole ML pipeline should be tested with a automated test that regulary triggers
- test that ml model get successfully loaded in production 
### Reproducibility
- every phase in this process should create an identical result given the same input
### Monitoring
- when model is deployed, monitor that model performance is as expected
- dependency changes and performances
- data schema and alert if schemas dont match
- stability of the model, can the model handle nans or infinites
- how old is the model in production, older models tend to decay in performance
- computational performance of ml system, notify if slow computational performance

## MLOps and model governance
- both processes are thightly interwoven
- MLOps is the equivalent to DevOps in software engineering, but specific for ML models
- setting up ML pipelines reduces the amount of time required to bring models into production
- companies need to: control access, put guidelines and legal requirements into practice, track interactions with ML models and results, document foundation of an ML model (stakeholders, business context, training data, features, guidlines for model reproduction, parameters, results) -> this is called model governance

### Model governance
- problem: companies fail to bring models into compliance with legal requirements
- risk category of AI determines the scope of regulations
    - unacceptable risk: endangers humans, security, livelihoods -> is forbidden (social scoring systems)
    - high risk: need to be robust, secure, accurate, should have high-quality training data, should be transparent and unbiased, need to be monitored by humans (credit scoring systems)
    - limited risk: needs to be transparent (chat bots, bot user need to be informed that they are interacting with AI)
    - minimal risk: not subject to any regulation (spam filters)
- model governance should also ensure quality of a ML system -> company cant sell bad systems
- reproducibility must be established and the model should be validated
- Observation, Security, Control: logging, metrics and auditing, cost transparency, model usage reports 
- key metrics should be continously monitored, if performance losses are detacted alerts should be sent 
- model service catalog: internal ui which shows users relevant metadata for a models
- security is important: Authentication, SSO, and role-based access control, models should also secure training data and information
- model governance should be a part of model management: final supervisory authority to approve a model for being deployed
- versioning of all models to create transparency for stakeholders
- comprehensive model documentation or reports

### Integration of Model Governance and MLOps
- determined by: strength of regulations and number of models that need to be in a software system
- more models lead to bigger importance of MlOps
- many models and strict regulation: model governance and MLOps are equally important
- many Models and little regulation: model governance weaker than MLOps and part of it
- few models and little regulation: model governance is optional, but still a good practice
- few models and strict regulation: model governance strong MlOps weak
- important to integrate model governance into every step of the ML life cycle 

## MLOps Stack
- defines language, framework, platform and infrastructure
- MLOps is hard, its still evolving and in its early stages
### MLOps Stack Canvas
- ensure models have a business impact
- planning cost of infrastructure: data and code management, ml model management and metadata management
- planning MLOps costs: CI/CD Tools and Assets, monitoring, alerting
- design ML system to fulfill: reproducibility, reliablity, efficency
### Components of MLOps Stack
#### Value Proposition
- central component outlining why customers benefit from the ML system
#### Data Sources and Data Versioning
- focus on estimating costs for data acquisition, storage, and processing.
#### Data Analysis and Experiment Management
- tasks related to translating business objectives, running experiments, and implementing proof of concept
#### Feature Store and Workflows
- feature engineering for ML model development
- feature store implementation and associated workflows
#### Foundations (Reflecting DevOps)
- inventory of available DevOps infrastructure and principles in ML projects
#### CI/CD: ML Pipeline Orchestration
- CI/CD pipelines for ML model releases
- introduces continuous training as a unique property for ML systems
#### Model Registry and Model Versioning
- essential for model evaluation phase
- ML model versioning and registry considerations
#### Model Deployment
- deploying ML models and continuous deployment strategies
#### Prediction Serving
- deals with ML model serving in batch or online modes
#### ML Model, Data, and System Monitoring
- constant monitoring to ensure model quality
- metrics and aspects to monitor for ML systems in production
#### Metadata Store
- component for metadata management in ML projects
### Dilemmas of MLOps:
- organizational aspects related to tooling, platforms, and skills in MLOps components
- architecture decision records recommended for documenting MLOps architecture
### MLOps Maturity Level:
- three phases of AI Readiness (Tactical, Strategic, Transformational)
- MLOps practices and infrastructure depend on AI Readiness level
