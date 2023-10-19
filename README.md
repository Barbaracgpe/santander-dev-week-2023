# Santander Dev Week 2023
Java RESTful API criada para a Santander Dev Week

## Diagrama de Classes

```mermaid
classDiagram
    class User {
        - name: String
        - account: Account
        - features: Feature[]
        - card: Card
        - news: News[]
    }

    class Account {
        - number: String
        - agence: String
        - balance: Float
        - limit: Float
    }

    class Feature {
        - icon: String
        - description: String
    }

    class Card {
        - number: String
        - limit: Float
    }

    class News {
        - icon: String
        - description: String
    }

    User "1" *-- "1" Account : has
    User "1" *-- "N" Feature : has many
    User "1" *-- "1" Card : has one
    User "1" *-- "N" News : has many
```

