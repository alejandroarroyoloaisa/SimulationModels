# Modelos de Simulación en SIMIO

Este repositorio contiene una colección de proyectos de simulación desarrollados con el software **SIMIO**. Los proyectos están organizados en dos secciones principales: una introducción a los modelos de simulación a través de una serie de casos prácticos, y un proyecto final que aborda un caso de estudio más complejo.

---

## Introducción a la Simulación

Esta sección incluye tres simulaciones de práctica que sirven como introducción al software SIMIO y a los conceptos fundamentales de la simulación.

### Simulación 1: Modelo de una Heladería 

Este modelo simula el funcionamiento de una pequeña heladería. Los clientes llegan, son atendidos por dos dependientes para pedir su helado, y luego se dirigen a una caja para pagar. Las distribuciones de probabilidad utilizadas para los eventos son:
* **Entrada de clientes**: Exponencial (0.5) minutos.
* **Servir Helado**: Triangular (0.4, 0.9, 1.5) minutos.
* **Pagar Helado**: Triangular (0.3, 0.4, 0.6) minutos.

### Simulación 2 y 3: Modelo de un Aeropuerto 

Este modelo se desarrolla en dos partes y simula el flujo de pasajeros en un aeropuerto.

* **Parte 1**: Se centra en los desplazamientos de los pasajeros desde el check-in hasta el control de seguridad para determinar el número óptimo de operadores. Las distribuciones de probabilidad son Exponencial (1) minutos para la llegada de pasajeros y Uniforme (2.5) minutos para el check-in.

* **Parte 2**: Esta versión incorpora diferentes tipos de pasajeros (con prioridad, estándar y en línea) para hacer el modelo más realista. Los pasajeros eligen una de las tres rutas disponibles según una probabilidad específica: 10% para la ruta de check-in prioritario, 70% para el check-in estándar y 20% para el check-in en línea.

---

## Simulación Final: Simulación de un Hotel

Este proyecto final consiste en un modelo de simulación completo del hotel **HOTEL EXPRESS**. El objetivo principal es optimizar la satisfacción de los clientes, que se mide por el tiempo total de espera en cada servicio.

### Sistema Real y Objetivos
El hotel tiene dos tipos de clientes:
* **Huéspedes**: Personas que se hospedan y utilizan todos los servicios (recepción, ascensor, habitación, restaurante).
* **Comensales**: Clientes no residentes que solo visitan el restaurante.

El proyecto busca responder dos preguntas principales:
1.  ¿Cuál es la mejor configuración de servicios (recepcionistas, ascensores, habitaciones y mesas de restaurante) para minimizar los tiempos de espera de los huéspedes? 
2.  ¿Cómo influye en la satisfacción de los huéspedes el permitir el acceso al restaurante a los clientes no residentes? 

### Experimentos y Conclusiones
Se realizaron 36 experimentos variando el número de recepcionistas, ascensores, habitaciones, mesas de restaurante, y limpiadores.

El mejor escenario de configuración encontrado para maximizar la satisfacción del cliente (minimizando el tiempo de espera) es el siguiente:
* **Número de recepcionistas**: 2
* **Número de ascensores**: 3
* **Número de habitaciones**: 16
* **Mesas del restaurante**: 12
* **Número de limpiadores**: 3
* **Tiempo de simulación**: 1 mes

El estudio concluye que, con esta configuración, el tiempo de espera medio total es de aproximadamente 2.067 horas. Además, se determinó que permitir el acceso a comensales externos no influye significativamente en la satisfacción de los huéspedes, lo que permite al hotel generar ingresos adicionales.
