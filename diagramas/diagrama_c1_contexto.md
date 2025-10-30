# Diagrama C1 - Contexto del Sistema

Este diagrama muestra la interacción entre el usuario y el sistema principal, así como las dependencias externas.

# Diagrama de Contexto (C1) - Gestor de Finanzas Personales

```mermaid
flowchart LR
    %% Nodos
    U[Usuario de Finanzas Personales]:::person
    S[Sistema Principal: App Flutter]:::software
    FB[Firebase: Base de datos y autenticación]:::software
    GEMINI[Google Gemini API: IA]:::software

    %% Relaciones
    U -->|Registra transacciones, visualiza reportes y recibe recomendaciones| S
    S -->|Almacena datos financieros y realiza autenticación| FB
    S -->|Clasifica transacciones y genera insights| GEMINI

    %% Estilos simples
    classDef person fill:#f4b400,stroke:#000,stroke-width:2px;
    classDef software fill:#ffffff,stroke:#007acc,stroke-width:2px;

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
