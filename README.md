# Tecnologías Emergentes enfocadas en Seguridad de Visitantes
Investigación de proyecto basado en mejorar el seguimiento y la seguridad de visitantes en los senderos de alta montaña del Parque Mahuida, en la comuna de La Reina, Santiago de Chile.

Proyecto de investigación aplicada que busca abordar la falta de trazabilidad en tiempo real de los visitantes que recorren los senderos de alta montaña del Parque Mahuida (La Reina, Santiago), zona con el porcentaje más alto de riesgo de deslizamientos de la Región Metropolitana. A partir de datos oficiales, entrevistas a guardaparques y registro en terreno, se analiza el sistema actual de control de acceso y seguimiento, y se exploran alternativas tecnológicas que permitan monitorear en tiempo real la ubicación y estado de las personas en ruta.

## Integrantes

* Victoria Atala
* Valeria Cheetham
* Maximiliano Greve
* Laura Hoppe

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

### 3. Desglose de entrevistas por pregunta, con clasificación cuali/cuanti

Aplicando la clasificación de datos vista en clase (separar cada dato en cuantitativo o cualitativo antes de analizar), se desglosan a continuación ambas entrevistas pregunta por pregunta.

#### Entrevista a Leo, guardaparque Parque Mahuida

**Pregunta 1 — Frecuencia de extravíos y rescates**

¿Con qué frecuencia se pierde o se atrasa gente en los senderos, sobre todo en Cerro La Cruz? ¿Han tenido que salir a buscar a alguien en el último tiempo?

El equipo actual de guardaparques lleva un año completo trabajando; antes hubo un período de prueba con un solo guardaparque. En esa etapa previa, los rescates/extravíos ocurrían entre 2 y 3 veces por mes. Desde que está el equipo completo, la cifra bajó a 1-2 casos cada 3 meses. Las causas actuales suelen ser fortuitas: torceduras de tobillo, caídas o deshidratación en época estival por mal manejo del agua.

| Dato | Tipo |
|---|---|
| Antigüedad del equipo actual (1 año) | Cuanti |
| Rescates antes del equipo completo: 2-3/mes | Cuanti |
| Rescates actuales: 1-2 cada 3 meses | Cuanti |
| Causas típicas (torcedura, caída, deshidratación) | Cuali |
| Explicación de por qué bajó (mejores indicaciones al ingreso) | Cuali |

**Pregunta 2 — Registro actual de entrada y salida**

¿Cómo funciona hoy el control de quién entra y sale? ¿Queda registrado en papel, en el QR, o de alguna otra forma?

El flujo de visitantes es muy desigual: de jueves a domingo llegan entre 300 y 400 personas, mientras que de lunes a miércoles a veces no se superan las 50. En días de baja afluencia, los porteros logran hacer un registro manual completo. En días de alta afluencia, hay 1 a 2 personas dedicadas al registro. En senderos de baja dificultad solo se anota nombre y sendero; en senderos de alta dificultad (Cerro La Cruz, Morro La Reina, Cerro San Ramón) se exige además registro en Socorro Andino, hora límite de bajada y una llamada de verificación entre la 1 y 2 PM.

| Dato | Tipo |
|---|---|
| Visitantes fin de semana: 300-400 | Cuanti |
| Visitantes entre semana: menos de 50 | Cuanti |
| Personal dedicado al registro (1 entre semana, 2 fin de semana) | Cuanti |
| Horario de llamada de verificación (1-2 PM) | Cuanti |
| Diferencia de exigencia de registro según dificultad del sendero | Cuali |
| Explicación del porqué del registro diferenciado | Cuali |

**Pregunta 3 — Seguimiento en ruta**

Una vez que la persona ya entró al sendero, ¿tienen alguna forma de saber dónde va o si sigue el ritmo normal, o solo se sabe cuando vuelve a la entrada?

El guardaparque afirmó explícitamente: "no sabemos en vivo, no tenemos seguimiento en vivo." Solo se sabe a qué sendero fue cada persona por el registro de entrada. Existe un sistema informal de "puntos de corte por tiempo" en senderos de alta dificultad: por ejemplo, un máximo de 45 minutos para llegar al punto conocido como "la antena"; si el visitante se demora más, se asume que no está en condiciones de completar la ruta. Este sistema está "en marcha blanca" y aún no se ha publicado en la página web del parque.

| Dato | Tipo |
|---|---|
| Punto de corte de 45 minutos hasta "la antena" | Cuanti |
| Tiempo promedio de Cerro La Cruz (5-6 horas) | Cuanti |
| "No sabemos en vivo, no tenemos seguimiento en vivo" (cita textual) | Cuali |
| Sistema de puntos de corte está "en marcha blanca", no publicado | Cuali |
| Apoyo actual: mapas físicos, señalética, presencia en app SUDA | Cuali |

**Pregunta 4 — Cobertura de señal y comunicación**

¿Cómo es la cobertura de señal (celular/radio) en la zona alta? ¿Cómo se comunican con alguien que está en la montaña si pasa algo?

El uso de radios es muy bajo (aproximadamente 1 de cada 100 personas). La cobertura celular varía por compañía: WOM tendría la mejor cobertura (llega incluso más allá de Morro La Reina hacia Cerro La Cruz), Entel sería regular, y Movistar la peor, con visitantes que pierden señal desde el inicio mismo de los senderos. La comunicación con quienes están en ruta se hace exclusivamente por teléfono, desde un celular exclusivo del equipo de guardaparques. De aproximadamente 500 visitantes un sábado, solo 20 a 40 van a senderos de alta dificultad, lo que representa un máximo de 40 llamadas de verificación en un día.

| Dato | Tipo |
|---|---|
| Uso de radios: ~1 de cada 100 personas | Cuanti |
| Ranking de cobertura por compañía (WOM > Entel > Movistar) | Cuanti (categórico) |
| Visitantes a senderos de alta dificultad: 20-40 de 500 | Cuanti |
| Llamadas de verificación por día: hasta 40 | Cuanti |
| Explicación de por qué Movistar falla desde el inicio del sendero | Cuali |
| Único canal de comunicación: teléfono del equipo | Cuali |

**Pregunta 5 — Regla de grupo mínimo y mayoría de edad**

Lo de los grupos mínimos de 2 personas y el requisito de mayoría de edad para Cerro La Cruz, ¿de dónde salió esa regla? ¿Ha habido algún incidente que la haya motivado?

Según Leo, no es una obligación formal, sino una recomendación de precaución que probablemente surgió de un criterio informal de una administración anterior del parque, cuya página web no se actualiza hace años. Si una persona con experiencia llega sola, no se le impide el ingreso. El 100% de los incidentes atendidos por el equipo correspondió a personas que iban acompañadas, y el aviso siempre llegó a través de un acompañante, familiar o amigo cercano.

| Dato | Tipo |
|---|---|
| 100% de los incidentes atendidos fue con personas acompañadas | Cuanti |
| La regla no es obligación, es sugerencia (aclaración explícita) | Cuali |
| Página web del parque no se actualiza hace años | Cuali |
| Lógica detrás de la sugerencia (tener apoyo en primeros auxilios) | Cuali |

---

#### Entrevista a Fernanda Barrios, guardaparque Parque Mahuida

**Pregunta 1 — Frecuencia de extravíos y rescates**

¿Con qué frecuencia se pierde o se atrasa gente en los senderos, sobre todo en Cerro La Cruz? ¿Has tenido que salir a buscar a alguien en el último tiempo?

Según Fernanda, la frecuencia de personas perdidas es baja, porque el sendero está bien señalizado y se dan indicaciones al ingreso, además de pedir a los visitantes llevar la ruta descargada. A ella personalmente no le ha tocado hacer un rescate. En incidentes graves de altas cumbres, el parque no realiza la evacuación: da aviso a Socorro Andino, que es quien evacúa; el equipo del parque solo apoya con primeros auxilios mientras llega ese apoyo externo.

| Dato | Tipo |
|---|---|
| A Fernanda no le ha tocado hacer rescates directamente | Cuanti (frecuencia nula en su experiencia) |
| Práctica de pedir ruta descargada a los visitantes | Cuali |
| Protocolo: Socorro Andino evacúa, el parque solo asiste | Cuali |
| Explicación de por qué la frecuencia es baja (señalética + indicaciones) | Cuali |

**Pregunta 2 — Registro actual de entrada y salida**

¿Cómo funciona hoy el control de quién entra y sale? ¿Queda registrado en papel, en el QR, o de alguna otra forma?

El sistema cambió hace aproximadamente un mes. Antes todo se anotaba en hoja de papel, y solo a quienes iban a rutas de altas cumbres (Tascún) se les hacía un registro más riguroso, con declaración jurada y aviso a Socorro Andino. Ahora todos los senderos se registran en una planilla Excel. Fernanda señaló textualmente: "sería lo ideal que tuviésemos también un sistema, una plataforma", y comentó que el equipo intenta automatizar manualmente el Excel con apoyo de herramientas de inteligencia artificial genéricas, pero sin contar con un sistema real.

| Dato | Tipo |
|---|---|
| Cambio de papel a Excel: hace ~1 mes | Cuanti (temporalidad) |
| Registro previo diferenciado solo para altas cumbres | Cuali |
| "Sería lo ideal tener una plataforma" (cita textual) | Cuali |
| Uso de IA genérica para intentar automatizar el Excel | Cuali |

**Pregunta 3 — Seguimiento en ruta**

Una vez que la persona ya entró al sendero, ¿tienen alguna forma de saber dónde va o si sigue el ritmo normal, o solo se sabe cuando vuelve a la entrada?

Fernanda confirmó, de forma independiente a Leo: "no sabemos dónde está hasta que sale." Dependen del teléfono del visitante, a quien se le pide anotar el número del parque. En el sendero Guayacán, donde la gente tiende a perderse con más frecuencia, el único apoyo disponible es que los visitantes envíen fotos de su ubicación para ser guiados. A quienes van a altas cumbres se les pide comunicarse a partir de la 1 PM, con un horario máximo de retorno; desde la tarde el equipo llama para verificar estado y ubicación.

| Dato | Tipo |
|---|---|
| Horario de inicio de llamadas de verificación (1 PM) | Cuanti |
| "No sabemos dónde está hasta que sale" (cita textual) | Cuali |
| Guayacán identificado como el sendero donde más se pierde la gente | Cuali |
| Método improvisado: visitantes envían fotos para ser guiados | Cuali |

**Pregunta 4 — Cobertura de señal y comunicación**

¿Cómo es la cobertura de señal, como celular o radio, en la zona alta? ¿Cómo se comunican con alguien que está en la montaña?

La señal es intermitente y varía según compañía; Fernanda usa Claro y la describe como no muy buena, mientras que WOM andaría mejor (coincide con lo señalado por Leo). Agregó un dato nuevo: ni siquiera las radios internas del equipo de guardaparques funcionan bien dentro del bosque — incluso el personal de la administración, ubicado más abajo, puede no recibir las comunicaciones de radio desde el sendero.

| Dato | Tipo |
|---|---|
| Comparación de cobertura por compañía (Claro deficiente, WOM mejor) | Cuanti (categórico) |
| Fallas de radio interna dentro del bosque | Cuali |
| La administración (abajo) a veces no recibe las radios del sendero | Cuali |

**Pregunta 5 — Regla de grupo mínimo y mayoría de edad**

Lo de los grupos mínimos de dos personas y el requisito de mayoría de edad para Cerro La Cruz, ¿de dónde salió esa regla? ¿Ha habido algún incidente que la haya motivado?

Fernanda coincidió con Leo: no es una regla formal, sino una recomendación de precaución, pensada sobre todo para personas sin experiencia. Si el guardaparque evalúa que la persona tiene las capacidades y conocimientos necesarios, no se le pone problema para ir sola. La única exigencia real y más estricta aplica a menores de edad, quienes sí deben ir acompañados de un adulto responsable por temas de responsabilidad ante un eventual accidente.

| Dato | Tipo |
|---|---|
| Confirmación cruzada con Leo: no es obligación, es sugerencia | Cuali |
| Exigencia real y distinta para menores de edad (adulto responsable) | Cuali |
| Criterio de evaluación caso a caso por parte del guardaparque | Cuali |
