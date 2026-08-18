# Arquitecturas de Software (ARSW)

Repositorio general del curso Arquitecturas de Software, que agrupa —mediante submódulos de git— las actividades académicas (trabajos en clase, tareas, talleres, laboratorios y parcial) y el proyecto del curso.

Cada submódulo es un repositorio independiente con su propio historial de commits y README. Para saber cómo aprovechar este repositorio, ver [Cómo usar este repositorio](#cómo-usar-este-repositorio).

## Estructura del proyecto

```
Arquitecturas-de-Software/
├── TrabajosEnClase/                                          # Submódulos
│   ├── MATRIX-Simulation-ARSW/
│   ├── ESTILOS-CALL-RETURN-ARSW/
│   └── reddis-ARSW/
├── Tareas/                                                   # Submódulo
│   └── java-go-concurrency-benchmark-ARSW/
├── Talleres/                                                 # Submódulo
│   └── KAFKA-ARSW/
├── Parciales/                                                # Submódulo
│   └── Parcial-T1-ARSW/
├── Laboratorios/                                             # Submódulos
│   ├── Lab_SnakeRace-Java21/
│   ├── wait-notify-excercise/
│   ├── BarrierSyncProblem-ARSW/
│   ├── Evolucion-de-Arquitecturas-Distribuidas-con-Java-ARSW/
│   ├── BluePrints/                                           # Labs de BluePrints + sus backends de ejemplo
│   │   ├── Lab_P1_BluePrints_Java21_API/
│   │   ├── Lab_P4_BluePrints_RealTime-Sokets/
│   │   ├── example-backend-socketio-node-/
│   │   └── example-backend-stopm/
│   ├── Alta-disponibilidad-ARSW/
│   ├── Observabilidad-ARSW/
│   ├── Escalabilidad-ARSW/
│   └── Pruebas-ARSW/                                          # Estrategia de pruebas por capas: unitarias, API, integración, E2E, carga y CI/CD
└── Proyectos/
    └── RaceFlow/                                             # Submódulos — organización RaceFlowECI
        ├── raceflow-frontend/
        ├── raceflow-api-gateway/
        ├── raceflow-auth-service/
        ├── raceflow-room-service/
        ├── raceflow-realtime-service/
        ├── raceflow-session-service/
        ├── raceflow-metrics-service/
        └── raceflow-observability/
```

## Temas del curso

El curso recorre el diseño y la operación de arquitecturas de software distribuidas, desde la concurrencia a nivel de hilos hasta el despliegue en la nube:

- Hilos y concurrencia en Java y Go; sincronización (`wait`/`notify`, barreras).
- Programación orientada a objetos avanzada: genéricos y expresiones lambda.
- Estilos de arquitectura Call-Return.
- Evolución de arquitecturas distribuidas: TCP, RMI, HTTP, gRPC.
- Sistemas basados en eventos distribuidos (Kafka).
- Principios INVEST para historias de usuario.
- Atributos y escenarios de calidad de software.
- Arquitecturas modernas de software (microservicios, APIs REST, WebSockets/tiempo real).
- Pruebas de software.
- Seguridad y calidad.
- Alta disponibilidad (balanceo de carga, múltiples zonas de disponibilidad en AWS).
- Escalabilidad horizontal (Auto Scaling en AWS).
- Observabilidad (métricas, logs y dashboards con Prometheus, Loki y Grafana).
- Infraestructura como código con Terraform.

## Cosas a tener en cuenta

- Cada repositorio corresponde a una actividad puntual (trabajo en clase, tarea, taller, laboratorio o parcial); el tipo de actividad está indicado en la descripción de cada repositorio, no en su nombre.
- Varios de los repositorios de laboratorio conservan sus ramas `develop`/`main` (y en algunos casos `develop-es`) del flujo de trabajo original; `main` es la rama que se referencia aquí como submódulo.
- Dentro de `Laboratorios/BluePrints/`, `example-backend-socketio-node-` y `example-backend-stopm` son backends de ejemplo (Socket.IO y STOMP) usados como referencia para el laboratorio de colaboración en tiempo real (`Lab_P4_BluePrints_RealTime-Sokets`), no actividades evaluadas por sí solas.
- El proyecto del curso, **RaceFlow**, es una plataforma de organización de carreras/eventos en tiempo real construida como un sistema de microservicios (frontend, API Gateway, autenticación, salas, tiempo real, sesiones, métricas y observabilidad). Su código vive en la organización [RaceFlowECI](https://github.com/RaceFlowECI).

## Herramientas

- **Java 21** y **Go** — concurrencia y comparación de rendimiento.
- **Spring Boot** — APIs y microservicios.
- **Kafka** — mensajería basada en eventos.
- **Node.js (Socket.IO)** y **STOMP sobre WebSocket** — comunicación en tiempo real.
- **Docker** — contenedores.
- **AWS** (EC2 Auto Scaling, Application Load Balancer, CloudWatch) y **Terraform** — infraestructura en la nube.
- **Prometheus, Loki y Grafana** — observabilidad.

## Profesor

Rodrigo Humberto Gualtero Martínez.

## Cómo usar este repositorio

Este repositorio no contiene código directamente: es una colección de repositorios independientes, uno por actividad, organizados por carpetas (`TrabajosEnClase/`, `Tareas/`, `Talleres/`, `Parciales/`, `Laboratorios/`, `Proyectos/`). Cada carpeta es un submódulo de git que apunta al repositorio real de esa actividad.

- **Para consultar una actividad puntual**: entra directamente a su carpeta en GitHub (o navega el submódulo) y revisa su propio README.
- **Para tener todo el contenido en tu máquina**:

```bash
git clone --recurse-submodules https://github.com/JuanGuayazanC/Arquitecturas-de-Software.git
```

Si ya clonaste el repositorio sin submódulos:

```bash
git submodule update --init --recursive
```
