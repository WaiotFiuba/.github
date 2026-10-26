# Waiot Intelligence

Prototipo desarrollado como Trabajo Profesional de Ingeniería Informática en la
Facultad de Ingeniería de la Universidad de Buenos Aires (FIUBA), en colaboración con
Alliansys.

[Waiot](https://www.waiot.site/), desarrollada por
[Alliansys](https://alliansys.com.ar/), es una plataforma que utiliza sensores
para monitorear el llenado de contenedores de residuos urbanos, visualizar el
estado de la red y generar rutas de recolección. A partir de reuniones con su
equipo se identificaron dos oportunidades de mejora, que Waiot Intelligence
desarrolla como base para su futura integración con la plataforma:

- **Proyección del llenado.** Estima cómo evolucionaría el llenado de cada sitio
  sin recolección y anticipa cuándo alcanzaría un nivel crítico. Compara un modelo
  base operativo, construido a partir de patrones históricos, con Chronos-2 Small,
  un modelo preentrenado de series temporales.
- **Redistribución de contenedores.** Analiza la utilización histórica de los
  sitios y propone traslados de contenedores para atender desbalances de
  capacidad y situaciones de saturación recurrente. Incluye un entorno What-If
  para explorar el impacto de las recomendaciones antes de aplicarlas.

El prototipo no desarrolla ni modifica los algoritmos de generación de rutas de
Waiot. Para evaluarlo se construyó un gemelo digital de la red de contenedores de
la Ciudad Autónoma de Buenos Aires, que combina datos oficiales de la Ciudad con
telemetría sintética.

## Repositorios

| Repositorio | Contenido |
| --- | --- |
| [backend](https://github.com/WaiotFiuba/backend) | API (FastAPI + PostgreSQL/PostGIS): red de contenedores y sitios, ingesta de telemetría, módulos de proyección y redistribución, y el simulador de telemetría. |
| [frontend](https://github.com/WaiotFiuba/frontend) | Aplicación web (React + TypeScript): mapa de la red, vista proyectada, entorno What-If y control de las simulaciones. |

## Documentación

**Backend**

- [README](https://github.com/WaiotFiuba/backend/blob/main/README.md): cómo
  levantar el backend, configuración, API y despliegue.
- [Datos y red de contenedores](https://github.com/WaiotFiuba/backend/blob/main/docs/DATOS.md):
  cómo se arma la red a partir de datos abiertos de CABA y cómo se guarda latelemetría.
- [Proyección del llenado](https://github.com/WaiotFiuba/backend/blob/main/docs/PROYECCION.md):
  modelos, historial y evaluación.
- [Redistribución de contenedores](https://github.com/WaiotFiuba/backend/blob/main/docs/REDISTRIBUCION.md):
  enfoques, estrategias y entorno What-If.
- [Hosting y despliegue](https://github.com/WaiotFiuba/backend/blob/main/docs/HOSTING.md).

**Simulador**

- [README](https://github.com/WaiotFiuba/backend/blob/main/simulator/README.md):
  cómo ejecutar el simulador y correr una simulación.
- [Funcionamiento](https://github.com/WaiotFiuba/backend/blob/main/simulator/FUNCIONAMIENTO.md):
  cómo se generan la demanda, los perfiles de zona y las recolecciones.

**Frontend**

- [README](https://github.com/WaiotFiuba/frontend/blob/main/README.md): cómo
  levantar la aplicación web.

## Equipo

- Joaquín Álvarez
- Valentín Brizuela
- Isaías Augusto Cabrera
- Lucas Pérez Esnaola
