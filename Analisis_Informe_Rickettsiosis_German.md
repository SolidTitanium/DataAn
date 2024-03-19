# Análisis del Informe Epidemiológico Semanal de Rickettsiosis, Sonora 2024

## Ideas Generales

- Un agrupamiento interesante para ver es identificar, casos y defunciones por indice de marginalización municipal (IMM).

- Me parece relevante estudiar los casos de FMRR por periodos climatológicos, en particular, las garrapatas suelen preferir un ambiente húmedo, agrupar por municipio o región climatológica y correlacionar con precipitación y nivel de humedad en el ambiente podria arrojar algo interesante, también creo que se podria encontrar alguna periodicidad que podria evidenciar estacionalización en los casos (o incluso las defunciones).

- Otro indicador interesante podria ser buscar una correlación entre la densidad poblacional y los casos de FMRR, en este caso es importante normalizar los datos ya que es esperable una mayor cantidad de casos en una pobalción mayor.

## Casos por Entidad Federativa (2da Página del Reporte)

- Veo beneficioso mostrar casos en semanas anteriores y mostrar los casos en esta semana de años anteriores.

- Podria mostrarse la diferencia entre la incidencia en esta semana en este año y años anteriores para identificar incrementos o decrementos imprevistos.

## Defunciones (3ra Página)

- Esta página da un promedio de edad para casos con defunción, agregar más estadísticos me parece importante, al menos su desviación estándar.

## Datos por Derechohabiencia (4ta Página)

- La distribución de casos por distritos de salud y derechohabiencia me parece muy relevante y útil.

- Se pueden formar indicadores a partir de síntomas previstos, esto se puede hacer directamente correlacionando datos pero me parece que sería mejor consultar un profesional de la salud.

## Datos por Municipio (5ta Página)

- Una vez más creo que comparar la incidencia y letalidad con años anteriores con respecto a cada municipio podria ser muy útil.

- Incluso se podria ofrecer proyecciones básicas para cada municipio.

- También veo importante hacer seguimiento a campañas de salud en cada municipio para determinar su impacto.

## Canal Endémico (6ta Página)

No encontre demasiada información acerca de la herramienta de "Canal Endémico", sin embargo, encontre unos cuantos estudios que la utilizan, y un par que ahondan un poco más en ella, en particular parece que solo ciertos paises usan esta herramienta como método de monitoreo para enfermedades endémicas y poco a poco se ha ido popularizando.

---

En el estudio por [Hernández, et al. (2016)](https://revistabiomedica.org/index.php/biomedica/article/view/2934) se analiza la tendencia del dengue en el departamento de Valle de Cauca, Colombia y se habla un poco acerca de la metodología para realizar canales endémicos.

> El  canal  endémico  es  la  representación  gráfica del  número  de  casos  que  se  presentan  en  un área  en  períodos  definidos  (semana  o  periodo epidemiológico), comparado con los datos de años anteriores (usualmente, de cinco años).</br></br>Existen   diferentes   métodos   para   suavizar   la tendencia   observada   y   establecer   límites   de control:   el   método   de   promedios   móviles,   el de   suavización   exponencial,   y   métodos   más sofisticados  como  los  modelos  autorregresivos  y la metodología de Box-Jenkins.

Desconozco el método que se utilizó para elaborar el canal endémico que aparece en el reporte pero considero relevante mencionar que los métodos de suavización utilizados afectan a los límites de control resultantes, en particular el estudio sugiere lo siguiente.

>Mientras  que  el  método  de  promedios  móviles se  ve  afectado  por  datos  extremos,  el  método de   suavización   exponencial   es   adecuado   en aquellos  casos  en  los  que  el  comportamiento  de los datos no tiene una tendencia ascendente o descendente.

Considerando esto creo que se deben realizar pruebas para determinar que metodología utilizar para realizar un canal endémico en el caso de la FMRR, más aún, el estudio no utiliza los métodos que denomino "más sofisticados", creo que seria importante caundo menos probar algún método de regresión y comparar sus resultados a los de los métodos tradicionales.

---

Todo lo anterior es para el tema del suavizamiento de la tendencia observada y elaboración de límites de control, falta abordar el tema de que periodo histórico utilizar para calibrar la herramienta. Buscando más información al respecto, no encontre mucho acerca de la metodología para la elección del periodo, no obstante en el estudio por [Norzaher Ismail, et al. (2020)](https://spaj.ukm.my/ijphr/index.php/ijphr/article/view/266) se construye un canal endémico para (una vez más) identificar el comienzo de una posible epidemia de Dengue en este caso en Negeri Sembilan, Malaisya.

En este estudio se utilizó el método de promedios móviles para elaborar el canal endémico, lo que me parecio interesante es que utilizaron tres periodos historicos diferentes, uno de 5 años (como se indica en el estudio anterior), uno de tres años y uno de dos. El estudio menciona que esto es debido a que en los años recientes ha habido fuertes epidemias pero tambien esfuerzos por combatir la enfermedad, esto hace que los tres diagramas sean muy diferentes entre sí (se pueden observar en las páginas 1234 y 1235) los primeros dos resultaron ser muy poco confiables como indicadores de un posible resurgimiento ya que hubo epidemias y cambios en los criterios de diagnóstico durante esos años, el estudio continua utilizando el 3er canal endémico con un periodo histórico de 2 años.

Si bien esto no arroja mucha luz en como se debe elegir este periodo, si evidencia que la elección del mismo es crucial para un funcionamiento fiable de la herramienta, considero importante probar diferentes periodos de historicidad y corroborar si no existieron brotes epidemicos fuertes, cambios en los criterios de diagnostico, casos faltantes en masa en los datos o cualquier otro problema que pueda causar que un periodo histórico se vuelva inválido.

## Medidas Preventivas (Última página del reporte)

Si bien no veo de más recordar a cualquier persona que lea el reporte las medidas de prevención básicas contra la rickettsia, al mismo tiempo no lo veo muy relevante, creo que seria apropiado tal vez hacer un documento diferente donde se vean más a fondo estos métodos preventivos. Normalmente la persona que debe de conocer con claridad los métodos preventivos no es la misma que aquella que necesita el reporte.