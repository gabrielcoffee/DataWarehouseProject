# DataWarehouseProject

Project to extract data from commodities and show in an dashboard online.

```mermaid
flowchart TD;
    A[Start] --> B[Extract: buscar_dados_commodities(simbolo)]
    B --> C[Transform: Adiciona coluna 'simbolo']
    C --> D[Repeat para cada símbolo em lista: buscar_todos_dados(commodities)]
    D --> E[Concatena todos os DataFrames]
    E --> F[Load: salvar_banco(df)]
    F --> G[Salva no banco com to_sql]
    G --> H[End]

    style A fill:#cce5ff,stroke:#007bff,stroke-width:2px
    style B fill:#d4edda,stroke:#28a745,stroke-width:2px
    style C fill:#d4edda,stroke:#28a745,stroke-width:2px
    style D fill:#d4edda,stroke:#28a745,stroke-width:2px
    style E fill:#d4edda,stroke:#28a745,stroke-width:2px
    style F fill:#fff3cd,stroke:#ffc107,stroke-width:2px
    style G fill:#fff3cd,stroke:#ffc107,stroke-width:2px
    style H fill:#cce5ff,stroke:#007bff,stroke-width:2px
```