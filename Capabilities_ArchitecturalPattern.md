# The ABCDesEnt Architectural Pattern
This pattern is not primarily a template but rather a tool to measure, compare and judge work against, be it a use case, a process analysis or more elaborate design or architectural work.  

# How it works
tbd model here...
Mermaid syntax explained here: https://mermaid.ai/open-source/syntax/usecase.html
Mermaid editor: www.mermaideditor.io


# Overview Model
# Another model
```mermaid
flowchart LR
    Context[govern] --> UseCase[action] --> Capability[Publish]
```
```mermaid
flowchart LR
    UseCase[action] --> Capability[provide]
```
```mermaid
flowchart LR
    BusinessModel[reconciliate] --> Product[implement]
```

```mermaid

classDiagram
  
  direction TB

  class Context {
    +String organisation
    +String governance
  }

  Context <|-- UseCase
  Context <|-- Capability
  Context <|-- Product
  Context <|-- BusinessModel

```

```mermaid
classDiagram

  direction LR

  class UseCase {
    +String user
    +String outcome
  }
  class Capability {
    <<architectural form>>
    +String process
    +String asset
    +String employee
    +impact() action
  }

  UseCase "1" --> "1" Capability : realises

```

```mermaid

  classDiagram
  direction LR

  class Product {
    <<architectural structure>>
    +string system
    +string employee
  }
  class BusinessModel {
    +int income
    +int cost
    +revenue() balance 
  }
  Product "1" --> "1" BusinessModel

```


# Use Cases
```mermaid
usecase-beta
direction LR

actor Customer("Customer")
systemBoundary "Capability"
  Checkout("Outcome")
end
Customer --> Checkout

```
