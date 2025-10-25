# Documentación de Arquitectura - Aplicación de Finanzas Personales con IA

Este repositorio contiene la documentación arquitectónica completa para el desarrollo de la aplicación móvil de gestión financiera personal asistida por inteligencia artificial.

## Estructura del Proyecto

```
├── diagramas/
│   ├── diagrama_c1_contexto.md       # Diagrama C1 - Contexto del Sistema
│   └── diagrama_c2_contenedores.md   # Diagrama C2 - Contenedores
├── adrs/
│   ├── ADR-001-arquitectura-general.md
│   ├── ADR-002-manejo-estado.md
│   ├── ADR-003-integracion-ia.md
│   └── ADR-004-seguridad-autenticacion.md
└── README.md
```

## Diagramas de Arquitectura

### Diagrama C1 - Contexto del Sistema
Muestra la interacción entre el usuario y el sistema principal, así como las dependencias externas (Firebase y Google Gemini API).

**Archivo:** `diagramas/diagrama_c1_contexto.md`

### Diagrama C2 - Contenedores
Detalla la arquitectura interna del sistema, mostrando los principales contenedores y sus responsabilidades.

**Archivo:** `diagramas/diagrama_c2_contenedores.md`

### Cómo Visualizar los Diagramas

Los diagramas están creados en formato Mermaid con un estilo profesional moderno. Para visualizarlos puedes:

1. **Vista Previa de Markdown (Más Fácil):**
   - Abre `diagramas/diagrama_c1_contexto.md` o `diagramas/diagrama_c2_contenedores.md`
   - Presiona `Ctrl+Shift+V` para vista previa
   - Los diagramas se renderizarán automáticamente

2. **Usar editores online:**
   - [Mermaid Live Editor](https://mermaid.live/) - Copia y pega el código del bloque ```mermaid
   - [Mermaid Chart](https://www.mermaidchart.com/) - Herramienta profesional

3. **Exportar como imagen (Alta calidad):**
   ```bash
   npm install -g @mermaid-js/mermaid-cli
   mmdc -i diagramas/diagrama_c1_contexto.md -o diagrama_c1.png -t dark
   mmdc -i diagramas/diagrama_c2_contenedores.md -o diagrama_c2.png -t dark
   ```

4. **Características del diseño:**
   - Colores profesionales y contrastantes
   - Iconos descriptivos para mejor comprensión
   - Etiquetas de tipo entre corchetes [Person], [Software System], etc.
   - Líneas punteadas para conexiones elegantes
   - Estructura clara y jerárquica

## ADRs (Architecture Decision Records)

Los ADRs documentan las decisiones arquitectónicas clave del proyecto:

### ADR-001: Decisión de Arquitectura General
**Estado:** Aceptada  
**Decisión:** Flutter + Firebase + Google Gemini API

### ADR-002: Decisión de Manejo de Estado
**Estado:** Aceptada  
**Decisión:** Riverpod como solución principal

### ADR-003: Decisión de Integración con IA
**Estado:** Aceptada  
**Decisión:** Google Gemini API para procesamiento de IA

### ADR-004: Decisión de Seguridad y Autenticación
**Estado:** Aceptada  
**Decisión:** Firebase Authentication + Security Rules

### ADR-005: Decisión de Framework de UI/UX
**Estado:** Aceptada  
**Decisión:** Material Design 3 + Custom Components

### ADR-006: Decisión de Modelado de Datos
**Estado:** Aceptada  
**Decisión:** NoSQL Documental con Cloud Firestore

### ADR-007: Decisión de Soporte Offline
**Estado:** Aceptada  
**Decisión:** Firebase Offline + SQLite Cache

### ADR-008: Decisión de Estrategia de Testing
**Estado:** Aceptada  
**Decisión:** Testing en Capas Integral

### ADR-009: Decisión de Deployment y CI/CD
**Estado:** Aceptada  
**Decisión:** GitHub Actions + Fastlane

### ADR-010: Decisión de Monitoreo y Analytics
**Estado:** Aceptada  
**Decisión:** Firebase Analytics + Crashlytics + Performance

## Resumen de Decisiones Arquitectónicas

| Aspecto | Decisión | Justificación |
|---------|----------|---------------|
| **Frontend** | Flutter | Desarrollo multiplataforma eficiente |
| **Backend** | Firebase | Backend-as-a-service completo |
| **Base de Datos** | Cloud Firestore | Base de datos NoSQL escalable |
| **Autenticación** | Firebase Auth | Seguridad integrada y múltiples métodos |
| **IA** | Google Gemini API | Integración nativa con ecosistema Google |
| **Estado** | Riverpod | Manejo de estado moderno y eficiente |
| **UI/UX** | Material Design 3 | Sistema de diseño moderno y accesible |
| **Offline** | Firebase Offline + SQLite | Soporte offline robusto |
| **Testing** | Testing en Capas | Cobertura integral de calidad |
| **CI/CD** | GitHub Actions + Fastlane | Deployment automatizado |
| **Monitoreo** | Firebase Analytics + Crashlytics | Monitoreo completo integrado |
| **Arquitectura** | MVVM + Clean Architecture | Separación de responsabilidades |

## Atributos de Calidad Considerados

- **Usabilidad:** Interfaz intuitiva y asistencia por IA
- **Seguridad:** Protección de datos financieros sensibles
- **Mantenibilidad:** Arquitectura limpia y modular
- **Escalabilidad:** Soluciones cloud que crecen con el proyecto
- **Rendimiento:** Optimización para dispositivos móviles

## Próximos Pasos

1. Configurar el proyecto Flutter
2. Integrar Firebase Authentication
3. Configurar Cloud Firestore
4. Implementar la integración con Gemini API
5. Desarrollar la UI/UX siguiendo los principios de usabilidad
6. Implementar las Security Rules
7. Configurar el manejo de estado con Riverpod

---

**Fecha de creación:** 2024-12-19  
**Versión:** 1.0  
**Estado:** En desarrollo
