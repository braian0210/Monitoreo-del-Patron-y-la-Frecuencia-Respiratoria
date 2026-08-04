# Monitoreo-del-Patron-y-la-Frecuencia-Respiratoria
#Introducción

La respiración es un proceso fisiológico esencial para la vida que permite el intercambio gaseoso a través de la membrana alveolocapilar, suministrando oxígeno (O₂) a los tejidos para el metabolismo celular y eliminando el dióxido de carbono (CO₂) resultante.
Este proceso se fundamenta en un ciclo mecánico compuesto por una fase de inspiración activa y una de espiración, que en condiciones normales de reposo es pasiva
. El sistema respiratorio se divide funcionalmente en los pulmones los cuales son los encargados de la conducción y el intercambio, y la bomba ventilatoria es aquella que esta constituida por los centros respiratorios, los nervios periféricos, la estructura ósea del tórax y los músculos respiratorios.

La mecánica pulmonar está regida por propiedades físicas críticas como la elasticidad, que permite al sistema volver a su posición inicial tras la deformación; la viscosidad, relacionada con la fricción interna durante el flujo de aire; y la tensión superficial en la capa alveolar
. El diafragma actúa como el principal músculo agonista de la inspiración, desplazándose para expandir la cavidad torácica y reducir la presión pleural, lo que genera el gradiente de presión necesario para la entrada de aire
. El equilibrio entre la capacidad neuromuscular de esta bomba y las cargas elásticas y resistivas impuestas por el sistema es fundamental para evitar la fatiga muscular y la consecuente falla ventilatoria
.
Clínicamente, la frecuencia respiratoria (RR) se reconoce como un signo vital de alta sensibilidad para el monitoreo de la estabilidad del paciente
. Alteraciones en este parámetro son marcadores precoces de patologías graves, permitiendo predecir eventos como paros cardíacos o ingresos a unidades de cuidado intensivo con mayor antelación y especificidad que otros signos como el pulso o la presión arterial
. No obstante, el patrón respiratorio es altamente variable y se ve influenciado por factores metabólicos, neurológicos y actividades voluntarias como la verbalización o el habla
,
.
En el ámbito de la ingeniería biomédica, la medición precisa de estas variables se logra mediante sistemas de instrumentación que integran sensores capaces de capturar variaciones físicas del proceso fisiológico
. Los sensores de detección de fuerza por resistencia (FSR), por ejemplo, permiten convertir la presión mecánica ejercida por la expansión torácica en señales eléctricas mediante configuraciones de divisor de voltaje. El desarrollo de estos sistemas no solo permite el seguimiento clínico continuo, sino que también facilita el estudio de cómo tareas específicas, como la fonación, alteran la relación temporal entre las fases del ciclo respiratorio


#Objetivos

Objetivo General
• Evaluar la influencia del habla o verbalización sobre el
patrón respiratorio.

Objetivos Específicos
• Reconocer las variables físicas principalmente involucradas en el proceso
respiratorio.

• Desarrollar un sistema que extraiga el patrón respiratorio y la frecuencia
respiratoria.

• Identificar tareas de verbalización a partir del patrón y/o la frecuencia
respiratoria.

#Metogología

PARTE A

1. Llevar a cabo una revisión de la literatura sobre el proceso respiratorio, con
énfasis en el reconocimiento de las variables físicas principalmente
involucradas. En caso de utilizar modelos de IA generativa (e.g., ChatGPT)
debe verificar la información contra una fuente confiable (e.g., libros, manuales,
informes técnicos).

2. Seleccionar el sensor que considere más adecuado para medir la variable de
interés y, de esa forma, capturar las variaciones producidas por el proceso
respiratorio. Considere un voltaje de alimentación de +3.3 a +5 VDC, en el
caso de tratarse de un sensor pasivo. Medite sobre cómo adaptar el sensor al
cuerpo del sujeto de prueba para capturar la señal con un mínimo de
interferencia.

3. Diseñe y elabore un sistema que acondicione y digitalice la señal respiratoria
utilizando para ello el sensor previamente elegido. Puede utilizar el conversor
análogo-digital integrado en la placa Arduino.

4. Coloque el sensor sobre alguno de los miembros del equipo para verificar la
operatividad del sistema.

5. Empleando la función “Serial Plotter” del menú “Herramientas” del entorno de
programación, tome capturas de pantalla que muestren la señal:

a. En reposo (cuente manualmente el número de veces que el sujeto inhala o
exhala).

b. Mientras el sujeto de prueba habla o lee.

PARTE B

1. Diseñe y elabore un breve código en MATLAB que permita la captura
temporizada de la señal respiratoria adquirida por el sistema que Ud. ha
construido y probado.

2. Capturar 30 segundos de señal respiratoria bajo las condiciones establecidas
en el paso 5 de la parte A (incisos “a” y “b”). Recuerde guardar en cada caso el
correspondiente archivo .MAT.

3. De ser necesario, aplique los filtros correspondientes para mejorar la calidad
de ambas señales. Especifique el tipo de filtro (pasa-bajas, pasa banda) y la(s)
frecuencia(s) de corte.

4. Obtenga la representación en frecuencia de ambas señales e identifique la
frecuencia dominante en cada caso.

PARTE C

• Pregunta 1: ¿Son los patrones respiratorios y frecuencias respiratorias
iguales o diferentes en cada caso? ¿A qué se debe esto?

• Pregunta 2: ¿Cuáles serían las ventajas y desventajas de emplear múltiples
sensores para el monitoreo del proceso respiratorio? ¿Cuáles podrían ser
las razones?

#Análisis de Resultados

#Conclusiones 

#Referencias 



