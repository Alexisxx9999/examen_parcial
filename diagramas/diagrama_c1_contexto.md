# Diagrama C1 - Contexto del Sistema

Este diagrama muestra la interacción entre el usuario y el sistema principal, así como las dependencias externas.

# 🧩 Diagrama C1 - Contexto del Sistema

Este diagrama de contexto representa la visión de alto nivel del sistema **“Gestor de Finanzas Personales Asistido por IA”**, mostrando los actores principales, los sistemas involucrados y las interacciones clave entre ellos.

---

```mermaid
graph LR
    %% ==== Elementos ====
    U["👤<br/>Usuario de Finanzas Personales<br/><br/>Persona que interactúa con la aplicación<br/><br/>[Person]"]
    S["📱<br/>Sistema Principal<br/><br/>Aplicación móvil desarrollada en Flutter<br/><br/>[Software System]"]
    FB["🔥<br/>Firebase<br/><br/>Servicio externo para base de datos y autenticación<br/><br/>[Software System]"]
    GEMINI["🤖<br/>Google Gemini API<br/><br/>Servicio externo de inteligencia artificial<br/><br/>[Software System]"]

    %% ==== Relaciones ====
    U -->|"Registra transacciones,<br/>visualiza reportes y recibe recomendaciones"| S
    S -->|"Almacena datos financieros<br/>y realiza autenticación de usuarios"| FB
    S -->|"Clasifica transacciones<br/>y genera insights personalizados"| GEMINI

    %% ==== Estilos visuales (basado en Structurizr DSL) ====
    classDef person fill:#f4b400,stroke:#f4b400,stroke-width:6px,color:#000000,font-weight:bold
    classDef system fill:#ffffff,stroke:#007acc,stroke-width:6px,color:#007acc,font-weight:bold

    %% ==== Asignación de estilos ====
    class U person
    class S,FB,GEMINI system


## Descripción

Este diagrama de contexto (C1) representa la visión de alto nivel del sistema "Gestor de Finanzas Personales Asistido por IA" y muestra:

- **Usuario de Finanzas Personales**: Persona que interactúa con la aplicación
- **Sistema Principal**: La aplicación móvil desarrollada en Flutter
- **Firebase**: Servicio externo para base de datos y autenticación
- **Google Gemini API**: Servicio externo de inteligencia artificial

## Interacciones Principales

1. **Usuario ↔ Sistema**: Registro de transacciones, visualización de reportes y recepción de recomendaciones
2. **Sistema ↔ Firebase**: Almacenamiento de datos financieros y autenticación de usuarios
3. **Sistema ↔ Gemini API**: Clasificación automática de transacciones y generación de insights personalizados
