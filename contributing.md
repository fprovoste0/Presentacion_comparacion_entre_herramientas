### Visualización de nuestro Flujo

```mermaid
gitGraph
   commit id: "Inicio del proyecto"
   branch develop
   checkout develop
   commit id: "Setup del entorno"
   branch feature/limpieza-datos
   checkout feature/limpieza-datos
   commit id: "Script en Python"
   commit id: "Manejo de nulos"
   checkout develop
   merge feature/limpieza-datos
   branch fix/query-extraccion
   checkout fix/query-extraccion
   commit id: "Corrección de SQL"
   checkout develop
   merge fix/query-extraccion
   checkout main
   merge develop tag: "v1.0.0"
