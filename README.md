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

El proceso respiratorio es uno de los mas importantes dentro de la fisiologia humana pues de su resultado depende la oxigenacion de las celulas del cuerpo, este proceso de ventilacion tiene como objetivo el transporte de gases  desde el entorno de la persona, hasta los alveolos y viseras.[5] El proceso respiratorio puede ser tanto activo que es cuando se realiza por accion de musculos respiratorios del individuo (el diafragma, los intercostales y musculos accesorio como los escalenos y esternoicleo mastoideo)[10], y pasivo/mecanico que es cuando se produce por mecanismos mecanicos externos como presiones[5]. 

La respiracion se define en dos ciclos diferentes, la inspiracion activa en la que el oxigeno entra en el cuerpo hacia los pulmones y una fase de espiracion pasiva que es en la que se exhala el anhidrido carbonico hacia el exterior [2]

La deformacion toracica que acompaña y media cada ciclo respiratorio es el producto mecanico dado que  las pleuras parietal y viseral estan en contacto, en la inspiracion el desplazamiento de la pared toracica arrastra consigo a los pulmones de modo que el cambio de volumenes que hay en la cavidad toracica induce un cambio equivalente en el volumen pulmonar [9], la expansion de la cavidad toracica disminuye la presion pleural haciendo que la presion alveolar caiga por debajo de la presion atmosferica siendo cerca de -6mmHg en relacion, por lo cual el aire entra hacia los alveolos[10] siguiendo el efecto boyle.

La espiracion es el efecto inverso y de forma pasiva, pues por la relajacion de los musculos el torax se achica y con el, el volumen de los pulmones tambien lo hace, por consiguiente la presion alveolar aumenta hasta  superar la presion atmosferica haciendo que este salga del cuerpo por la diferencia de presiones [10]

Durante el habla el patron difiere de los ciclos esperados al caracterizarlos en presion, la respiracion ya no esta governada por el control automatico del tronco encefalico unicamente, la corteza cerebral ejerce un control voluntario que se superpone a ese control y adapta el ritmo y las profundidades respiratorias para poder sincronizarlas con la fonacion, por lo tanto se producen espiraciones prolongadas y controladas voluntariamente dejando la pasividad de espiracion del tronco que se adaptan a cada oracion realizada, eso se puede traducir en un patron menos periodico y con una relacion de Rpm mas variable pero usualmente con menos cantidad de ciclos[9]



2. Seleccionar el sensor que considere más adecuado para medir la variable de
interés y, de esa forma, capturar las variaciones producidas por el proceso
respiratorio. Considere un voltaje de alimentación de +3.3 a +5 VDC, en el
caso de tratarse de un sensor pasivo. Medite sobre cómo adaptar el sensor al
cuerpo del sujeto de prueba para capturar la señal con un mínimo de
interferencia.

Para la detección de las variaciones mecánicas asociadas al ciclo ventilatorio, se ha seleccionado el sensor de fuerza por resistencia (FS4), específicamente el modelo FSR 402, este transductor se define como un dispositivo de película gruesa de polímero  que presenta una disminución en su resistencia eléctrica ante el incremento de la fuerza aplicada sobre su superficie activa.

La elección del FSR 402 responde a los requerimientos de sensibilidad y dimensiones necesarios para el monitoreo no invasivo. A demás el sensor posee una fuerza de actuación mínima de 0,1 N y un rango de sensibilidad que se extiende hasta los 10 N, lo cual es adecuado para captar la presión ejercida por la expansión de la caja torácica durante la inspiración. El FSR tiene un  perfil ultra delgado de 0,55 mm y su área activa de 12,7 mm de diámetro facilitan su integración entre el cuerpo y una banda de sujeción sin alterar el patrón fisiológico del sujeto. La alimentación del sensor se realizó mediante una configuración de divisor de voltaje, que permite convertir la variación de resistencia en una señal de voltaje analógica (V OUT) proporcional a la fuerza mecánica, lo cual facilitó su digitalización a través de una placa ESP32-S3-N16R8.

La adaptación del sensor se fundamenta en la mecánica respiratoria, donde la contracción del diafragma y de los músculos intercostales externos
 provoca un aumento del diámetro transversal y anteroposterior de la caja torácica. Este desplazamiento mecánico es el que se busca capturar para extraer el patrón respiratorio.

 Se anexa imagen del prototipo diseñado:



<img width="1600" height="1100" alt="dispisitivo" src="https://github.com/user-attachments/assets/782e1935-d55c-40d6-8108-171a00bbb9c8" />



El procedimiento de adaptación consiste en situar el área activa del sensor sobre la región torácica o abdominal del sujeto, el sensor se asegura mediante una banda elástica que mantenga una tensión base; de esta forma, cada fase inspiratoria generará un aumento de la fuerza sobre el sensor, disminuyendo su resistencia y produciendo un pico de voltaje en la señal adquirida. Esta configuración permite diferenciar claramente entre la inspiración activa y la espiración, cumpliendo con el objetivo de monitorear la frecuencia respiratoria  en tiempo real.

3. Diseñe y elabore un sistema que acondicione y digitalice la señal respiratoria
utilizando para ello el sensor previamente elegido. Puede utilizar el conversor
análogo-digital integrado en la placa Arduino.

Debido a que se escogió el sensor FSR 402, para acondicionar la señal se elaboró un divisor de voltaje, en el cual el sensor se conecta en serie con una resistencia de medición (RM) fija. La salida (VOUT) corresponde a la fracción de la tensión de alimentación (V+) determinada con la relación[6]:
                       RM/(RM+RFSR)                                  (1)

De tal modo que al disminuir la resistencia del FSR con el aumento de la fuerza aplicada, la salida se incrementa proporcionalmente [6]. Para el caso practico elaborado, se utilizó una resistencia de 10kΩ la cual hacía posible que la señal se mantuviera periódica y no se saturara.

Esta señal se digitalizó mediante el conversor análogo digital integrado en la ESP32-S3 N16R8, el rango de valores digitalizados corresponden a valores entre 0 y 4095, en donde para este cado este valor máximo representa 3.3 voltios. Para 

A continuación, se anexa la imagen que describe el divisor de voltaje anteriormente mencionado y las diferentes conexiones.



<img width="495" height="209" alt="image" src="https://github.com/user-attachments/assets/27829b2f-fec4-4fae-a534-1326808c03a1" />

Posteriormente para poder digitalizar el la señal, antes de poderla visualizar en MATLAB se realizó un código en ARduino IDE para configurar la placa y así poder realizar la respectiva configuración en MATLAB para enlazar la ESP32-S3N16R8 Y Capturar la señal.

A continuación se anexa el código que se utilizó en Arduino IDE para configurar la placa


```

const int FSR_PIN = 4;                         // GPIO4 -> ADC1_CH3
const int ADC_RESOLUTION_BITS = 12;             // 0 a 4095
const unsigned long SAMPLE_INTERVAL_US = 10000; // 10 ms -> Fs = 100 Hz

unsigned long lastSampleTime = 0;

void setup() {
  Serial.begin(115200);
  while (!Serial) { ; }

  analogReadResolution(ADC_RESOLUTION_BITS);
  analogSetPinAttenuation(FSR_PIN, ADC_11db);   // permite medir hasta ~3.3V

  delay(1000); // tiempo para estabilizar antes de iniciar el envío
}

void loop() {
  unsigned long now = micros();

  if (now - lastSampleTime >= SAMPLE_INTERVAL_US) {
    lastSampleTime = now;
    int raw = analogRead(FSR_PIN);
    Serial.println(raw);   // una muestra por línea -> Serial Plotter y MATLAB
  }
}

```
4. Coloque el sensor sobre alguno de los miembros del equipo para verificar la
operatividad del sistema.

Para esta sección, después de terminar el ensamble del sistema creado, se colocó en uno de los miembros del grupo de laboratorio. Posteriormente se elaboró un código de captura de tiempo real en MATLAB con el cual el objetivo era confirmar que el sistema entregaba una señal periódica y sincronizada con los ciclos de inspiración y espiración del sujeto de prueba antes de proceder a las capturas de 30 segundos en condiciones de reposo y habla.
A continuación se anexa la imagen de la captura en tiempo real de la señal respiratoria de verificación de operatividad en donde se experimento realizando ciclos normales de inspiración y expiración y otros en los que se mantenían estos ciclos con el fin de evidenciar el funcionamiento correcto y la entrega de la señal del sistema creado.



<img width="1619" height="748" alt="image" src="https://github.com/user-attachments/assets/d2354bd4-51ec-414d-bc06-38371abcf45b" />

De igual forma se anexa el código en MATLAB con el cual se evidenció la operatividad del sistema por medio de la captura de la señal respiratoria en tiempo real.

```
clear; close all; clc;

disp('Puertos disponibles:');
disp(serialportlist("available"));

COM = "COM3";          
baudRate = 115200;      

s = serialport(COM, baudRate);
configureTerminator(s, "LF");
flush(s);


Fs = 100;               
ventana_s = 60;         
Nmuestras = Fs * ventana_s;

t = (0:Nmuestras-1) / Fs;
buffer = nan(1, Nmuestras);

figure('Name', 'Señal respiratoria en tiempo real');
h = plot(t, buffer);
xlabel('Tiempo (s)');
ylabel('Valor ADC (0-4095)');
title('Señal respiratoria en tiempo real ');
ylim([0 4095]);
grid on;

disp('Adquisición en tiempo real.');

while ishandle(h)
    if s.NumBytesAvailable > 0
        linea = readline(s);
        valor = str2double(linea);
        if ~isnan(valor)
            buffer = [buffer(2:end), valor];  
            set(h, 'YData', buffer);
            drawnow limitrate;
        end
    end
end

clear s;
disp('Adquisición finalizada.');

```


5. Empleando la función “Serial Plotter” del menú “Herramientas” del entorno de
programación, tome capturas de pantalla que muestren la señal:

a. En reposo (cuente manualmente el número de veces que el sujeto inhala o
exhala).



b. Mientras el sujeto de prueba habla o lee.

PARTE B

1. Diseñe y elabore un breve código en MATLAB que permita la captura
temporizada de la señal respiratoria adquirida por el sistema que Ud. ha
construido y probado.


```
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
```


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

Diferentes en ambos aspectos, los patrones respiratorios en reposo se comportan como oscilaciones de forma similar a una señal senosoidal, pues comparte caracteristicas tipicas como un ritmo, frecuencia y amplitud constante ademas que una similitud entre sus ondas resultantes, esto se causa a un proceso mecanico repetitivo y sin interferencia, los musculos encargados de la respiracion aumentan el volumen del pulmon reduciendo su presion de forma natural y su relajacion reduce el volumen por lo cual la presion aumenta y el aire sale al ambiente por efecto boyle, mientras que en el habla para poder efectuar la fonacion, se realizan respiraciones mas abruptas y salidas de aire controladas dando un efecto impulso en la inspiracion y luego una señal descendiente, prolongada y controlada por la naturaleza de la frase,palabra u oracion efectuada.

• Pregunta 2: ¿Cuáles serían las ventajas y desventajas de emplear múltiples
sensores para el monitoreo del proceso respiratorio? ¿Cuáles podrían ser
las razones?

Primero es necesario diferenciar si los sensores son del mismo tipo con proposito de medir la misma variable fisiologica o diferentes, en caso de ser la misma (en este caso otro sensor de deformacion/presion), entre las ventajas tenemos la posibilidad de que se coloquen en los 2 pulmonnes y de esa manera comprobar la capacidad de almacenamiento de volumen entre los pulmones y un ponderado de ambos, esto permite medir la funcion pulmonar individual ademas de la coordinacion de la elevacion, una diferencia fuera de parametros podria significar malformacioens anatomicas o patologias fisiologicas de los musculos respiratorios, sin embargo requiere estudios para saber cuales son los parametros de diferencia entre ambos teniendo en cuenta que no son simetricamente perfecto por el volumen ocupado del lado que contiene al organo cardiaco sin contar el aumento en los equipos necesarios tanto profesional como tecnico.
Por otro lado si son diferentes tipos, tambien tiene ventajas como la combinacion del sensor de deformacion toracica con otro sensor de CO2, para poder medir el proceso respiratorio tanto por medio de una medicion de diferencia anatomica entre las fases, como el intercambio de gases en su simultaneo y poder medir la concordancia, este puede ser utilizado especialmente en pacientes internados para comprobar el correcto flujo de oxigeno y evitar posibles hipercapnias e hipocapnias[10], pero se requiere tambien de mayor profundizacion tecnica y de que solo serviria como un remplazo temporal a la saturacion de oxigeno en sangre del pulsioximetro ya muy eficaz


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

