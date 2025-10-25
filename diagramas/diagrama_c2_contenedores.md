# Diagrama C2 - Contenedores

Este diagrama detalla la arquitectura interna del sistema, mostrando los principales contenedores y sus responsabilidades.

```mermaid
graph TB
    %% Usuario
    Usuario["👤<br/>Usuario de Finanzas<br/>Personales<br/><br/>[Person]"]
    
    %% Aplicación Móvil Flutter
    subgraph AppMobile["📱 Aplicación Móvil Flutter [Mobile App]"]
        UI["🖥️<br/>Interfaz de Usuario<br/>Screens, Widgets<br/>Navigation<br/><br/>[Flutter App]"]
        ViewModel["⚙️<br/>ViewModels<br/>Business Logic<br/>MVVM Pattern<br/><br/>[Flutter App]"]
        State["🔄<br/>State Management<br/>Riverpod Provider<br/>Reactive Updates<br/><br/>[Flutter App]"]
    end
    
    %% Servicios Backend
    subgraph Backend["☁️ Servicios Backend [Backend Services]"]
        Auth["🔐<br/>Firebase Authentication<br/>Login, Registro<br/>Biometría<br/><br/>[Firebase Service]"]
        Firestore["💾<br/>Cloud Firestore<br/>Transacciones, Usuarios<br/>Configuración<br/><br/>[Firebase Service]"]
        Storage["📁<br/>Firebase Storage<br/>Archivos adjuntos<br/>Reportes PDF<br/><br/>[Firebase Service]"]
    end
    
    %% Servicios de IA
    subgraph AI["🤖 Servicios de Inteligencia Artificial [AI Services]"]
        GeminiAPI["🧠<br/>Google Gemini API<br/>Clasificación automática<br/>de transacciones<br/><br/>[External API]"]
        AIProcessor["⚡<br/>Procesador de IA<br/>Análisis de patrones<br/>Recomendaciones<br/><br/>[AI Service]"]
    end
    
    %% Interacciones
    Usuario -.->|"Interactúa con<br/>la interfaz"| UI
    UI -.->|"Eventos de<br/>usuario"| ViewModel
    ViewModel -.->|"Gestión de<br/>estado reactivo"| State
    ViewModel -.->|"Autenticación<br/>segura"| Auth
    ViewModel -.->|"CRUD de datos<br/>financieros"| Firestore
    ViewModel -.->|"Clasificación<br/>automática"| GeminiAPI
    ViewModel -.->|"Almacenar<br/>archivos"| Storage
    GeminiAPI -.->|"Procesamiento<br/>inteligente"| AIProcessor
    
    %% Estilos profesionales modernos
    classDef userClass fill:#1e3a8a,stroke:#3b82f6,stroke-width:3px,color:#ffffff,font-weight:bold
    classDef appClass fill:#7c3aed,stroke:#a855f7,stroke-width:3px,color:#ffffff,font-weight:bold
    classDef backendClass fill:#059669,stroke:#10b981,stroke-width:3px,color:#ffffff,font-weight:bold
    classDef aiClass fill:#dc2626,stroke:#ef4444,stroke-width:3px,color:#ffffff,font-weight:bold
    
    class Usuario userClass
    class UI,ViewModel,State appClass
    class Auth,Firestore,Storage backendClass
    class GeminiAPI,AIProcessor aiClass
```

## Descripción

Este diagrama de contenedores (C2) muestra la arquitectura interna detallada del sistema, organizada en tres grupos principales:

### 📱 Aplicación Móvil Flutter
- **Interfaz de Usuario**: Screens, Widgets y Navigation
- **ViewModels**: Lógica de negocio siguiendo el patrón MVVM
- **State Management**: Gestión de estado reactivo con Riverpod

### ☁️ Servicios Backend
- **Firebase Authentication**: Login, registro y autenticación biométrica
- **Cloud Firestore**: Almacenamiento de transacciones, usuarios y configuración
- **Firebase Storage**: Gestión de archivos adjuntos y reportes PDF

### 🤖 Servicios de Inteligencia Artificial
- **Google Gemini API**: Clasificación automática de transacciones
- **Procesador de IA**: Análisis de patrones y generación de recomendaciones

## Flujo de Datos

1. **Usuario** interactúa con la **Interfaz de Usuario**
2. **UI** envía eventos al **ViewModel**
3. **ViewModel** gestiona el **Estado** y comunica con servicios externos
4. **Backend Services** manejan autenticación, datos y almacenamiento
5. **AI Services** procesan transacciones y generan insights
