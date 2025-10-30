# Diagrama C1 - Contexto del Sistema

Este diagrama muestra la interacción entre el usuario y el sistema principal, así como las dependencias externas.

graph LR
    %% ==== Elementos ====
    Usuario["👤<br/>Usuario de Finanzas Personales<br/><br/>Persona que interactúa con la aplicación<br/><br/>[Person]"]
    Sistema["📱<br/>Sistema Principal<br/><br/>Aplicación móvil desarrollada en Flutter<br/><br/>[Software System]"]
    Firebase["🔥<br/>Firebase<br/><br/>Servicio externo para base de datos y autenticación<br/><br/>[Software System]"]
    Gemini["🤖<br/>Google Gemini API<br/><br/>Servicio externo de inteligencia artificial<br/><br/>[Software System]"]

    %% ==== Relaciones ====
    Usuario -->|"Registra transacciones,<br/>visualiza reportes y recibe recomendaciones"| Sistema
    Sistema -->|"Almacena datos financieros<br/>y realiza autenticación de usuarios"| Firebase
    Sistema -->|"Clasifica transacciones<br/>y genera insights personalizados"| Gemini

    %% ==== Estilos visuales ====
    classDef userClass fill:#f4b400,stroke:#d97706,stroke-width:3px,color:#000000,font-weight:bold
    classDef systemClass fill:#ffffff,stroke:#3b82f6,stroke-width:3px,color:#007acc,font-weight:bold
    classDef externalClass fill:#ffffff,stroke:#3b82f6,stroke-width:3px,color:#007acc,font-weight:bold
    classDef background fill:#0f172a,stroke:none,color:#ffffff

    %% ==== Aplicar clases ====
    class Usuario userClass
    class Sistema systemClass
    class Firebase,Gemini externalClass

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
