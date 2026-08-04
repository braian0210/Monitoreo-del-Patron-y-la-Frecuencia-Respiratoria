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

Para la detección de las variaciones mecánicas asociadas al ciclo ventilatorio, se ha seleccionado el sensor de fuerza por resistencia (FS4), específicamente el modelo FSR 402, este transductor se define como un dispositivo de película gruesa de polímero (PTF) que presenta una disminución en su resistencia eléctrica ante el incremento de la fuerza aplicada sobre su superficie activa.

La elección del FSR 402 responde a los requerimientos de sensibilidad y dimensiones necesarios para el monitoreo no invasivo. A demás el sensor posee una fuerza de actuación mínima de 0,1 N y un rango de sensibilidad que se extiende hasta los 10 N, lo cual es adecuado para captar la presión ejercida por la expansión de la caja torácica durante la inspiración. El FSR tiene un  perfil ultra delgado de 0,55 mm y su área activa de 12,7 mm de diámetro facilitan su integración entre el cuerpo y una banda de sujeción sin alterar el patrón fisiológico del sujeto. La alimentación del sensor se realizó mediante una configuración de divisor de voltaje, que permite convertir la variación de resistencia en una señal de voltaje analógica (V OUT) proporcional a la fuerza mecánica, lo cual facilitó su digitalización a través de una placa ESP32-S3-N16R8.

La adaptación del sensor se fundamenta en la mecánica respiratoria, donde la contracción del diafragma y de los músculos intercostales externos
 provoca un aumento del diámetro transversal y anteroposterior de la caja torácica. Este desplazamiento mecánico es el que se busca capturar para extraer el patrón respiratorio.

 Se anexa imagen del prototipo diseñado:


 <img width="1600" height="1204" alt="image" src="https://github.com/user-attachments/assets/f1568bb1-e51d-4165-9723-7852f22a4eee" />


 
 
El procedimiento de adaptación consiste en situar el área activa del sensor sobre la región torácica o abdominal del sujeto, el sensor se asegura mediante una banda elástica que mantenga una tensión base; de esta forma, cada fase inspiratoria generará un aumento de la fuerza sobre el sensor, disminuyendo su resistencia y produciendo un pico de voltaje en la señal adquirida. Esta configuración permite diferenciar claramente entre la inspiración activa y la espiración, cumpliendo con el objetivo de monitorear la frecuencia respiratoria  en tiempo real.

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

'
clear; close all; clc;

COM = "COM3";            
baudRate = 115200;
Fs = 100;               
duracion_s = 30;
Nmuestras = Fs * duracion_s;

condicion = input('Condición de la captura ("reposo" o "habla"): ', 's');

s = serialport(COM, baudRate);
configureTerminator(s, "LF");
flush(s);


datos = nan(Nmuestras, 1);
fprintf('Iniciando captura de %d segundos (%s)...\n', duracion_s, condicion);

tic;
idx = 1;
while idx <= Nmuestras
    if s.NumBytesAvailable > 0
        linea = readline(s);
        valor = str2double(linea);
        if ~isnan(valor)
            datos(idx) = valor;
            idx = idx + 1;
        end
    end
end
tiempo_transcurrido = toc;
clear s;

t = (0:Nmuestras-1)' / Fs;

nombreArchivo = sprintf('senal_respiratoria_%s.mat', condicion);
save(nombreArchivo, 'datos', 't', 'Fs', 'condicion');
fprintf('Datos guardados en %s (duración real: %.2f s)\n', nombreArchivo, tiempo_transcurrido);


fc_baja = 0.05;   
fc_alta = 5;   
[b, a] = butter(4, [fc_baja fc_alta] / (Fs/2), 'bandpass');
datos_filtrados = filtfilt(b, a, datos - mean(datos));

figure;
subplot(2,1,1);
plot(t, datos);
title(['Señal cruda - ' condicion]);
xlabel('Tiempo (s)'); ylabel('ADC'); grid on;

subplot(2,1,2);
plot(t, datos_filtrados);
title('Señal filtrada (pasa-banda Butterworth 0.1-1.0 Hz)');
xlabel('Tiempo (s)'); ylabel('Amplitud'); grid on;

N = length(datos_filtrados);
Y = fft(datos_filtrados);
f = (0:N-1) * (Fs/N);
P = abs(Y/N);
P = P(1:floor(N/2)+1);
f = f(1:floor(N/2)+1);

figure;
plot(f, P);
xlim([0 2]);
xlabel('Frecuencia (Hz)');
ylabel('|P(f)|');
title(['Espectro de frecuencia - ' condicion]);
grid on;

mascara = f > 0.05;
[~, idxMax] = max(P(mascara));
f_validas = f(mascara);
f_dominante = f_validas(idxMax);
fr_resp = f_dominante * 60; 

fprintf('Frecuencia dominante: %.3f Hz (%.1f resp/min)\n', f_dominante, fr_resp);


'

2. Capturar 30 segundos de señal respiratoria bajo las condiciones establecidas
en el paso 5 de la parte A (incisos “a” y “b”). Recuerde guardar en cada caso el
correspondiente archivo .MAT.



<img width="935" height="297" alt="image" src="https://github.com/user-attachments/assets/c2c8b1d3-c98b-4ca1-81c0-a838b5430aee" />



<img width="938" height="301" alt="image" src="https://github.com/user-attachments/assets/0db29319-3e1e-4173-a6a7-e37368a71e5d" />




3. De ser necesario, aplique los filtros correspondientes para mejorar la calidad
de ambas señales. Especifique el tipo de filtro (pasa-bajas, pasa banda) y la(s)
frecuencia(s) de corte.

4. Obtenga la representación en frecuencia de ambas señales e identifique la
frecuencia dominante en cada caso.ç

Para el caso en reposo:


<img width="1123" height="747" alt="espectro_profereposo" src="https://github.com/user-attachments/assets/507d0391-bd64-46f6-b1b2-bf149838ffaf" />


Para el caso hablando:


<img width="1123" height="747" alt="espectro_profehabla" src="https://github.com/user-attachments/assets/11ae9788-a06b-4bc5-89d9-b6a7b9ae6da7" />


PARTE C

• Pregunta 1: ¿Son los patrones respiratorios y frecuencias respiratorias
iguales o diferentes en cada caso? ¿A qué se debe esto?

• Pregunta 2: ¿Cuáles serían las ventajas y desventajas de emplear múltiples
sensores para el monitoreo del proceso respiratorio? ¿Cuáles podrían ser
las razones?

#Análisis de Resultados

#Conclusiones 

#Referencias 

[1] Universidad Militar Nueva Granada, “Guía de Preparación Práctica de Laboratorio: Monitoreo del patrón y frecuencia respiratoria,” Ing. Alejandra Rosero Cárdenas, 2025.

[2] R. D. Camargo R., “Signo vital Respiración,” Acta Colombiana de Cuidado Intensivo, vol. 11, no. 2, pp. 11-21, 2010.

[3] R. D. Camargo R., “Signos Vitales,” Acta Colombiana de Cuidado Intensivo, vol. 11, no. 2, pp. 179-181, 2011.

[4] H. Puppo, R. Fernández, y G. Hidalgo, “Función Pulmonar: Fisiología de los músculos de la respiración,” Revista Neumología Pediátrica, vol. 16, no. 4, pp. 146-151, 2021.

[5] J. Canet, “Ventilación y Mecánica Respiratoria,” en Fisiología Respiratoria, pp. 1-2.

[6] Interlink Electronics, “FSR 402 Data Sheet: Force Sensing Resistor,” 2010.

[7] W. Cristancho Gómez, Fisiología respiratoria: Lo esencial en la práctica clínica, Bogotá: Editorial El Manual Moderno.

[8] J. B. West, Fisiología del sistema respiratorio: Conceptos fundamentales, fragmentos de capítulos y capturas de pantalla integradas en la práctica de laboratorio.
 
 [9] A. F. Tresguerres, C. Ariznavarreta, V. Cachofeiro, D. Cardinali, E. Escrich, P. Gil-Loyzaga, V. Lahera Juliá, F. Mora Teruel, M. Romano Pardo y J. Tamargo Menéndez, Fisiología humana, 3.ª ed. Madrid, España: McGraw-Hill Interamericana de España, 2005.

