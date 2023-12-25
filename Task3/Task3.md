# Exercise Data Mesh

When I visited datamesh-manager.com, I noticed a comprehensive and visually appealing platform for the management and analysis of data meshes. The system is designed to document and handle data products and associated contracts, providing detailed insights into the relationships between data products, metrics, data contracts, and governance.

## Data Mesh Map Overview 
The platform allows users to visualize various data sources and products from which data originates, along with other products that utilize this data. It provides detailed information on input and output ports, showcasing the different types of relationships with data contracts and showing how data is ingested into other data products and transferred between them.

## Data product details
We can view metrics for each data product, including costs, compliance policies, and consumer information or define new and custom metrics. The manager also displays input and output ports for each data product, revealing data contract details. These contracts outline terms of usage, schema, data examples, and data quality specifications. This feature shows how data will be exchanged between different domain teams and data products.  
The platform provides a view of relationships between data products, showcasing state and contracts with other domain products. We can manage, approve, or reject these contracts.  
Under the *Teams* menu, we can see all teams and their members, assign roles, and manage related tasks and compliances. The system supports the creation of new teams, categorized into domain teams, platform teams, enabling teams, and governance groups. Domain teams own data products, platform teams provide domain-agnostic platforms, enabling teams help domain teams implement a data-driven structure and data contracts. The governance group is a collection of representatives for governance and compliance purposes, which also make decisions on standardized policies. This hierarchical structuring allows data-driven team management, ensuring that teams are appropriately equipped to handle specific aspects of data governance.  
The platform offers the ability to set global policies and create associated TODO lists. These lists track the progress of policy implementation and also provide a process for accepting or rejecting policies. This centralized governance approach ensures that data management aligns with organizational policies and standards.

All specifications of data contracts and products can be created, modified and exported in a standardized YAML. This makes it possible to understand or export these data contracts without using the data manager tool.

## Conclusion
In conclusion, the Data Mesh Manager presents a solution for the governance of data meshes. Its features cover the spectrum of data management, from visualizing data flows and relationships to managing teams, contracts, and policies. The platform's demo and visualization demonstrate what a well-implemented data mesh can look like. Data meshes are an structure for organizations seeking control of their data ecosystems in a decentralized way.

<br>
<br>

# Notes about data meshes
## Data Mesh
- domain oriented decentralization for analytical data
- shift tasks from the central data team to domain teams
- platform and enabling team to support domain teams

## What is a data mesh?
- domain ownership
   - move data ownership away from central data team to domain teams	 
- data as a product
   - there a consumers for domain teams data in other domains
   - domain data should be treated like every other public api
- self serve data infrastructure platform
   - the central data team gets a dedicated data platform team
   - provides tools, functionality and systems to domain teams to managedata
- federated governance
   - standardize all data products to organization rules and industryregulations

## What is a Data Mesh?
- domain ownership
  - move data ownership away from the central data team to domain teams
- data as a product
  - there are consumers for domain team data in other domains
  - domain data should be treated like any other public API
- self-serve data infrastructure platform
  - the central data team is now a dedicated data platform team and enabling team
  - provides tools, functionality, and systems to domain teams to manage data
- federated governance
  - standardize all data products to organization rules and industry regulations

## How to Design a Data Mesh?
- every domain manages its own data
- can publish data contracts to serve other domains data needs with its data.
## Terminology
### Data Product
- Contains components to process and store domain data for domain use cases.
- Can serve data with output ports to others, and how the data is structured is defined in a data contract.
### Data Contract
- Document that defines the product provider, structure (schema), format, semantics, quality, and terms of usage
- is used when data is exchanged between different teams
- can be specified by standardized YAML
### Federated governance
- representatives of each domain, decide global boundaries and policies
### Transform
- preprocess data into small entities
### Ingesting 
- as etl or from workflows with batches
- clean data (every domain team is responsible for its data)
### Data platform
- automate policies
- provides and defines query engine/languages
### Enabling team
- enables team to manage its own data (learning material, consultancy)
### Mesh
- mesh emerges when teams use other domains data products 