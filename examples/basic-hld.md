# Basic high-level architecture diagram

These are used for Alpha assessment outputs and to give a basic orientation to the application you're working on.

Don't include anything that isn't part of the service being described.

```mermaid
flowchart LR

    User[User]
    
    subgraph SDIP["Common Infrastructure Platform"]
        direction LR
        WebApp[Web application]
        Postgres["Datastore<br>(Postgres)"]@{ shape: cyl}

        WebApp --> Postgres
    end

    User --> WebApp

    style SDIP fill:none,stroke:blue,stroke-width:2px
    style User fill:gainsboro,color: black
```