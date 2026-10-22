# The ABCDesEnt Architectural Pattern
This pattern is not primarily a template but rather a tool to measure, compare and judge work against, be it a use case, a process analysis or more elaborate design or architectural work.  

# How it works
tbd model here...
Mermaid syntax explained here: https://mermaid.ai/open-source/syntax/usecase.html
Mermaid editor: www.mermaideditor.io


# Model
```mermaid

classDiagram
  class Customer {
    +String name
    +String email
  }
  class Order {
    +String id
    +Date placedAt
    +total() Money
  }
  class LineItem {
    +int quantity
  }
  class Payment {
    <<interface>>
    +authorise() bool
  }
  Customer "1" --> "*" Order : places
  Order "1" *-- "*" LineItem : contains
  Order --> Payment : settled by

```

# Another model
```mermaid
flowchart LR
    A[Write] --> B[Preview] --> C[Publish]
```

# And another model
```mermaid
usecase-beta
direction LR
actor Customer("Customer")
systemBoundary "Order system"
  Checkout("Place order")
end
Customer --> Checkout
```
