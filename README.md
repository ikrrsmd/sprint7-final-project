# Análisis de uso de servicios móviles - ConnectaTel

## Objetivo
Entender cómo usan los clientes de ConnectaTel (México y Colombia) las llamadas y los mensajes, detectar usos atípicos y segmentar a los clientes para mejorar la oferta de planes.

## Datos
- `plans.csv`: planes disponibles (Básico y Premium).
- `users_latam.csv`: 4,000 clientes (edad, ciudad, fecha de registro, plan).
- `usage.csv`: 40,000 registros de llamadas y mensajes.

## Proceso
1. Carga y revisión de los datasets.
2. Limpieza: sentinel -999 en edad (55 filas), "?" en ciudad (565 usuarios sin dato en total), fechas imposibles de 2026 (40 filas) y revisión de nulos.
3. Agregación del uso por usuario (mensajes, llamadas y minutos).
4. Análisis de distribuciones y outliers (método IQR).
5. Segmentación por nivel de uso y por edad.

## Hallazgos principales
- 73.6% de los usuarios tiene uso medio, 19.5% uso bajo y 7.0% uso alto.
- El uso es casi igual entre los planes Básico y Premium y entre grupos de edad.
- Hay usuarios con uso extremo, sobre todo en minutos (109 usuarios, 2.7%), que conviene revisar por posible fraude.
- 466 usuarios (11.65%) se han dado de baja.

## Recomendaciones
Revisar el valor del plan Premium, crear una oferta para uso alto, impulsar al uso bajo y monitorear los consumos extremos.

## Cómo ejecutar
Abrir el notebook en Jupyter con los tres CSV disponibles en la ruta `/datasets/`.
