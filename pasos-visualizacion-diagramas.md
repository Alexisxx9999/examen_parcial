# Visualización de Diagramas - Aplicación de Finanzas Personales con IA

## Diagrama C1 - Contexto del Sistema

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

---

## Diagrama C2 - Contenedores

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

---

## Cómo Visualizar los Diagramas en VS Code

### Primero Instalar las extensiones
- Markdown Preview enhanced 
- Markdown Preview Mermaid


### Método 1: Vista Previa de Markdown (Recomendado)


1. Abre el archivo `visualizacion-diagramas.md` en VS Code
2. Presiona `Ctrl+Shift+V` para abrir la vista previa de Markdown
3. Los diagramas se renderizarán automáticamente

### Método 2: Vista Previa de Mermaid Directa
1. Abre cualquiera de los archivos `.mmd` en VS Code
2. Presiona `Ctrl+Shift+P` y busca "Mermaid Preview"
3. Selecciona "Mermaid: Preview" para ver el diagrama renderizado

### Método 3: Comando de Paleta
1. Con cualquier archivo `.mmd` abierto
2. `Ctrl+Shift+P` → "Mermaid: Preview"
3. Se abrirá una nueva pestaña con el diagrama renderizado

### Características de los Diagramas
- ✅ **Estilo profesional** con colores modernos
- ✅ **Iconos descriptivos** para mejor comprensión
- ✅ **Etiquetas de tipo** estándar [Person], [Software System], etc.
- ✅ **Líneas punteadas** para conexiones elegantes
- ✅ **Colores diferenciados** por tipo de componente
- ✅ **Estructura clara** y jerárquica
