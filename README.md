# Tecnologías Emergentes enfocadas en Seguridad de Visitantes

Investigación de proyecto basado en mejorar el seguimiento y la seguridad de visitantes en los senderos de alta montaña del Parque Mahuida, en la comuna de La Reina, Santiago de Chile.

Proyecto de investigación aplicada que busca abordar la falta de trazabilidad en tiempo real de los visitantes que recorren los senderos de alta montaña del Parque Mahuida (La Reina, Santiago), zona con el porcentaje más alto de riesgo de deslizamientos de la Región Metropolitana. A partir de datos oficiales, entrevistas a guardaparques y registro en terreno, se analiza el sistema actual de control de acceso y seguimiento, y se exploran alternativas tecnológicas que permitan monitorear en tiempo real la ubicación y estado de las personas en ruta.

## Integrantes

- Victoria Atala
- Valeria Cheetham
- Maximiliano
- Laura Hoppe

---

## Avance 20-08-2026

### 1. Problemática y enmarque

#### Problemática

El Parque Mahuida reconoce oficialmente que su zona de alta montaña presenta riesgo de deslizamientos, pero no cuenta con un sistema que permita saber en tiempo real qué personas están recorriendo los senderos ni si alguien se atrasó en su retorno.

#### Contexto

La Reina tiene un 48,1% de su superficie en zonas de riesgo de deslizamiento, el porcentaje más alto de la Región Metropolitana, y el sector montañoso del Parque Mahuida está identificado dentro de esa zona. En rutas de alta dificultad como Cerro La Cruz (2.554 msnm, 14,2 km, hasta 10 horas de ascenso), el registro de visitantes sigue dependiendo de anotaciones manuales, planillas Excel recientes y llamadas telefónicas puntuales a media tarde, sin ningún mecanismo de trazabilidad continua durante el recorrido.

#### Enmarques

1. **Riesgo identificado, control básico** — el municipio reconoce el riesgo, pero el control de las personas en terreno depende de señalética y criterio humano, no de datos en tiempo real.
2. **Se sabe dónde está el peligro, no dónde están las personas** — existe mapa de zonas de riesgo, pero no información en tiempo real sobre quién está recorriendo esas zonas.

### 2. Datos cualitativos y cuantitativos provenientes de fuentes

#### Datos cuantitativos

##### PLADECO La Reina 2019-2025

La Reina tiene un 48,1% de su superficie en zonas con riesgo de deslizamientos de tierra, el porcentaje más alto de la Región Metropolitana. Entre 2014 y 2019 hubo 7 incendios forestales en la comuna, que afectaron aproximadamente 11,5 hectáreas, principalmente en la zona precordillera cercana al parque.

* Fuente: PLADECO La Reina 2019-2025

##### Parque Mahuida / Municipalidad de La Reina (información oficial)

El sendero Cerro La Cruz llega a 2.554 msnm, con 14,2 km y hasta 10 horas de duración — la ruta de mayor riesgo del parque. Para señalizar solo 10 km de senderos de montaña, el parque trasladó 80 estacas (800 kilos) en 3 viajes de helicóptero.

* Fuente: Parque Mahuida y Municipalidad de La Reina (información oficial)

##### Entrevistas propias a guardaparques (20-08-2026)

Según los guardaparques Leo y Fernanda Barrios, los rescates bajaron de un promedio de 2 a 3 casos por mes (con guardaparque único, antes del equipo actual) a 1-2 casos cada 3 meses tras la incorporación de un equipo completo hace un año.

* Acotación: Este es un dato observacional recogido en entrevista, no una cifra oficial publicada por el parque.

#### Datos cualitativos

##### Entrevista Leo, guardaparque Parque Mahuida (20-08-2026)

Leo explicó el funcionamiento actual del registro de visitantes y del seguimiento en ruta. Según el profesional, el registro varía según el día y la dificultad del sendero: en senderos de baja dificultad solo se anotan datos básicos, mientras que en rutas de alta montaña (Cerro La Cruz, Morro La Reina, Cerro San Ramón) se exige además registro en Socorro Andino y se establece una hora límite de bajada, verificada mediante una llamada telefónica entre la 1 y 2 PM.

El guardaparque confirmó explícitamente que no existe seguimiento en tiempo real: "no sabemos en vivo, no tenemos seguimiento en vivo." También describió un sistema informal de puntos de corte por tiempo en rutas de alta dificultad (por ejemplo, un máximo de 45 minutos para llegar a un punto de control), que actualmente está "en marcha blanca" y aún no ha sido publicado formalmente por el parque.

Respecto a la cobertura de señal, indicó que varía según la compañía telefónica: WOM tendría la mejor cobertura dentro del parque, mientras que Movistar sería la más deficiente, con visitantes que pierden señal desde el inicio de algunos senderos. La comunicación con quienes están en ruta depende exclusivamente de llamadas desde un celular exclusivo del equipo de guardaparques.

Sobre la exigencia de grupos mínimos de dos personas y mayoría de edad para Cerro La Cruz, Leo señaló que no se trata de una obligación formal sino de una recomendación de precaución, y que el 100% de los incidentes atendidos correspondió a personas que iban acompañadas.

##### Entrevista Fernanda Barrios, guardaparque Parque Mahuida (20-08-2026)

Fernanda confirmó de manera independiente varios de los puntos señalados por Leo. Indicó que el sistema de registro cambió de papel a una planilla Excel hace aproximadamente un mes, y que anteriormente solo se aplicaba un registro más riguroso a quienes iban a senderos de altas cumbres. Señaló textualmente que "sería lo ideal tener también un sistema, una plataforma", mientras el equipo intenta automatizar manualmente la planilla con apoyo de herramientas de inteligencia artificial genéricas.

Respecto al seguimiento en ruta, coincidió en que "no sabemos dónde está hasta que sale", y describió que en el sendero Guayacán —donde la gente tiende a perderse con mayor frecuencia— el único método de apoyo disponible es que los visitantes envíen fotografías de su ubicación para ser guiados telefónicamente.

Sobre la cobertura de comunicación, indicó que la señal celular es intermitente y varía por compañía, y añadió un dato adicional relevante: incluso las radios internas del equipo de guardaparques pierden cobertura dentro del bosque, lo que dificulta la comunicación entre el personal en terreno y la administración del parque.

* Acotación: Ambas entrevistas fueron realizadas en terreno como parte del levantamiento propio del equipo, y se complementan con registro fotográfico del parque (cuaderno de registro, señalética y puntos de control) disponible en la carpeta `fotos/`.

##### Reglamento del Parque Mahuida (información oficial)

El parque exige credencial presencial e intransferible para el ingreso, con límite de un acompañante sin costo adicional. Se prohíbe pernoctar, encender fuego, arrancar vegetación y abandonar mascotas; estas deben portar correa y su acceso está limitado hasta el punto conocido como "la antena". El horario general de funcionamiento es de 8:00 a 19:00 horas, con horarios de ascenso diferenciados según sendero (por ejemplo, Cerro La Cruz hasta las 9:00 AM).

* Acotación: El reglamento evidencia un control riguroso sobre el acceso al parque, que contrasta con la ausencia de seguimiento una vez que el visitante ya se encuentra en el sendero.
