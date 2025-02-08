# 1. Descripción breve del software LTI, valor añadido y ventajas competitivas. Explicación de las funciones principales. Añadir un diagrama Lean Canvas para entender el modelo de negocio.

LTI es un Applicant Tracking System (ATS) de nueva generación que revoluciona el proceso de contratación aprovechando la inteligencia artificial. Diseñado para equipos de reclutamiento modernos, LTI automatiza las tareas repetitivas, facilita la colaboración en tiempo real entre recruiters y managers, y proporciona insights basados en datos para mejorar la calidad de las contrataciones.

Características clave:

- Automatización end-to-end del proceso usando IA avanzada
- Colaboración en tiempo real con herramientas integradas de comunicación
- Experiencia de candidato moderna y personalizada
- Analytics predictivos para mejorar la calidad de contratación
- API extensible para integración con otras herramientas de RRHH

El sistema reduce el tiempo de contratación hasta en un 50% mientras mejora la calidad de las contrataciones y la experiencia tanto del equipo de recruiting como de los candidatos.

<style>
  table {
    width: 100%;
    border-collapse: collapse;
    font-family: system-ui;
  }
  th, td {
    border: 1px solid #ddd;
    padding: 12px;
    text-align: left;
    vertical-align: top;
  }
  th {
    background-color: #f8f9fa;
    font-weight: bold;
  }
  ul {
    margin: 0;
    padding-left: 20px;
  }
</style>

<table>
  <tr>
    <th>1. PROBLEMA
      <ul>
        <li>Procesos manuales lentos y repetitivos en reclutamiento</li>
        <li>Descoordinación entre recruiters y hiring managers</li>
        <li>Pérdida de candidatos por mala experiencia</li>
        <li>Decisiones basadas en intuición, no en datos</li>
      </ul>
    </th>
    <th>2. SOLUCIÓN
      <ul>
        <li>Automatización IA end-to-end</li>
        <li>Hub de colaboración en tiempo real</li>
        <li>Portal de candidato moderno</li>
        <li>Analytics predictivos</li>
      </ul>
    </th>
    <th>3. PROPUESTA DE VALOR ÚNICA
      <p>ATS impulsado por IA que reduce el tiempo de contratación un 50% mientras mejora significativamente la calidad de las contrataciones y la experiencia de todos los stakeholders.</p>
    </th>
  </tr>
  <tr>
    <td>4. VENTAJA COMPETITIVA
      <ul>
        <li>IA estado del arte</li>
        <li>UX moderna e intuitiva</li>
        <li>API extensible</li>
        <li>Automatización avanzada</li>
      </ul>
    </td>
    <td>5. SEGMENTOS DE CLIENTE
      <ul>
        <li>Empresas tech 50-500 empleados</li>
        <li>Startups en fase de crecimiento</li>
        <li>Equipos de recruiting ágiles</li>
      </ul>
    </td>
    <td>6. MÉTRICAS CLAVE
      <ul>
        <li>Time-to-hire</li>
        <li>Calidad de contrataciones</li>
        <li>NPS de candidatos</li>
        <li>Churn rate</li>
      </ul>
    </td>
  </tr>
  <tr>
    <td>7. CANALES
      <ul>
        <li>Venta directa B2B</li>
        <li>Partnerships con ATS legacy</li>
        <li>Marketplaces de RRHH</li>
      </ul>
    </td>
    <td>8. ESTRUCTURA DE COSTES
      <ul>
        <li>Desarrollo de producto</li>
        <li>Infraestructura cloud</li>
        <li>Customer Success</li>
        <li>Marketing & Ventas</li>
      </ul>
    </td>
    <td>9. FUENTES DE INGRESOS
      <ul>
        <li>Suscripción por usuario/mes</li>
        <li>Setup & Onboarding</li>
        <li>Servicios profesionales</li>
      </ul>
    </td>
  </tr>
</table>

# 2. Descripción de los 3 casos de uso principales, con el diagrama asociado a cada uno.
## Casos de uso y overview

1. Proceso de publicación y gestión de ofertas (hiring manager + recruiter)
2. Proceso de evaluación de candidatos con IA
3. Portal del candidato y proceso de aplicación

```mermaid
flowchart TB
    subgraph ATS
        CU1[Gestionar Ofertas]
        CU2[Evaluar Candidatos]
        CU3[Aplicar a Ofertas]
        
        %% Casos de uso relacionados con Gestión de Ofertas
        CU1.1[Crear Oferta]
        CU1.2[Aprobar Oferta]
        CU1.3[Publicar Oferta]
        
        %% Casos de uso relacionados con Evaluación
        CU2.1[Screening IA]
        CU2.2[Programar Entrevista]
        CU2.3[Evaluar Fit]
        
        %% Casos de uso relacionados con Portal
        CU3.1[Registrarse]
        CU3.2[Subir CV]
        CU3.3[Ver Estado]
    end
    
    HM((Hiring Manager))
    RC((Recruiter))
    CD((Candidato))
    AI((Sistema IA))
    
    %% Relaciones Gestión Ofertas
    HM --> CU1.1
    RC --> CU1.1
    HM --> CU1.2
    RC --> CU1.3
    
    %% Relaciones Evaluación
    AI --> CU2.1
    RC --> CU2.2
    HM --> CU2.3
    
    %% Relaciones Portal
    CD --> CU3.1
    CD --> CU3.2
    CD --> CU3.3
    
    %% Jerarquía
    CU1.1 & CU1.2 & CU1.3 --> CU1
    CU2.1 & CU2.2 & CU2.3 --> CU2
    CU3.1 & CU3.2 & CU3.3 --> CU3
```

## Caso de uso 1: Proceso de publicación y gestión de ofertas (hiring manager + recruiter)

**Nombre:** Gestión de Ofertas

**Actores:**

- Hiring Manager (Principal)
- Recruiter (Principal)
- Sistema IA (Secundario)

**Precondiciones:**

Usuarios autenticados con roles correspondientes
Plantillas de ofertas disponibles

**Flujo Principal:**

1. Hiring Manager inicia creación de oferta

- Completa información básica (título, departamento, ubicación)
- Define requisitos técnicos y soft skills
- Sistema IA sugiere mejoras en tiempo real
- Guarda borrador

2. Recruiter refina la oferta

- Revisa y optimiza descripción
- Ajusta requisitos según mercado
- Añade información de beneficios y empresa
- Sistema IA valida contenido y SEO

3. Proceso de aprobación

- Recruiter solicita aprobación
- Hiring Manager recibe notificación
- Revisa cambios y aprueba
- Sistema notifica aprobación


4. Publicación

- Recruiter selecciona canales
- Sistema publica oferta
- Notifica a stakeholders


**Flujos Alternativos:**

- Hiring Manager solicita cambios en paso 3
- Oferta requiere aprobación adicional (ej: presupuesto)
- Publicación falla en algún canal

**Post-condiciones:**

- Oferta publicada en canales seleccionados
- Stakeholders notificados
- Sistema listo para recibir aplicaciones
```mermaid
sequenceDiagram
    actor HM as Hiring Manager
    actor RC as Recruiter
    participant S as Sistema
    participant AI as Sistema IA
    participant N as Notificaciones

    HM->>S: Crear borrador oferta
    S->>AI: Analizar requisitos
    AI-->>S: Sugerir mejoras
    S-->>HM: Mostrar sugerencias
    
    HM->>S: Guardar borrador
    S->>N: Notificar nuevo borrador
    N->>RC: Enviar notificación
    
    RC->>S: Abrir borrador
    RC->>S: Refinar oferta
    S->>AI: Validar cambios
    AI-->>S: Confirmar optimización
    
    RC->>S: Solicitar aprobación
    S->>N: Notificar pendiente aprobación
    N->>HM: Enviar notificación
    
    HM->>S: Revisar cambios
    HM->>S: Aprobar oferta
    
    S->>N: Notificar aprobación
    N->>RC: Enviar notificación
    
    RC->>S: Seleccionar canales publicación
    RC->>S: Publicar oferta
    
    S->>N: Notificar publicación exitosa
    N->>HM: Confirmar publicación
    N->>RC: Confirmar publicación
```

## Caso de uso 2: Proceso de evaluación de candidatos con IA

### Descripción
Sistema de evaluación automatizada de candidatos que combina análisis de IA con supervisión humana para optimizar el proceso de selección.

### Actores
#### Principales
- Sistema IA
- Recruiter

#### Secundarios
- Hiring Manager
- Candidato

### Precondiciones
- Oferta de trabajo activa y publicada
- Modelo de IA entrenado con los requisitos específicos de la posición
- Criterios de evaluación y umbrales definidos
- Calendario de entrevistadores configurado

### Flujo Principal

#### 1. Screening Inicial
- Sistema recibe nueva aplicación del candidato
- IA realiza análisis del CV contra requisitos de la posición
- IA verifica histórico del candidato si existe en el sistema
- Sistema genera puntuación inicial y evaluación detallada

#### 2. Evaluación Automatizada
- Sistema verifica si la puntuación supera el umbral mínimo
- IA genera reporte de adecuación al puesto
- IA prepara sugerencias de preguntas para entrevista
- Sistema notifica resultados al recruiter

#### 3. Proceso de Entrevista
- Sistema calcula slots disponibles basados en calendarios
- Candidato selecciona horario preferido
- Sistema agenda entrevista automáticamente
- IA prepara briefing para el entrevistador con puntos clave

#### 4. Feedback y Decisión
- Hiring Manager registra evaluación post-entrevista
- IA analiza el feedback y actualiza la puntuación
- Sistema determina y notifica siguientes pasos
- IA genera comunicaciones personalizadas según resultado

### Flujos Alternativos

#### A1. Candidato No Cumple Umbral
1. Sistema detecta puntuación insuficiente
2. IA genera feedback constructivo personalizado
3. Sistema envía rechazo automático con feedback
4. Actualiza analytics del proceso

#### A2. Problemas con Entrevista
1. Candidato rechaza todos los slots propuestos
2. Sistema notifica al recruiter
3. Recruiter decide acción manual

#### A3. Evaluación Técnica Adicional
1. Hiring Manager solicita prueba técnica
2. Sistema selecciona prueba apropiada
3. IA ajusta evaluación incluyendo resultados

### Post-condiciones
- Evaluación del candidato completamente registrada
- Candidato notificado del estado/resultado
- Pipeline de contratación actualizado
- Métricas del proceso actualizadas en el sistema

### Requisitos Especiales
- Tiempo máximo de respuesta inicial: 1 hora
- Disponibilidad del sistema: 99.9%
- Cumplimiento GDPR/LOPD
- Trazabilidad completa del proceso

### Frecuencia
- Continua, según volumen de aplicaciones
- Picos esperados tras publicación de nuevas ofertas

## Notas
- El sistema debe mantener un nivel de humanización en las comunicaciones
- Las evaluaciones de IA deben ser auditables
- Se debe permitir override manual de decisiones automatizadas
```mermaid
sequenceDiagram
    actor CD as Candidato
    actor RC as Recruiter
    actor HM as Hiring Manager
    participant S as Sistema
    participant AI as Sistema IA
    participant DB as Base de Datos
    participant CAL as Calendario
    participant N as Notificaciones

    CD->>S: Aplicar a oferta
    S->>DB: Guardar aplicación
    S->>AI: Iniciar screening
    
    AI->>DB: Obtener requisitos oferta
    AI->>DB: Analizar CV candidato
    AI->>DB: Obtener histórico evaluaciones
    
    AI-->>S: Enviar score y evaluación
    S->>DB: Actualizar candidato
    
    alt Score > Umbral Mínimo
        S->>N: Notificar candidato viable
        N->>RC: Enviar evaluación IA
        
        RC->>S: Revisar evaluación
        RC->>S: Aprobar siguiente fase
        
        S->>AI: Sugerir slots entrevista
        AI->>CAL: Consultar disponibilidad HM
        CAL-->>AI: Devolver slots disponibles
        
        S->>N: Enviar opciones entrevista
        N->>CD: Solicitar preferencia horaria
        CD->>S: Seleccionar slot
        
        S->>CAL: Agendar entrevista
        S->>N: Confirmar entrevista
        N->>CD: Enviar confirmación
        N->>HM: Enviar calendario + contexto
    else Score < Umbral Mínimo
        S->>AI: Generar feedback constructivo
        S->>N: Enviar rechazo automático
        N->>CD: Notificar + feedback
    end

    HM->>S: Registrar feedback entrevista
    S->>AI: Analizar feedback
    AI-->>S: Actualizar evaluación
    
    S->>N: Notificar actualización
    N->>RC: Enviar nueva evaluación
```

## Caso de Uso 3: Portal del Candidato

### Descripción
Portal web que permite a los candidatos gestionar su proceso de búsqueda de empleo, desde el registro hasta el seguimiento de sus aplicaciones, proporcionando una experiencia personalizada y transparente.

### Actores
#### Principal
- Candidato

#### Secundarios
- Sistema IA
- Sistema de Notificaciones
- API LinkedIn

### Precondiciones
- Portal web operativo y accesible
- Sistema de autenticación funcionando
- Conexión con LinkedIn API configurada
- Ofertas activas en el sistema

### Flujo Principal

#### 1. Registro y Perfil
- Candidato accede al portal
- Crea cuenta o inicia sesión con email/LinkedIn
- Completa perfil profesional
- Sistema sincroniza datos con LinkedIn (opcional)
- IA analiza perfil para personalización

#### 2. Exploración de Ofertas
- Sistema muestra dashboard personalizado
- IA recomienda ofertas relevantes
- Candidato puede buscar y filtrar ofertas
- Sistema muestra match score por oferta

#### 3. Aplicación a Ofertas
- Candidato selecciona oferta
- Revisa requisitos y descripción
- Adjunta/actualiza CV específico
- Completa preguntas específicas
- Sistema confirma aplicación

#### 4. Seguimiento
- Candidato accede a su dashboard
- Visualiza estado de cada aplicación
- Recibe notificaciones de actualizaciones
- Gestiona próximos pasos (ej: entrevistas)

### Flujos Alternativos

#### A1. Registro con LinkedIn
1. Candidato elige "Conectar con LinkedIn"
2. Autoriza acceso a datos
3. Sistema pre-rellena perfil
4. Candidato verifica/completa información

#### A2. CV no Compatible
1. Sistema detecta formato no soportado
2. Muestra instrucciones de formato
3. Permite nuevo intento de subida

#### A3. Recuperación de Acceso
1. Candidato solicita reset de contraseña
2. Sistema verifica identidad
3. Envía instrucciones de recuperación

### Post-condiciones
- Perfil del candidato actualizado
- Aplicaciones registradas correctamente
- Notificaciones configuradas
- Analytics de uso actualizadas

### Requisitos Especiales
- Interfaz responsive (mobile-first)
- Tiempo de carga máximo: 2 segundos
- Accesibilidad WCAG 2.1
- Soporte multi-idioma
- Cumplimiento GDPR/LOPD

### Frecuencia
- Acceso continuo 24/7
- Picos durante horario laboral
- Aumentos tras publicación de nuevas ofertas

### Métricas Clave
- Tasa de registro completado
- Tiempo medio por aplicación
- Tasa de conversión (visitas/aplicaciones)
- NPS del portal
- Tasa de abandono

### Notas
- El diseño debe priorizar la experiencia de usuario
- Todas las acciones deben ser confirmadas
- Sistema debe mantener histórico de interacciones
- Feedback continuo del estado de las aplicaciones

```mermaid
sequenceDiagram
    actor CD as Candidato
    participant P as Portal
    participant S as Sistema
    participant AI as Sistema IA
    participant DB as Base de Datos
    participant N as Notificaciones
    participant LI as LinkedIn API

    CD->>P: Acceder al portal
    
    alt Nuevo Usuario
        CD->>P: Registrarse
        P->>S: Crear cuenta
        S->>DB: Almacenar datos
        
        opt Conectar LinkedIn
            CD->>P: Autorizar LinkedIn
            P->>LI: Solicitar perfil
            LI-->>P: Datos perfil
            P->>S: Sincronizar datos
            S->>DB: Actualizar perfil
        end
    else Usuario Existente
        CD->>P: Login
        P->>S: Validar credenciales
        S-->>P: Confirmar acceso
    end

    CD->>P: Explorar ofertas
    P->>AI: Solicitar recomendaciones
    AI->>DB: Analizar perfil/preferencias
    AI-->>P: Mostrar ofertas personalizadas
    
    CD->>P: Aplicar a oferta
    P->>S: Enviar aplicación
    S->>AI: Analizar aplicación
    AI-->>S: Evaluación inicial
    S->>DB: Guardar aplicación
    S->>N: Generar confirmación
    N-->>CD: Enviar confirmación
    
    CD->>P: Ver estado aplicaciones
    P->>DB: Consultar estados
    DB-->>P: Estado actualizado
    P-->>CD: Mostrar dashboard
    
    loop Seguimiento
        S->>DB: Actualizar estado
        S->>N: Notificar cambios
        N-->>CD: Enviar actualización
        CD->>P: Ver detalles
    end
```

# 3. Modelo de datos:
```mermaid
erDiagram
    Company ||--o{ User : "employs"
    User ||--o{ JobPosting : "creates/manages"
    User ||--o{ Application : "submits"
    User ||--o{ Evaluation : "performs"
    User ||--o{ Feedback : "provides"
    
    JobPosting ||--o{ Application : "receives"
    JobPosting ||--o{ Skill : "requires"
    
    Application ||--o{ Evaluation : "undergoes"
    Application ||--o{ Interview : "schedules"
    Application ||--o{ Feedback : "receives"
    
    User {
        uuid id PK
        string email
        string password_hash
        string first_name
        string last_name
        enum role
        string phone
        datetime created_at
        datetime updated_at
    }

    Company {
        uuid id PK
        string name
        string description
        string website
        string industry
        string size_range
        datetime created_at
    }

    JobPosting {
        uuid id PK
        uuid company_id FK
        uuid creator_id FK
        string title
        text description
        string location
        enum status
        date start_date
        date end_date
        datetime created_at
        datetime updated_at
    }

    Application {
        uuid id PK
        uuid job_id FK
        uuid candidate_id FK
        text cover_letter
        string cv_url
        enum status
        float ai_score
        datetime applied_at
        datetime updated_at
    }

    Evaluation {
        uuid id PK
        uuid application_id FK
        uuid evaluator_id FK
        float score
        text comments
        json criteria_scores
        datetime created_at
    }

    Interview {
        uuid id PK
        uuid application_id FK
        uuid interviewer_id FK
        datetime scheduled_at
        enum status
        string meeting_url
        text notes
    }

    Skill {
        uuid id PK
        string name
        string category
        text description
    }

    Feedback {
        uuid id PK
        uuid application_id FK
        uuid provider_id FK
        text content
        integer rating
        datetime created_at
    }
```
# 4. Diseño de Alto Nivel - LTI ATS

## Visión General
LTI ATS está diseñado como una plataforma cloud-native basada en microservicios, priorizando escalabilidad, mantenibilidad y capacidad de evolución independiente de cada componente.

## Capas del Sistema

### 1. Client Layer
- **Web Application**: SPA desarrollada en React para acceso desde navegador
- **Mobile Application**: App móvil en React Native para acceso en movilidad
- Ambas comparten lógica de negocio y componentes core

### 2. API Gateway
- **Gateway**: Punto único de entrada, manejo de routing y rate limiting
- **Auth Service**: Gestión de autenticación y autorización con Keycloak
- Implementa JWT para seguridad entre servicios

### 3. Core Services
Microservicios especializados:
- **Jobs Service**: Gestión de ofertas de trabajo
- **Candidates Service**: Gestión de perfiles de candidatos
- **Applications Service**: Gestión de postulaciones
- **Evaluation Service**: Motor de evaluaciones
- **Interview Service**: Gestión de entrevistas

### 4. AI Layer
Servicios especializados de IA:
- **Matching Engine**: Análisis de fit candidato-oferta
- **Evaluation Engine**: Evaluación automática de perfiles
- **Recommendations**: Sistema de recomendaciones personalizado

### 5. Data Layer
- **PostgreSQL**: Almacenamiento principal relacional
- **Redis**: Caché y gestión de sesiones
- **Elasticsearch**: Búsqueda avanzada y análisis de texto

### 6. External Services
Integraciones con servicios externos:
- **Email Service**: Notificaciones por correo
- **Calendar Service**: Gestión de agendas y entrevistas
- **LinkedIn API**: Integración con perfiles profesionales

## Aspectos Técnicos Clave

### Escalabilidad
- Servicios stateless para escalar horizontalmente
- Caché distribuida con Redis
- Load balancing a nivel de API Gateway

### Resiliencia
- Circuit breakers entre servicios
- Retry policies para operaciones fallidas
- Health checks y auto-healing

### Monitorización
- Distributed tracing
- Métricas de rendimiento
- Logs centralizados

### Seguridad
- Autenticación JWT
- Encryption en tránsito y reposo
- WAF en API Gateway

## Consideraciones de Implementación

### DevOps
- CI/CD automatizado
- Infraestructura como código
- Containerización con Docker
- Orquestación con Kubernetes

### Desarrollo
- API First approach
- Documentación automática con OpenAPI
- Testing automatizado en todas las capas

### Datos
- Migraciones automáticas
- Backups periódicos
- Estrategia de disaster recovery

## Próximos Pasos
1. MVP con servicios core
2. Iteración en capa de IA
3. Ampliación de integraciones
4. Optimización de rendimiento

```mermaid
flowchart TB
    subgraph ClientLayer[Client Layer]
        WEB["Web App\n(React)"]
        MOB["Mobile App\n(React Native)"]
    end

    subgraph Gateway[API Gateway]
        GW["API Gateway\n(Kong/Nginx)"]
        AUTH["Auth Service\n(Keycloak)"]
    end

    subgraph CoreServices[Core Services]
        JOBS["Jobs Service\n(Ofertas)"]
        CAND["Candidates Service\n(Candidatos)"]
        APP["Applications Service\n(Postulaciones)"]
        EVAL["Evaluation Service\n(Evaluaciones)"]
        INTER["Interview Service\n(Entrevistas)"]
    end

    subgraph AILayer[AI Layer]
        AI_MATCH["AI Matching Engine"]
        AI_EVAL["AI Evaluation Engine"]
        AI_REC["AI Recommendations"]
    end

    subgraph DataLayer[Data Layer]
        DB[(PostgreSQL)]
        CACHE[(Redis)]
        SEARCH[(Elasticsearch)]
    end

    subgraph ExternalServices[External Services]
        EMAIL["Email Service"]
        CAL["Calendar Service"]
        LINKEDIN["LinkedIn API"]
    end

    WEB --> GW
    MOB --> GW
    GW --> AUTH
    GW --> JOBS
    GW --> CAND
    GW --> APP
    GW --> EVAL
    GW --> INTER
    
    JOBS --> DB
    CAND --> DB
    APP --> DB
    EVAL --> DB
    INTER --> DB
    
    JOBS & CAND & APP & EVAL & INTER --> CACHE
    JOBS & CAND & APP & EVAL & INTER --> SEARCH
    
    JOBS --> AI_MATCH
    CAND --> AI_MATCH
    APP --> AI_EVAL
    EVAL --> AI_REC
    
    JOBS --> EMAIL
    APP --> EMAIL
    INTER --> CAL
    CAND --> LINKEDIN
```


# 5. Diagramas C4 para el componente: Evaluation Service

## Descripción
El Evaluation Service es el corazón del sistema de IA de LTI ATS. Se encarga de evaluar candidatos, realizar matching con ofertas y proporcionar recomendaciones basadas en datos.

## Componentes Principales

### API Controller
- Implementado en FastAPI
- Expone endpoints REST/gRPC
- Maneja autenticación y validación
- Coordina flujos de evaluación

### Matching Engine
- Core de IA para match candidato-oferta
- Utiliza TensorFlow para deep learning
- Análisis semántico de CVs y ofertas
- Scoring multidimensional

### Profile Scorer
- Evaluación objetiva de perfiles
- Modelos de ML para scoring
- Análisis de skills técnicos
- Predicción de fit cultural

### Rules Engine
- Implementa reglas de negocio
- Validaciones personalizables
- Filtros configurables
- Políticas de empresa

### ML Pipeline
- Gestión de modelos ML
- Entrenamiento automático
- Monitorización de rendimiento
- Versionado de modelos

### Repository
- Capa de acceso a datos
- Caché inteligente
- Queries optimizadas
- Transacciones ACID

## Tecnologías Clave
- Python 3.9+
- FastAPI
- TensorFlow/PyTorch
- SQLAlchemy
- Redis
- PostgreSQL

## Características
- Alta disponibilidad
- Escalado horizontal
- Procesamiento asíncrono
- Monitorización avanzada

## Diagrama C4 Nivel 1: Contexto
```mermaid
flowchart TB
    subgraph Users
        candidate[Candidato]
        recruiter[Recruiter]
        manager[Hiring Manager]
    end

    subgraph LTI ATS
        ats[Sistema de gestión\nde candidatos con IA]
    end

    subgraph External Systems
        linkedin[LinkedIn]
        calendar[Calendar Provider]
        email[Email Provider]
    end

    candidate --> ats
    recruiter --> ats
    manager --> ats

    ats --> linkedin
    ats --> calendar
    ats --> email
```


## Diagrama C4 Nivel 2: Contenedores
```mermaid
flowchart TB
    subgraph Frontend
        spa[Single Page App\nReact]
        mobile[Mobile App\nReact Native]
    end

    subgraph API Layer
        gateway[API Gateway\nKong]
        jobs[Jobs Service\nNode.js]
        candidates[Candidates Service\nNode.js]
        evaluation[Evaluation Service\nPython]
        interviews[Interview Service\nNode.js]
    end

    subgraph Data Layer
        db[(PostgreSQL)]
        cache[(Redis)]
        search[(Elasticsearch)]
    end

    subgraph External
        linkedin[LinkedIn]
        calendar[Calendar]
        email[Email]
    end

    spa --> gateway
    mobile --> gateway
    
    gateway --> jobs & candidates & evaluation & interviews
    
    jobs & candidates & evaluation & interviews --> db
    evaluation --> cache
    evaluation --> search
    
    evaluation --> linkedin
    interviews --> calendar
    jobs --> email
```

## Diagrama C4 Nivel 3: Componentes del Evaluation Service
```mermaid
flowchart TB
    subgraph Evaluation Service
        api[API Controller\nFastAPI]
        matcher[Matching Engine\nPython+TensorFlow]
        scorer[Profile Scorer\nPython+Scikit]
        rules[Rules Engine\nPython]
        ml[ML Pipeline\nPython+MLflow]
        repo[Repository\nSQLAlchemy]
    end

    subgraph External Components
        gateway[API Gateway]
        db[(Database)]
        cache[(Cache)]
    end

    gateway --> api
    api --> matcher & scorer & rules
    matcher & scorer --> ml
    api --> repo
    repo --> db
    matcher --> cache
```
