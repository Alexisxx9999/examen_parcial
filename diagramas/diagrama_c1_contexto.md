# Diagrama C1 - Contexto del Sistema

Este diagrama muestra la interacción entre el usuario y el sistema principal, así como las dependencias externas.

# 🧩 Diagrama C1 - Contexto del Sistema

Este diagrama representa la visión de alto nivel del sistema **Gestor de Finanzas Personales Asistido por IA**, mostrando los actores principales, los sistemas involucrados y las interacciones clave.

```mermaid
graph LR
    %% ==== Elementos ====
    U["👤 Usuario de Finanzas Personales\n[Person]"]
    S["📱 Sistema Principal\nAplicación móvil desarrollada en Flutter\n[Software System]"]
    FB["🔥 Firebase\nServicio externo para base de datos y autenticación\n[Software System]"]
    GEMINI["🤖 Google Gemini API\nServicio externo de inteligencia artificial\n[Software System]"]

    %% ==== Relaciones ====
    U -->|"Registra transacciones,\nvisualiza reportes y recibe recomendaciones"| S
    S -->|"Almacena datos financieros\ny realiza autenticación de usuarios"| FB
    S -->|"Clasifica transacciones\ny genera insights personalizados"| GEMINI

    %% ==== Estilos visuales (compatibles con GitHub) ====
    classDef person fill:#f4b400,stroke:#f4b400,stroke-width:3px,color:#000000,font-weight:bold
    classDef system fill:#ffffff,stroke:#007acc,stroke-width:3px,color:#007acc,font-weight:bold

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
