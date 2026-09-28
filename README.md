```metmaid
flowchart TD
    A([Inicio]) --> B[Abrir aplicación]
    B --> C[Registrar hora de entrada]
    C --> D{¿Entrada antes de las 08:00?}
    D -->|Sí| E[Registrar coordenadas de acceso]
    D -->|No| F[Registrado y Advertencia]
    E --> G{¿Está dentro del área de trabajo hasta 50m?}
    G -->|Sí| H[Registrado y OK]
    G -->|No| F
    H --> I([Fin])
    F --> I

    classDef ok fill:#28a745,color:#ffffff,stroke:#1e7e34,stroke-width:2px;
    classDef advertencia fill:#dc3545,color:#ffffff,stroke:#a71d2a,stroke-width:2px;

    class H ok;
    class F advertencia;
```
