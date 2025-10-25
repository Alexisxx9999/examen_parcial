# Diagrama C1 - Contexto del Sistema

Este diagrama muestra la interacción entre el usuario y el sistema principal, así como las dependencias externas.

```mermaid
graph LR
    %% Usuarios del Sistema
    Usuario["👤<br/>Usuario de Finanzas<br/>Personales<br/><br/>[Person]"]
    
    %% Sistema Principal
    Sistema["📱<br/>Gestor de Finanzas<br/>Personales Asistido por IA<br/><br/>[Software System]"]
    
    %% Sistemas Externos
    Firebase["🔥<br/>Firebase<br/>Base de Datos y<br/>Autenticación<br/><br/>[External System]"]
    Gemini["🤖<br/>Google Gemini API<br/>Procesamiento<br/>de IA<br/><br/>[External System]"]
    
    %% Interacciones
    Usuario -.->|"Registra transacciones<br/>Visualiza reportes<br/>Recibe recomendaciones"| Sistema
    Sistema -.->|"Almacena datos<br/>financieros<br/>Autentica usuarios"| Firebase
    Sistema -.->|"Clasifica transacciones<br/>Genera insights<br/>personalizados"| Gemini
    
    %% Estilos profesionales
    classDef userClass fill:#1e3a8a,stroke:#3b82f6,stroke-width:3px,color:#ffffff,font-weight:bold
    classDef systemClass fill:#7c3aed,stroke:#a855f7,stroke-width:3px,color:#ffffff,font-weight:bold
    classDef externalClass fill:#dc2626,stroke:#ef4444,stroke-width:3px,color:#ffffff,font-weight:bold
    
    class Usuario userClass
    class Sistema systemClass
    class Firebase,Gemini externalClass
```

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
