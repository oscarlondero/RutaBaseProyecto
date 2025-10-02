# Ruta Base de Proyecto — TUP UTN

Guía práctica para egresados/as de la Tecnicatura Universitaria en Programación (UTN) para **dar forma, organizar y entregar** proyectos de desarrollo, ya sea **individualmente** o en **equipos**. Este README funciona como referencia viva y punto único de consulta.

---

## Tabla de contenidos
- [Visión general](#visión-general)
- [Ruta base de proyecto](#ruta-base-de-proyecto)
  - [0) Kickoff](#0-kickoff-½1-día)
  - [1) Descubrimiento rápido](#1-descubrimiento-rápido-23-días)
  - [2) Diseño funcional](#2-diseño-funcional-35-días)
  - [3) Diseño técnico](#3-diseño-técnico-24-días)
  - [4) Construcción iterativa (Sprints)](#4-construcción-iterativa-sprints-de-12-semanas)
  - [5) QA + UAT](#5-qa--uat-1-semana)
  - [6) Despliegue y transferencia](#6-despliegue-y-transferencia-23-días)
  - [7) Cierre y mejora](#7-cierre-y-mejora-12-días)
- [Cronograma sugerido (8–10 semanas)](#cronograma-sugerido-810-semanas)
- [Plantillas (templates)](#plantillas-templates)
- [Organización del equipo](#organización-del-equipo)
- [Paquete mínimo para el demandante](#paquete-mínimo-para-el-demandante-cada-hito)
- [Variantes según contexto](#variantes-según-contexto)
- [CI base (Continuous Integration)](#ci-base-continuous-integration)
- [Cómo usar este repositorio](#cómo-usar-este-repositorio)
- [Contribuir](#contribuir)
- [Licencia](#licencia)

---

## Visión general
Este esquema te ayuda a **alinear expectativas**, **planificar por fases**, **entregar evidencias** y **mejorar continuamente**, manteniendo calidad técnica y claridad con el demandante del proyecto.

---

## Ruta base de proyecto

### 0) Kickoff (½–1 día)
**Objetivo:** Alinear expectativas y alcance inicial.  
**Entregables al demandante:**
- Project Brief 1-página (problema, objetivo, alcance y fuera de alcance, métricas, stakeholders, canales y frecuencia).
- Agenda de trabajo (fechas de hitos y demos).

**Organización interna:**
- Crear repositorio (GitHub/GitLab), tablero (Trello/Jira), carpeta compartida (Drive).
- Definir roles mínimos: Líder/PM, Líder técnico, Dev, QA, UX/Funcional (pueden solaparse en equipos chicos).
- Acordar encuentros: daily 10–15 min, planning semanal, demo quincenal.

---

### 1) Descubrimiento rápido (2–3 días)
**Objetivo:** Entender procesos y restricciones.  
**Entregables al demandante:**
- Mapa de proceso (MER/UML simple o bullets/Viñetas).
- Lista priorizada de requerimientos.

**Organización interna:**
- Armar Backlog (épicas → historias de usuario (necesidades) con criterios de aceptación).
- Registrar supuestos y riesgos (log de riesgos).

---

### 2) Diseño funcional (3–5 días)
**Objetivo:** Acordar qué hará el sistema desde el punto de vista del negocio/usuario.  
**Entregables al demandante:**
- Historias de usuario con criterios de aceptación (GWT: Given-When-Then).
- Wireframes/prototipo de baja fidelidad (3–5 pantallas clave).
- Reglas de negocio y casos borde.

**Organización interna:**
- Definition of Ready (DoR) para dar por “listo para desarrollar”.
- Criterios de priorización (valor, riesgo, dependencia).

---

### 3) Diseño técnico (2–4 días)
**Objetivo:** Bajar a arquitectura y estándares.  
**Entregables al demandante (resumen ejecutivo):**
- Arquitectura mínima (diagrama simple: frontend, backend, DB, integraciones).
- No-funcionales clave (seguridad, rendimiento, auditoría, backup, compatibilidad).

**Organización interna:**
- Stack y convenciones (nombres, ramas git, code style.).
- Esquema de datos (DER inicial), migraciones base.
- Pipelines: CI/CD simple (build + tests + deploy a staging). Integraciones con  entornos.
- Definition of Done (DoD): code + tests + revisión + documentación mínima + demo.

---

### 4) Construcción iterativa (Sprints de 1–2 semanas)
**Objetivo:** Entregar valor en pequeños incrementos demostrables.  
**Entregables al demandante (por sprint):**
- Demo funcional (video corto o sesión en vivo).
- Changelog y feedback recogido.

**Organización interna:**
- Sprint Planning: capacidad, historias comprometidas, criterios de aceptación.
- Daily 10–15 min (bloqueos, plan del día).
- Code reviews (codigos chicos).
- QA continuo: pruebas exploratorias + checklist de regresión.
- Métricas: lead time, bugs abiertos, % historias completadas.

---

### 5) QA + UAT (1 semana)
**Objetivo:** Validación de calidad y del usuario (User Acceptance Testing).  
**Entregables al demandante:**
- Plan de pruebas UAT + Guía de uso (breve).
- Acta de conformidad o lista de observaciones con plazos.

**Organización interna:**
- Test funcional, de seguridad básica (authZ/authN, inyección), y rendimiento mínimo.
- Corrección de observaciones priorizadas.

---

### 6) Despliegue y transferencia (2–3 días)
**Objetivo:** Poner en producción y dejar todo documentado.  
**Entregables al demandante:**
- Paquete de entrega:
  - URL de producción + usuario demo.
  - Manual de usuario (PDF o página).
  - Manual técnico corto (infra/variables/env, jobs, backup/restore).
  - Plan de soporte (qué, quién, contactos).
- Capacitación express (video 10–15 min o sesión breve).

**Organización interna:**
- Tag de versión (v1.0.0), backup inicial, monitoreo básico.
- Ticketera de soporte (SLA simple).

---

### 7) Cierre y mejora (1–2 días)
**Objetivo:** Aprender y dejar lista la siguiente iteración.  
**Entregables al demandante:**
- Reporte final: objetivos logrados, métricas y pendientes.

**Organización interna:**
- Retrospectiva (qué salió bien, qué mejorar, acciones).
- Archivar proyecto y limpiar pendientes técnicos.

---

## Cronograma sugerido (8–10 semanas)

| Semana | Hito / foco        | Entregables clave                               |
|---:|---|---|
| 0 | Kickoff           | Brief + agenda + set-up herramientas             |
| 1 | Descubrimiento    | Mapa proceso + requerimientos priorizados        |
| 2 | Diseño funcional  | Historias + wireframes + reglas                  |
| 3 | Diseño técnico    | Arquitectura + DER + DoD/DoR + CI base           |
| 4 | Sprint 1          | Demo 1 + feedback + changelog                    |
| 5 | Sprint 2          | Demo 2 + feedback + hardening                    |
| 6 | Sprint 3          | Demo 3 (MVP completo)                            |
| 7 | QA/UAT            | Plan UAT + acta/observaciones                    |
| 8 | Deploy            | Paquete de entrega + capacitación                |
| 9 | Cierre            | Reporte final + retro + roadmap                  |

> Si el tiempo es menor, compactar: (1) Kickoff+Descubrimiento, (2) Diseño (funcional+técnico), (3) 2 sprints, (4) UAT+Deploy, (5) Cierre.

---

## Plantillas (templates)

Las plantillas están en [`/templates`](./templates) listas para copiar y completar:
- `project_brief.md`
- `user_story.md`
- `moscow_prioritization.md`
- `risk_log.md`
- `meeting_minutes.md`
- `uat_plan.md`
- `qa_checklist.md`
- `changelog.md`
- `delivery_package.md`
- `retrospective.md`

> **Historias de usuario:** “Como [rol] quiero [función] para [beneficio]” + Criterios GWT (Dado/Cuando/Entonces). Se usan para planificar, implementar y probar.

---

## Organización del equipo

- **Roles:** PM/Líder (agenda/cliente), Tech Lead (arquitectura), Dev(s), QA/Funcional.  
- **Encuentros:** planning (60’), daily (15’), review+retro por sprint (45’).  
- **Git:** `main` estable, `dev` integración, ramas cortas `feature/*`, PR obligatorio.  
- **Tablero:** Backlog → Ready → In Progress → Code Review → QA → Done.  
- **Métricas sanas:** issues resueltos/sprint, bugs abiertos, lead time, cobertura de criterios de aceptación.

---

## Paquete mínimo para el demandante (cada hito)
1. Documento breve (1–2 páginas) con decisiones, alcance y próximos pasos.  
2. Demo o capturas (evidencia tangible).  
3. Changelog (qué cambió y por qué).  
4. Riesgos/impedimentos (top 3 con plan de mitigación).  
5. Fecha del próximo hito.

---

## Variantes según contexto
- **Proyecto individual:** mismas fases, pero daily asíncrono (nota diaria en el tablero) y review con mentor/cliente.  
- **Proyecto grande:** dividir por “módulos verticales” (ABM Productos, Pedidos, Facturación), cada uno con mini-sprints y demos propias.

---

## Estimación y Costos

Esta guía resume **métodos**, **pasos** y **fórmulas** para estimar **esfuerzo, plazo y costo**. Usá más de un enfoque y triangulá.

### 1) Enfoques de estimación
- **Analogía / Experiencia**: comparar con proyectos similares (ajustar por complejidad/alcance).  
- **Top‑down**: a partir de un presupuesto/plazo global, repartir por módulos. Útil en etapas tempranas.  
- **Bottom‑up (WBS)**: descomponer en tareas pequeñas, estimar cada una y sumar. Mayor precisión.  
- **Tres puntos (PERT)**: estimar **Optimista (O)**, **Más probable (M)**, **Pesimista (P)** por tarea.  
  - Duración esperada: \( E = \frac{O + 4M + P}{6} \)  
  - Desvío estándar: \( \sigma = \frac{P - O}{6} \)  
  - Varianza: \( \sigma^2 = \left(\frac{P - O}{6}\right)^2 \)  
- **Paramétricos**: usar una tasa conocida (p.ej., *story points* → horas vía *velocity*; o LOC, pantallas, casos de uso).  
- **Planning Poker / T‑Shirt sizing**: estimación relativa para priorizar; luego convertir a horas.

### 2) De esfuerzo a costo
Definir **tarifas** y **costos no laborales**:
- Tarifa/hora por rol (Dev, QA, UX, Líder técnico, PM).  
- Costos fijos/variables: licencias, dominios, hosting/nube, integraciones, viajes, equipos.  
- **Fórmula base**:  
  \[ \text{Costo Total} = \sum (\text{Horas por rol} \times \text{Tarifa}) + \text{Costos no laborales} + \text{Contingencia} + \text{Margen} \]

**Contingencia**: 10–30% según riesgo/volatilidad.  
**Margen** (si corresponde a servicios): 10–25% típico educativo/comercial.

### 3) Paso a paso recomendado
1. **Armar WBS** (ver plantilla en `/templates/wbs.md`).  
2. Estimar cada tarea con **PERT** o **horas directas** (si el equipo tiene alta experiencia).  
3. Calcular **esfuerzo total** por rol, **plazo** (en función de disponibilidad/solapamiento) y **costo**.  
4. Agregar **contingencia** según el **log de riesgos**.  
5. Revisar con el demandante: **alcance ↔ costo ↔ plazo**, negociar recortes/incrementos.  
6. Publicar **Presupuesto vX** con supuestos y exclusiones.

### 4) Conversión de Story Points a costo (scrum)
- **Velocity** del equipo: p.ej., 20 puntos / sprint (2 semanas).  
- 1 sprint = 2 semanas = ~80 h por dev (ejemplo).  
- **Horas por punto** ≈ (horas totales del equipo en el sprint) / (puntos completados).  
- **Costo por punto** = (costo del sprint) / (puntos completados).  
  - Útil para presupuestos iterativos/rolling wave.

### 5) Curva S y control
- Contrastar **acumulado planificado vs. real** en horas/costos (Curva S).  
- Métricas: **CPI** (Cost Performance Index) y **SPI** (Schedule Performance Index) si usan valor ganado.  
- Replanificar con datos reales cada sprint (rolling forecast).

### 6) Ejemplo breve (educativo)
**Módulo “Pedidos”** (ABM + lista + filtros + detalle + impresión).  
- WBS (resumen): Análisis (6h), UX (8h), Backend (24h), Frontend (20h), Pruebas (10h), Deploy (4h).  
- Total ≈ 72h. Tarifas: Dev $10/h, QA $8/h, UX $9/h, Líder/PM $12/h.  
- Distribución (ejemplo): Dev 44h, QA 10h, UX 8h, PM 10h.  
- **Costo laboral** ≈ 44*10 + 10*8 + 8*9 + 10*12 = $440 + $80 + $72 + $120 = **$712**  
- Costos no laborales: dominio/hosting proporcional $30.  
- Contingencia 15%: (712+30)*0.15 = $111.3  
- **Total estimado** ≈ $712 + $30 + $111.3 = **$853.3** (redondear).

> Consejos: (a) registrar **supuestos** (p.ej., “sin pasarela de pagos”), (b) explicitar **exclusiones**, (c) versionar el **presupuesto** si cambia el alcance.

---

## Cómo usar este repositorio

1. **Crear un repo nuevo** y copiar este contenido.  
2. Completar [`templates/project_brief.md`](./templates/project_brief.md).  
3. Crear el **Backlog** con historias usando [`templates/user_story.md`](./templates/user_story.md).  
4. Configurar el tablero y ramas Git (`main`, `dev`, `feature/*`).  
5. Usar los workflows provistos.  
6. Hacer **demos periódicas** y mantener el **changelog** por sprint.  
7. Llegado el momento de UAT/Deploy, usar las plantillas de `uat_plan.md` y `delivery_package.md`.

---

## Contribuir
- Proponé mejoras.
- Sumá plantillas o checklists que usen otros equipos.

## Licencia
![License](https://img.shields.io/badge/license-Educational-green)
