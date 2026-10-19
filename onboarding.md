# Onboarding

Welcome to the technical architecture practice within Schools Digital

Principles

- Work in the open
- Favour commodity solutions

## FAQ

### Diagramming

Use Mermaid for technical documentation, use the C4 templates. A C4 container diagram maps to a high-level design diagram, a C4 component diagram to a low-level design diagram. The low-level diagram can be supplemented with a C4 deployment diagram if you want more detail on the infrastructure components.

For threat modelling A data flow diagram (DFD) 0 maps to a C4 system diagram and the C4 container diagram can be substituted for the DFD 1 diagram so don't generate more variants than are necessary.

Many teams use Lucid as an interactive diagramming tool so if you're in a team doing that then feel free to make use of it. However regard Lucid canvases as ephemeral and make sure the information is present in a Github repo in an open format if it is being repeatedly referred to.

Otherwise use Excalidraw for general diagramming and visualisation and make sure to check your canvases into a repo that is either publically available or accessible by the other architects in the portfolio.

### Infrastructure and designs

The portfolio uses Azure Kubernetes Service (AKS) as its main deployment platform and makes as much use of open Kubernetes components as possible over proprietary technologies. Designs should be broken down into standard Kubernetes patterns like Application and Job.

When the application is deployed on the platform it integrates with platform solutions for logging, alerting, notifications, dashboards, integrations with SEIM, metrics and error reporting. Don't reinvent the wheel here, consult with Infrastructure before adding new or duplicate systems.

Check your cloud costings with the Infrastructure team to see if we need to consult with FinOps with any changes to our reserved capacity.

Data warehousing

The portfolio has a pattern for integrating transactional data into the portfolio data warehouse, this is different to the rest of the department as it uses GCP. When you need to integrate initiate the process via the Data and Insights Teams channel.

Commodity technology

In your designs, favour Postgres as a datastore, Kubernetes as infrastructure functionality, REST as a protocol, JSON as an exchange format.

When considering adding a technical capability to services it is important that the capability can be sourced from at least two suppliers. If it is something that cannot be substituted easily it should be recorded as a risk.
