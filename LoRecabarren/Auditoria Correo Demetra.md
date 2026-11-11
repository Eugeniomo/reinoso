# Auditoría del correo de consultas a Demetra (AUD-2026-11-11)

Fecha: 11-11-2026. Objeto: borrador del correo con 31 consultas (scratchpad, `correo_demetra.txt`). No se modificaron ni el correo ni el xlsx.

Fuentes contrastadas: itemizado original `~/Downloads/13.08.26 - Presupuesto Lo Recabarren.xlsx`, `Cubicacion LoRecabarren.xlsx` (columnas Observación y hoja 'Consultas Demetra'), `Auditoria Cubicacion.md`, memoria Rev 1, las 15 láminas en PDF (renderizadas y revisadas a la vista: pav 1, 8, 9 y 10; AALL 2, 4 y 5) y los DXF. Extracción propia de todos los textos de `pav.dxf` y `all.dxf` (modelo y espacio papel, 29.576 textos) y conteo propio de bloques y largos con ezdxf en el venv existente. Lo que solo viene de las auditorías anteriores y no remedí se marca como tal.

## Veredicto

El correo cubre todos los ítems 'A VERIFICAR' del xlsx, pero no deja resuelta la oferta: faltan 3 ítems estimados sin consulta, 25 dudas con costo que nadie anotó (entre ellas, que el proyecto no está aprobado por SERVIU) y 6 condiciones comerciales que la solicitud de Demetra exige. Tiene 4 cifras o afirmaciones erradas o no sostenibles (consultas 3, 5/22, 8 y 12) y 7 consultas que se pueden contestar con un 'sí' o que no preguntan nada.

Se proponen 25 consultas nuevas (32 a 56) y 26 correcciones (24 consultas, el saludo y el cierre del correo).

## 1. Cobertura

Los 29 ítems 'A VERIFICAR' del xlsx tienen consulta (2.1.6-2.1.13 y 2.1.31 en la 3; 2.2.1 en la 2; 2.3.4, 2.3.18 y 2.3.19 en la 9; 2.3.8 en la 7; 2.3.11-2.3.14 en la 10; 2.3.22 en la 11; 2.4.4 en la 20; 2.4.20, 2.4.33 y 2.5.2 en la 24; 2.4.21, 2.4.22 y 2.4.24 en la 16; 2.4.30 y 2.4.31 en la 18; 2.5.1 en la 21; 2.5.3 en la 17).

Faltan:

| Ítem o riesgo | Cifra en el xlsx | Problema | Destino |
|---|---|---|---|
| 2.1.27 Separador de carril a retirar | 30 un. (estimado) | Un solo rótulo y 30 bloques dibujados (12 SEPA + 18 SEPA2, verificado) | Consulta 43 |
| Fila 30 sin código, Acceso a trasladar | 2 un. (estimado) | Nadie define qué se traslada | Consulta 43 |
| Fila 29 sin código, Sumidero a trasladar | 1 un. (estimado) | all.dxf lo rotula 'sumidero trasladado que se conecta a red existente'; no se relaciona con la C.I. existente del sumidero 2 | Corrección 19 |
| 2.3.3 Soleras (clasificación de las segmentadas) | 4.305,6 ml, de ellos 375,3 ml segmentados tomados como rebajadas | La simbología de la lámina 1/10 usa línea segmentada para tipo A plinto 0,00 y para tipo C; la tipo C va 'incluida en rodados' según Demetra | Consulta 37 |
| 2.3.17 Cama de soleras | 219,6 m3 (146,4 m3 con 0,10 m) | La consulta 9 cita la cama de 0,15 m pero no pregunta cuál rige | Corrección 9 |
| 2.1.23 Mora | 1 un. (estimado) | Es una zona, no una unidad; la consulta 25 solo pregunta si se cotiza | Corrección 25 |
| AUD-9 Proyecto 63023 | HCV ~194 m2, vereda 38-40 m2, baldosa 8,3 m2, solera 63,8 + 10,6 ml, demolición 24,1 m2 | La consulta 22 solo da la ciclovía; sin las cifras Demetra puede responder 'incluido' sin medir la exposición | Corrección 22 |
| AUD-13 Subrasante bajo soleras | 650 a 1.290 m2 | La consulta 2 lo pregunta sin cifra | Corrección 2 |
| AUD-18 Demolición fuera de la huella | 644,6 m2 | La consulta 8 pregunta quién rellena, sin la cifra | Corrección 8 |
| R8 Dos versiones de DWG | HCV difiere 20,6 m2; rebajes 31 contra 32 (cifras de R8, no remedidas) | Sin consulta; además pav.dxf conserva la descarga antigua del colector 15 a colector existente D=500 mm (verificado) | Consulta 33 |

## 2. Dudas con costo que nadie anotó

Evidencia propia, por orden de costo probable. Los montos son órdenes de magnitud con precios supuestos y se deben validar con costos de Reinoso.

1. Proyecto sin aprobar. Las 15 láminas dicen 'PARA APROBACION SERVIU' (Rev 0 del 12-11-2024 y Rev 1 de septiembre de 2025) y el recuadro 'aprobado por oficio SERVIU N° ... de fecha ...' está vacío. Con precio cerrado, cualquier observación de SERVIU que cambie cantidades la paga Reinoso. Riesgo no acotado. Consulta 32.
2. Corte y sello de juntas sin ítem. La lámina 10/10 detalla junta transversal de contracción, transversal de construcción y longitudinal de construcción, con barras de traspaso, cordón, imprimación CSS-1 y sellante elastomérico JAC-3405. Estimación propia: 16.193 m2 de calzada / 4 m de espaciamiento = unos 4.000 ml transversales + unos 2.200 ml longitudinales, del orden de 6.000 ml. Con 2.500 a 5.000 CLP/ml, CLP 15 a 30 millones. Consulta 35.
3. Relleno estructurante de colectores. La sección típica HDPE de la lámina 5/5 exige relleno estructurante clase II o III (grava y arena, máximo 1½") hasta 20 cm sobre la clave, y solo admite material de excavación en el relleno final. Demetra anotó que 2.4.5 (relleno estructural) va 'incluido en 2.4.22' (relleno con material de excavación). Estimación propia con ancho mínimo 1,25 De + 0,30 m: unos 370 m3 en DN375 y 125 m3 en DN300, unos 490 m3 de empréstito; CLP 10 a 15 millones. Consulta 38.
4. Contenido de las zanjas de infiltración. Lámina 4/5: excavación de 4,30 m (4,75 m en la N°1), 0,50 m de recubrimiento, cama de gravilla de 0,20 m, geotextil no tejido de 200 g/m2 y relleno lateral y superior de arena gruesa y limpia. Estimación propia de arena, con taludes supuestos de 0,40 m por lado: 550 a 650 m3 en los 130,2 m de zanjas. El ítem es global (gl) y nadie confirmó qué incluye. Consulta 39.
5. Dos sistemas de infiltración distintos. La lámina 4/5 dice 'estanque de drenaje Atlantis' (26 t/m2) en los cortes y 'sistema de drenaje Hidrocelda' en la planta, y advierte que las dimensiones de los módulos varían según el fabricante. Consulta 40.
6. Cálculo estructural de cámaras. Nota de la lámina 5/5: 'el presente plano considera solo formas y dimensiones útiles... debiendo complementarse con los cálculos estructurales correspondientes'. Nadie lo entrega; afecta decantadoras de hasta 3,48 m. Consulta 41.
7. Napa e infiltración. Las bases de cálculo de la tubería suponen 'sin presencia de napa freática' y el sistema depende de que el suelo infiltre. No hay ensayo de infiltración ni napa informada. Consulta 42 y corrección 29.
8. Interferencias con servicios existentes. En la topografía, a menos de 50 m de la red proyectada: 'colector ALL existente D=500 mm' (35 m), 'tubería D. 300 mm' (44 m), 'tubo' y 'pozo 3b' (19 m), y cámaras de alcantarillado, agua potable, electricidad y teléfonos (capa Lot_EXISTENTE). No hay catastro. Consulta 34.
9. Demolición de dos casas: permiso municipal, corte de empalmes, ocupación y posible asbesto. Consulta 47.
10. Traslado de 7 luminarias y 2 postes sin proyecto eléctrico ni tramitación definida. Consulta 46.
11. Canal proyectado: la memoria dice que se reemplazó la descarga al canal y que este 'se encuentra en tramitación aparte'. Conviene dejarlo excluido por escrito. Consulta 45.
12. Empalmes con Santa María y Agua del Palo y reposición de pavimento existente dañado. Consulta 36.
13. Itemizado incompleto: la fila 2.3.9 no tiene descripción, el código 2.4.23 no existe y las filas 28, 29, 30 y 41 no tienen código. Consulta 44.
14. Accesos al Club de Polo y al club de golf ('ACCESO CLUB DE POLO', 'ACCESO A CLUB DE GOLF' en planta) y horario de Vitacura. Consulta 56.
15. Materiales que pudiera suministrar Demetra (la solicitud pide declarar materiales propios o de terceros). Consulta 48.

## 3. Lo que la oferta exige y el correo no pregunta

La solicitud pide APU por ítem, IVA, forma de pago, vigencia y anticipo. El correo pregunta forma de pago, retenciones, garantías, seguros y multas (28), pero no:

- si el contrato es a suma alzada o a precios unitarios con pago de lo ejecutado, ni cómo se pagan las obras extraordinarias (consulta 49). Es la pregunta que define cuánto pesa cada error de cubicación;
- moneda, reajustabilidad e IVA (consulta 50);
- formato del APU, leyes sociales, gastos generales y utilidad (consulta 51);
- si hay anticipo, con qué porcentaje y devolución, y la vigencia de la oferta (consulta 52);
- si los supuestos y exclusiones de la oferta forman parte del contrato (consulta 53 y corrección del cierre);
- visita a terreno y entrega de la faja (consulta 54);
- quién es el contratista ante SERVIU, quién paga los derechos de inspección y las garantías SERVIU (consulta 55).

## 4. Exactitud

| N° | Afirmación del correo | Fuente | Resultado |
|---|---|---|---|
| 1 | La memoria remite a las EETT SERVIU RM | Memoria, cap. 6 | Correcto |
| 2 | -1,31 m en Km 0+600 y +0,41 m en Km 0+400; terreno cada 100 m; sin perfiles transversales | pav.dxf, filas 'ELEVACION RASANTE/TERRENO': 681,18 - 682,49 y 677,05 - 676,64 | Correcto. El signo no está definido en el texto: corregir a 'bajo/sobre el terreno' |
| 3 | 2 recintos, 1 portón, 2 pilares, 2 señales, 2 resaltos (3 en la capa) | Rótulos de 01_Dem Ext_Txt; bloques PILAR; hatch 1-RESALTO | Pilares: hay 1 rótulo 'pilar a retirar' y 2 bloques, no '2 rótulos'. Lo demás correcto |
| 4 | 1.017 m; 405,8 + 28,4 + 5,2 + 577,6 | Capa 01_Dem Ext_Solera tipo A: 52 polilíneas, 1.017,0 m (medido) | Total correcto; el reparto por rótulo viene de la cubicación y no lo rehíce. Omite los ~17 m dibujados dos veces |
| 5 | Lámina 1/10 hormigón y 2/10 asfáltica 'para la misma superficie' | Simbologías: 'CALZADA DE HORMIGON A DEMOLER' (lám. 1), 'CALZADA ASFALTICA A DEMOLER' (lám. 2); 5 rótulos en planta 'CALZADA HCV A DEMOLER' | 'Para la misma superficie' no se puede sostener: son simbologías de láminas distintas. Además contradice la 22, que lee la misma simbología de la lámina 2/10 como la intersección 63023 |
| 6 | Memoria base 15 cm en accesos; lámina 8/10 acceso 0,30 m; corte 1-1 con 0,30 m bajo la calzada de 6,50 m; tramo ~155 m | Memoria cap. 4; lámina 8/10 vista | Correcto (el tramo de 155 m es de la re-auditoría R2, no remedido) |
| 7 | Corte 6-6, banda de 3,00 m, G35 e=0,17; itemizado G30 e=0,17 | Lámina 8/10; ítem 2.3.8 | Correcto. Omite que la lámina 10/10 trae el detalle tipo de la banda |
| 8 | Bandejón de 3,00 a 3,50 m; franjas de 1,00 a 1,30 m; anchos totales de 23,00 a 25,00 m | Cortes 1-1 a 5-5, lámina 8/10 | Errado en parte: bandejón de 3,00 a 4,00 m (2-2: 3,00 + 1,00); franjas de hasta 3,00 m (5-5) y 5,70 m (4-4); los cortes 3-3 (9,50 + 9,50) y 4-4 (9,20 + 4,80) no tienen bandejón y muestran calzadas que la memoria no menciona. Total 23,00-25,00 correcto |
| 9 | Cama de 0,15 m y respaldo H-10 | Lámina 9/10 | Correcto; la cama dibujada mide ~0,10 m (R3) y el correo no lo dice |
| 10 | 29 accesos y 31 rebajes | Auditorías previas (pav.dxf) | Se acepta; all.dxf tiene 32 rebajes (R8) |
| 11 | Detalle de resalto en la lámina 10/10, sin cantidad | Lámina 10/10 | Correcto. El detalle incluye rejilla prefabricada a ambos lados (2.3.22) y demarcación de paso de cebra |
| 12 | 'Reemplazo de suelo si el CBR es menor a 12 %' | Nota de la lámina 9/10 (texto completo extraído) | Errado: un CBR distinto de 12 % obliga a rediseñar; el reemplazo por subbase corresponde si la subrasante es orgánica o expansiva, si no llega a 95 % del Proctor modificado o si la base no llega a CBR 60 %, con espesor 'indicado en las EETT del proyecto', que no existen. Las otras notas están bien |
| 13 | 899 m cuadro; 863,2 m perfiles; colector 15: 8,0 m y acumulado de 21,3 a 31,3 | all.dxf, perfil colector 15: parciales 21,3 y 8,0; acumuladas 0,0, 21,3, 31,3 | Correcto (863,2 de la re-auditoría) |
| 14 | 8 decantadoras; 'decantadoras dobles = 0' | 8 rótulos 'CAMARA DECANTADORA N°1..8' en all.dxf; resumen de la lámina 2/5 | Correcto. Omite que los sumideros S-2, S-3 y las baterías también son 'con cámara decantadora' (lámina 5/5) |
| 15 | Zanja 8 rotulada en 2/5; memoria verifica 1 a 7; sin detalle propio; 1,64 contra 2,05 m | Memoria; lámina 4/5 (detalles N°1, N°2-N°7, N°3, N°4, N°5-N°6) | Correcto |
| 16 | Colector 14 con 2,4 m3 de 2 a 4 m; descargas DN300 385 m | Cuadro de cañerías; perfiles | Correcto |
| 17 | Módulos de 3,60 a 4,05 m; decantadoras hasta 3,48 m | Rótulos de zanjas; decantadora N°7 H total 3,48 | Correcto, pero la excavación real es 4,30 a 4,75 m (lámina 4/5) y esa es la cifra que justifica la entibación |
| 19 | 38 S-2, 4 S-3, 8 baterías; DWG 46 S-2, 8 S-3, 4 de otro tipo | Cuadro; bloques en 00_S2_All ext_Sumidero (46 + 8 + 4, verificado) | Cifras correctas, pero ambos suman 58: la diferencia es de tipo, no de cantidad. '¿Qué cantidad rige?' induce a error |
| 20 | Cámara repartidora en la lámina 5/5 | Texto 'CAMARA REPARTIDORA' en la lámina 5/5 y 'cámara repartidora según detalle' en la 4/5 | Correcto |
| 21 | Al menos 10 rótulos de cámara a nivelar, uno en plural | 7 + 1 + 1 + 1 rótulos en 01_Dem Ext_Txt | Correcto: son exactamente 10 |
| 22 | Ciclovía de unos 376 m2 | 375,9 m2 (cubicación), 375,8 m2 (re-auditoría) | Correcto. Ver contradicción con la 5 |
| 23 | 33 señales proyectadas, 6 bolardos | 6 bloques J-BOLARDO-CICLOVIA (verificado); la capa '00_Señal proy 01' incluye bloques rotulados 'EXISTENTE' (RPI-2) | Bolardos correctos. Las 33 señales vienen de la auditoría previa; no todas son proyectadas |
| 24 | Pares repetidos; 2.4.33 sin unidad; E50 suma m3 con m2 | Itemizado original | Correcto. 2.5.2 tampoco tiene unidad. E50 es un error de planilla de Demetra que no cambia nada: sobra |
| 25 | Mora sin nota | Itemizado F38 vacío | Correcto |

## 5. Redacción

- Sin pregunta: la 20 (junturas) y la 24 ('solicitamos aclarar' no dice qué debe contestar Demetra).
- Se resuelven con un 'sí' sin cerrar nada: la 14, la 17 (primera mitad), la 22, la 23 y la 25. La 12 ofrece dos opciones sin pedir unidad de precio.
- Doble lectura: la 2 (signo de -1,31 y +0,41) y la 19 ('qué cantidad rige', cuando la cantidad total coincide).
- La 1 mezcla cinco obligaciones distintas en una frase y pide 'los ensayos que se exigirán', no quién los paga ni en qué ítem.
- La 24 menciona E50, que no aporta y le resta seriedad.
- Abreviatura 'All' en el saludo: escribir 'Aguas Lluvias'.
- El trato de usted y el tono son correctos en todo el correo; no hay voseo.
- Con 56 consultas, conviene enviarlas además como tabla adjunta (N°, sección, consulta, respuesta) para que Demetra responda una por una.

## 6. Consultas nuevas listas para pegar

Antecedentes

32. Aprobación del proyecto. Las 15 láminas están emitidas 'para aprobación SERVIU' (revisión 1, septiembre de 2025) y el recuadro del oficio de aprobación está en blanco. Solicitamos indicar si el proyecto ya cuenta con aprobación SERVIU y, si no la tiene, cómo se pagarán las obras que aumenten o cambien si SERVIU lo aprueba con observaciones, dado que la solicitud de cotización no admite cambios de precio.

33. Versión vigente de los archivos. El DWG de pavimentación conserva una versión anterior de aguas lluvias: en él, el colector 15 descarga a una C.I. existente y a un colector existente D=500 mm, mientras el DWG de aguas lluvias lo descarga a la zanja de infiltración N°8. Además, la calzada HCV difiere en unos 20 m2 y los rebajes de vereda son 31 en un archivo y 32 en el otro. Solicitamos confirmar que para pavimentos rige el DWG de pavimentación y para aguas lluvias el DWG de aguas lluvias, o enviar una versión única vigente.

34. Servicios existentes. Las láminas muestran instalaciones existentes cercanas a las obras (colector de aguas lluvias D=500 mm, tuberías de 300 y 500 mm, un pozo y cámaras de alcantarillado, agua potable, electricidad y teléfonos), sin catastro ni cotas. Solicitamos el catastro de servicios con que cuente el mandante e indicar quién gestiona ante cada compañía, y quién paga, los cruces, protecciones, traslados y nivelaciones de esas instalaciones, incluidas las calicatas de reconocimiento previas.

Pavimentación

35. Juntas del pavimento. La lámina 10/10 detalla la junta transversal de contracción, la junta transversal de construcción y la junta longitudinal de construcción, con barras de traspaso, cordón de respaldo, imprimación CSS-1 y sellante asfáltico elastomérico JAC-3405 o similar. El itemizado no tiene ítem para el corte y sello de juntas, que estimamos del orden de 6.000 ml en la calzada. Solicitamos indicar en qué ítem se paga, el espaciamiento de las juntas transversales que rige y si las juntas de vereda llevan sello.

36. Empalmes con pavimentos existentes. Solicitamos indicar hasta dónde llega el pavimento de esta partida en las intersecciones con Av. Santa María y Av. Agua del Palo, cómo se ejecuta el empalme con el pavimento existente (corte con sierra, barras de traspaso) y en qué ítem se paga la reposición de losas, soleras o veredas existentes que resulten dañadas.

37. Soleras en línea segmentada. La simbología de la lámina 1/10 usa línea segmentada tanto para la solera tipo A plinto 0,00 m como para la solera tipo C, y en planta hay unos 375 m de solera en línea segmentada. Solicitamos indicar qué largo corresponde a solera tipo A rebajada (ítem 2.3.3) y cuál a solera tipo C, que según el itemizado va incluida en los dispositivos de rodado (2.3.21).

Aguas lluvias

38. Relleno de zanjas de colectores. La sección típica de tubería HDPE de la lámina 5/5 exige relleno estructurante de suelo clase II o III (grava y arena, tamaño máximo 1½") hasta 20 cm sobre la clave, compactado a 90 % o 95 % de la D.M.C.S., y admite material de excavación solo en el relleno final. El itemizado indica que el relleno estructural (2.4.5) va incluido en el relleno con material de excavación (2.4.22). Para 899 m de DN375 y 385 m de DN300 estimamos unos 490 m3 de relleno estructurante. Solicitamos indicar en qué ítem y con qué unidad se paga ese material de empréstito, o si Demetra acepta usar el material de excavación como relleno estructurante.

39. Contenido del precio de cada zanja de infiltración. El detalle de la lámina 4/5 indica para cada zanja una excavación de 4,30 m (4,75 m en la N°1), cama de gravilla bajo 1½" de 0,20 m, módulos envueltos en geotextil no tejido de 200 g/m2 y relleno lateral y superior de arena gruesa y limpia, que estimamos entre 550 y 650 m3 en las 8 zanjas. Solicitamos confirmar qué incluye el precio global de cada zanja (2.4.10 a 2.4.16 y 2.4.25): excavación, entibación o taludes, agotamiento, gravilla, geotextil, módulos, arena, tubería interior, cámara repartidora, relleno, retiro de excedentes y reposición del área verde sobre la zanja.

40. Sistema de infiltración especificado. La lámina 4/5 nombra dos sistemas: 'estanque de drenaje Atlantis', con resistencia mínima de 26 t/m2, en los cortes de las zanjas, y 'sistema de drenaje Hidrocelda' en la planta, y advierte que las dimensiones de los módulos pueden variar según el fabricante. Solicitamos indicar qué sistema rige, si se aceptan equivalentes y, en ese caso, si se debe cumplir el número de cajas de cada zanja (9.745 en total) o su volumen útil.

41. Cálculo estructural de cámaras. La nota de la lámina 5/5 indica que el plano considera solo formas y dimensiones útiles y que debe complementarse con los cálculos estructurales correspondientes. Solicitamos indicar si el mandante entregará ese cálculo (armaduras de cámaras, de decantadoras de hasta 3,48 m de altura y de la cámara repartidora) o si el oferente debe incluir su desarrollo y la aprobación respectiva.

42. Capacidad de infiltración. El diseño supone que no hay napa freática y su funcionamiento depende de la capacidad de infiltración del suelo, que no se informa en los antecedentes. Solicitamos indicar si se exigirá un ensayo de infiltración en terreno antes de construir las zanjas, de cargo de quién, y cómo se pagarán las obras adicionales si el resultado obliga a ampliar o modificar el sistema.

Alcance e itemizado

43. Retiros sin definición. Solicitamos indicar: a) si el separador de carril a retirar (2.1.27) son 30 unidades, ya que hay un solo rótulo y 30 elementos dibujados; b) qué se traslada en el ítem 'acceso a trasladar' (sin código, 2 rótulos); y c) si el talud del rótulo 'pirca y talud a retirar' se paga como movimiento de tierra (2.2.3) o dentro del retiro de pirca (2.1.8).

44. Filas incompletas del itemizado. La fila 2.3.9 no tiene descripción, el código 2.4.23 no existe y las filas 'poste de madera con luminaria a retirar', 'sumidero a trasladar', 'acceso a trasladar' y 'pimientos que se retiran' no tienen código. Solicitamos indicar si falta algún ítem y con qué código deben presentarse esas filas en la oferta.

45. Canal proyectado. La memoria indica que la descarga a un canal proyectado se reemplazó por infiltración y que el canal está en tramitación aparte. Solicitamos confirmar que el canal y sus obras asociadas no forman parte de esta partida.

46. Luminarias y postes. El itemizado pide trasladar 7 luminarias (2.1.29) y 1 poste de fierro, y retirar 1 poste de madera con luminaria, sin proyecto de alumbrado. Solicitamos indicar si el traslado incluye fundación, canalización, cableado y reconexión, y quién tramita y paga ante la distribuidora eléctrica y la Municipalidad de Vitacura.

47. Demolición de casas. Los ítems 2.1.7 y 2.1.31 piden retirar la casa principal y la casa secundaria. Solicitamos indicar quién obtiene el permiso municipal de demolición, quién corta y retira los empalmes de agua, electricidad y gas, si las casas estarán desocupadas al inicio de la obra y si existen materiales con asbesto que requieran retiro especial.

48. Materiales suministrados por el mandante. Solicitamos indicar qué materiales suministrará Demetra, si alguno (por ejemplo hormigón, soleras, tuberías, módulos de infiltración o rejillas), para excluirlos de los precios unitarios.

Oferta y condiciones de ejecución

49. Modalidad del contrato. Solicitamos indicar si el contrato será a suma alzada sobre las cantidades de la oferta o a precios unitarios con pago de las cantidades realmente ejecutadas, y cómo se valorizarán los aumentos, disminuciones y obras extraordinarias que ordene Demetra o que resulten de las respuestas a estas consultas.

50. Moneda, reajuste e IVA. Solicitamos indicar si los precios deben ofertarse en pesos o en UF, netos y con el IVA en línea aparte, y si se aplicará algún reajuste (por ejemplo, IPC o índice de la Cámara Chilena de la Construcción) si el inicio se posterga o si la obra supera un plazo determinado.

51. Formato del análisis de precios. Solicitamos indicar si Demetra tiene un formato propio de análisis de precios unitarios, si los gastos generales y la utilidad deben incluirse en cada precio unitario o presentarse como ítems separados, y qué porcentaje de leyes sociales debe usarse.

52. Anticipo y vigencia. Solicitamos indicar si Demetra otorgará anticipo, con qué porcentaje, garantía y forma de devolución, y qué vigencia mínima debe tener la oferta.

53. Supuestos y exclusiones. Solicitamos indicar si la lista de supuestos y exclusiones que acompañará la oferta, junto con las respuestas a estas consultas, formará parte del contrato y, si no, de qué forma se incorporarán.

54. Visita y entrega del terreno. Solicitamos coordinar una visita a terreno antes del cierre de la oferta e indicar si la faja de la obra se entregará completa al inicio, con los predios desocupados y las cesiones resueltas, o por tramos, y con qué fechas.

55. Responsabilidades ante SERVIU. Solicitamos indicar quién figurará como contratista ante SERVIU (inscripción en el registro, libro de obra y profesional residente), quién paga los derechos de inspección de SERVIU y quién entrega las garantías que SERVIU exija para la recepción de las obras.

56. Horario y accesos. Solicitamos indicar el horario de trabajo permitido, las restricciones municipales de ruido o de faenas en Vitacura y si deben mantenerse habilitados en todo momento los accesos a los predios vecinos, al Club de Polo y al club de golf.

## 7. Correcciones a consultas existentes

Saludo

Texto actual: 'en relación con la solicitud de cotización de Pavimentación y All del proyecto Lo Recabarren'.

Texto propuesto: 'en relación con la solicitud de cotización de Pavimentación y Aguas Lluvias del proyecto Lo Recabarren'.

Consulta 1

Texto actual: Especificaciones técnicas. La carpeta compartida no incluye EETT y la memoria remite a las EETT SERVIU RM. Solicitamos las EETT del proyecto o la confirmación de que rigen las SERVIU vigentes, junto con los ensayos, la topografía, la recepción SERVIU y los planos as built que se exigirán al subcontratista.

Texto propuesto: Especificaciones técnicas y obligaciones de calidad. La carpeta compartida no incluye EETT y la memoria (capítulo 6) remite a las especificaciones de pavimentación del SERVIU Metropolitano y a las normas INN. Solicitamos las EETT del proyecto o la confirmación de que rigen las SERVIU vigentes. Como el itemizado no tiene ítems para las siguientes obligaciones, solicitamos indicar cuáles serán de cargo del subcontratista y en qué ítem se pagan: a) topografía de replanteo y control; b) ensayos de autocontrol y de recepción (densidades, CBR, probetas o testigos de hormigón y espesores); c) pruebas de colectores (estanqueidad o inspección con cámara); d) gestión de la recepción SERVIU; y e) planos as built.

Consulta 2

Texto actual: Movimiento de tierra. El perfil longitudinal muestra que la rasante no sigue al terreno (de -1,31 m en Km 0+600 a +0,41 m en Km 0+400), pero el terreno viene cada 100 m y no hay perfiles transversales. Solicitamos los perfiles transversales o la cubicación de tierra del proyecto, el espesor de escarpe considerado, el esponjamiento a usar y si la subrasante se mide también bajo las soleras.

Texto propuesto: Movimiento de tierra. El perfil longitudinal (láminas 5/10 y 6/10) muestra que la rasante no sigue al terreno: queda 1,31 m bajo el terreno en el Km 0+600 (corte) y 0,41 m sobre el terreno en el Km 0+400 (relleno). El terreno solo está acotado cada 100 m y no hay perfiles transversales. Solicitamos: a) los perfiles transversales o la cubicación de tierra del proyecto; b) el espesor de escarpe a considerar; c) el esponjamiento a usar; d) si el material de corte puede usarse en los terraplenes; y e) si la preparación de subrasante (2.2.2) se mide también bajo las soleras y su cama, lo que agrega entre 650 y 1.290 m2.

Consulta 3

Texto actual: Demoliciones y retiros. No hay cuadro de demolición y retiros. Cercos, rejas, pircas y muros solo aparecen como rótulos, sin largos; los rótulos indican 2 recintos a retirar sin distinguir casa principal y secundaria, 1 portón, 2 pilares, 2 señales y 2 resaltos a demoler (en la capa de resaltos hay 3 elementos). Solicitamos el catastro con cantidades.

Texto propuesto: Demoliciones y retiros. No hay cuadro de demoliciones y retiros. Cercos, rejas, pircas y muros aparecen solo como rótulos, sin largos. Los rótulos indican 2 recintos a retirar, sin distinguir casa principal y casa secundaria, 1 portón, 1 pilar (con 2 pilares dibujados), 2 señales y 2 resaltos a demoler (con 3 resaltos dibujados). Solicitamos el catastro con cantidades para los ítems 2.1.6 a 2.1.14 y 2.1.31 o, si no existe, confirmar que esos ítems se pagarán por la cantidad realmente ejecutada.

Consulta 4

Texto actual: Soleras a retirar. De unos 1.017 m de solera a demoler, 405,8 m están rotulados Manquehue, 28,4 m tipo A y 5,2 m rebajada; 577,6 m no tienen rótulo. El itemizado no tiene ítem para retiro de solera tipo A. Solicitamos confirmar tipos y largos.

Texto propuesto: Soleras a retirar. De unos 1.017 m de solera a demoler (de los que unos 17 m parecen dibujados dos veces), 405,8 m están rotulados Manquehue, 28,4 m tipo A y 5,2 m rebajada, y 577,6 m no tienen rótulo. El itemizado no tiene ítem para el retiro de solera tipo A. Solicitamos indicar el tipo y el largo de cada tramo y en qué ítem se paga el retiro de solera tipo A.

Consulta 5

Texto actual: Material de la calzada a demoler. La lámina 1/10 indica hormigón y la 2/10 calzada asfáltica para la misma superficie. Solicitamos aclarar el material.

Texto propuesto: Material de la calzada a demoler. Los 1.939,8 m2 de calzada a demoler (ítem 2.1.2) están rotulados en planta como 'calzada HCV a demoler', pero la simbología de la lámina 1/10 dice 'calzada de hormigón a demoler' y la de la lámina 2/10, 'calzada asfáltica a demoler'. Solicitamos indicar el material y el espesor de cada sector, y si la demolición incluye la base existente y el transporte a botadero.

Consulta 7

Texto actual: Calzada e=0,17 m. El corte 6-6 (banda de estacionamiento de 3,00 m) indica HCV G35 e=0,17 m y el itemizado pide G30 e=0,17 m. ¿Qué grado rige y en qué tramo va la banda de estacionamiento?

Texto propuesto: Calzada e=0,17 m y banda de estacionamiento. El corte 6-6 (lámina 8/10) indica una banda de estacionamiento de 3,00 m con HCV G35 e=0,17 m sobre base de 0,15 m, y la lámina 10/10 trae el detalle tipo de la banda (3,00 x 5,80 m por estacionamiento), pero en planta no hay ubicación ni largo. El itemizado pide HCV G30 e=0,17 m (2.3.8). Solicitamos indicar qué grado rige, en qué tramos van las bandas y cuántos estacionamientos son.

Consulta 8

Texto actual: Bandejón y franjas. Los cortes muestran un bandejón de 3,00 a 3,50 m y franjas de 1,00 a 1,30 m sin pavimento, con anchos totales de 23,00 a 25,00 m, mientras la memoria indica calzadas de 7,50, 7,00 y 6,50 m. ¿Quién ejecuta el bandejón y las franjas, y quién rellena esas superficies?

Texto propuesto: Bandejón, franjas y anchos de calzada. Los cortes de la lámina 8/10 muestran bandejones de 3,00 a 4,00 m (cortes 1-1, 2-2 y 5-5) y franjas sin pavimento de 1,00 a 1,30 m, que llegan a 3,00 m en el corte 5-5 y a 5,70 m en el corte 4-4. También muestran calzadas de 9,50 m (corte 3-3) y de 9,20 y 4,80 m (corte 4-4), que la memoria no menciona (indica 7,50, 7,00 y 6,50 m). Además, 644,6 m2 de la demolición quedan fuera del pavimento nuevo. Solicitamos indicar quién ejecuta el bandejón y las franjas (relleno, tierra vegetal o paisajismo) y quién rellena las superficies demolidas que no se pavimentan.

Consulta 9

Texto actual: Soleras. El detalle de colocación indica cama de 0,15 m y respaldo de hormigón H-10. ¿El respaldo va incluido en el precio de la solera (2.3.3)? Para el mortero de pega (2.3.4), las barras de traspaso (2.3.18) y las esquinas agudas (2.3.19) no hay cuadro ni dosis: solicitamos el criterio de medición.

Texto propuesto: Soleras. El detalle de colocación de soleras tipo A (lámina 9/10) acota una cama de base de 0,15 m, aunque el dibujo mide unos 0,10 m, y un respaldo de hormigón H-10 de 170 kg cem/m3, del orden de 215 m3 en total. Solicitamos indicar: a) el espesor de cama que rige para el ítem 2.3.17; b) si el respaldo va incluido en el precio de la solera (2.3.3) o en qué ítem se paga; y c) el criterio de medición del mortero de pega (2.3.4), de las barras de traspaso (2.3.18, en kg) y del refuerzo de esquinas agudas (2.3.19, dos barras Ø12 de 1,50 m por esquina), junto con el número de esquinas agudas.

Consulta 10

Texto actual: Accesos y dispositivos de rodado. Hay 29 accesos vehiculares y 31 rebajes de vereda, y el itemizado pide cuatro tipos de dispositivo de rodado sin tipificación. ¿El precio de cada dispositivo incluye su pavimento y su base, o estos se pagan en los ítems de calzada y base?

Texto propuesto: Accesos y dispositivos de rodado. Hay 29 accesos vehiculares (1.107,5 m2 de pavimento HCV sobre base de 0,30 m) y 31 rebajes de vereda, y el itemizado pide cuatro tipos de dispositivo de rodado (2.3.11 a 2.3.14) sin indicar cuál corresponde a cada acceso. Solicitamos: a) la cantidad de cada tipo; y b) indicar si el precio de cada dispositivo incluye su pavimento, su base, la solera tipo C y la superficie antideslizante, o si estos se pagan en los ítems de calzada (2.3.5), base (2.3.7) y solera.

Consulta 11

Texto actual: Resaltos. La lámina 10/10 trae el detalle de resalto, pero no la cantidad ni la ubicación. ¿Cuántos son y en qué ítem se pagan (2.3.14, 2.3.20 o 2.3.22)?

Texto propuesto: Resaltos. La lámina 10/10 trae el detalle de resalto (lomo de toro plano de asfalto, de 6,00 m, con paso de cebra y rejilla prefabricada de aguas lluvias a ambos lados), pero no la cantidad ni la ubicación. Solicitamos indicar cuántos son, dónde van y en qué ítem se paga cada componente: el resalto (2.3.14 o 2.3.20), la rejilla (2.3.22) y la demarcación.

Consulta 12

Texto actual: Notas de la lámina 9/10. Las notas asignan al contratista las redes de servicios no integradas, las autorizaciones y recepciones, el reemplazo de suelo si el CBR es menor a 12 %, el rediseño de la estructura si el CBR real difiere del de diseño, el corte de vereda con cortadora mecánica y una superficie antideslizante de 1,00 m a cada lado en el cruce de acceso con vereda. Ninguna tiene ítem. ¿Se cotizan aparte o se declaran como exclusión?

Texto propuesto: Notas de la lámina 9/10. Las notas asignan al contratista: a) los costos de modificar o trasladar redes de servicios no integradas al proyecto; b) las autorizaciones, aprobaciones, inspecciones y recepciones de las compañías de servicios; c) el rediseño de la estructura de pavimento si el CBR real difiere del 12 % de diseño; d) el reemplazo del suelo natural por subbase granular si la subrasante es orgánica o expansiva, si no alcanza el 95 % del Proctor modificado o si la base no alcanza CBR 60 %, con el espesor indicado en las EETT del proyecto, que no están en los antecedentes; e) el corte de veredas con cortadora mecánica; y f) una superficie antideslizante de 1,00 m a cada lado en el cruce de acceso con vereda. Ninguna tiene ítem. Solicitamos indicar, para cada una, si la asume Demetra, si se paga con un precio unitario adicional (por ejemplo, m3 de reemplazo de suelo, con el espesor a considerar) o si debe declararse como exclusión.

Consulta 13

Texto actual: Largo de colectores DN375. El cuadro de cañerías indica 899 m y la suma de los perfiles da 863,2 m. En el perfil del colector 15 el tramo mide 8,0 m, pero el acumulado pasa de 21,3 a 31,3. ¿Qué cifra rige?

Texto propuesto: Largo de colectores DN375. El cuadro de cañerías indica 899 m y la suma de los perfiles da 863,2 m. En el perfil del colector 15 el tramo mide 8,0 m, pero el acumulado pasa de 21,3 a 31,3. Solicitamos indicar qué largo rige para la oferta y si el pago se hará por esa cifra o por el largo realmente instalado.

Consulta 14

Texto actual: Cámaras decantadoras. Los planos muestran 8 cámaras decantadoras, una por zanja, pero el resumen de la lámina 2/5 indica decantadoras dobles = 0. Solicitamos confirmar que el ítem 2.4.1 (cámara de inspección con decantador) corresponde a esas 8.

Texto propuesto: Cámaras decantadoras. Los planos muestran 8 cámaras decantadoras, una por zanja, pero el resumen de la lámina 2/5 indica 'decantadoras dobles' = 0. Además, la lámina 5/5 detalla los sumideros S-2 y S-3 y las baterías 'con cámara decantadora'. Solicitamos indicar a qué cámaras corresponde el ítem 2.4.1 (cámara de inspección con decantador) y si la cámara decantadora de cada sumidero va incluida en los ítems 2.4.6, 2.4.7 y 2.4.29.

Consulta 17

Texto actual: Entibaciones. Los módulos de las zanjas miden de 3,60 a 4,05 m de alto y las decantadoras llegan a 3,48 m. ¿La entibación (2.5.3, por mes) corre por cuenta del subcontratista y con qué criterio se mide?

Texto propuesto: Entibaciones. Según el detalle de la lámina 4/5, las zanjas de infiltración se excavan a 4,30 m (4,75 m en la N°1: 0,50 m de recubrimiento, módulos de 3,60 a 4,05 m y 0,20 m de gravilla), y las decantadoras llegan a 3,48 m. Solicitamos indicar si se exige entibación o si se acepta excavar con taludes, y cómo se mide y paga el ítem 2.5.3, cuya unidad es el mes (número de meses, metros entibados o equipo considerado).

Consulta 19

Texto actual: Sumideros. El cuadro indica 38 S-2, 4 S-3 y 8 baterías; en el DWG hay 46 bloques de sumidero S-2, 8 S-3 y 4 de otro tipo. ¿Qué cantidad rige? El sumidero 2 se conecta a una C.I. existente: solicitamos su ubicación y estado.

Texto propuesto: Sumideros. El cuadro de la lámina 2/5 indica 38 S-2, 4 S-3 y 8 baterías (16 sumideros), 58 en total. El DWG también tiene 58 sumideros, pero repartidos en 46 S-2, 8 S-3 y 4 de otro tipo. Solicitamos confirmar que el tipo de cada sumidero es el del cuadro. El sumidero 2 se conecta a una C.I. existente, y el DWG rotula un 'sumidero trasladado que se conecta a red existente', que podría ser el ítem 'sumidero a trasladar' (sin código). Solicitamos la ubicación y el estado de esa C.I., y confirmar si la conexión y su eventual reparación se pagan en ese ítem.

Consulta 20

Texto actual: Cámara repartidora y juntas. La lámina 5/5 trae el detalle de una cámara repartidora que no tiene ítem, y las junturas de dilatación (2.4.4) no tienen referencia en los planos.

Texto propuesto: Cámara repartidora y junturas. La lámina 5/5 trae el detalle de una cámara repartidora, y la lámina 4/5 la ubica a la entrada del sistema de infiltración, pero no tiene ítem ni cantidad. Solicitamos indicar cuántas son y si van incluidas en el precio de cada zanja. Las junturas de dilatación (2.4.4, en m2) no tienen referencia en los planos de aguas lluvias: solicitamos indicar a qué elemento corresponden y su cantidad, o si el ítem se anula.

Consulta 21

Texto actual: Cámaras a nivelar (2.5.1). Hay al menos 10 rótulos de cámara a nivelar, uno de ellos en plural. Solicitamos la cantidad exacta.

Texto propuesto: Cámaras a nivelar (2.5.1). Hay 10 rótulos de 'cámara a nivelar cota de anillo', uno de ellos en plural. Solicitamos la cantidad exacta e indicar a qué compañía pertenece cada cámara, ya que nivelar cámaras de agua potable, alcantarillado, electricidad o telecomunicaciones requiere la autorización de la compañía respectiva.

Consulta 22

Texto actual: Proyecto SERVIU 63023. Las intersecciones con Av. Santa María y Agua del Palo aparecen según el proyecto SERVIU 63023, incluida una ciclovía de unos 376 m2. ¿Quedan fuera del alcance? La lámina 2/10 pide además demoler calzada asfáltica en esa intersección, sin ítem.

Texto propuesto: Proyecto SERVIU 63023. Las intersecciones con Av. Santa María y Av. Agua del Palo aparecen según el proyecto SERVIU 63023 y no se incluyeron en nuestras cantidades: del orden de 194 m2 de calzada HCV, 38 a 40 m2 de vereda, 8,3 m2 de baldosa, 63,8 m de solera tipo A y 10,6 m de solera tipo C, 24,1 m2 de demolición y una ciclovía de unos 376 m2. Solicitamos confirmar que esas obras quedan fuera del alcance o, si no, enviar sus cantidades.

(Nota para el remitente: la frase sobre la calzada asfáltica de la lámina 2/10 se quita de la 22 porque esa simbología queda preguntada en la 5 corregida; dejarla en ambas da dos lecturas distintas de la misma simbología.)

Consulta 23

Texto actual: Señalización y demarcación. El DWG trae 33 señales proyectadas, demarcación y 6 bolardos de ciclovía, sin ítem. ¿Corresponden a otra partida? De no recibir respuesta, se declararán como exclusión.

Texto propuesto: Señalización y demarcación. El DWG trae unas 33 señales en la capa de señales proyectadas (algunas rotuladas como existentes), demarcación de pavimento, la demarcación del paso de cebra de los resaltos y 6 bolardos de ciclovía, sin ítem. Solicitamos indicar si corresponden a otra partida y, si son de esta, la cantidad de señales nuevas, de señales a reinstalar y los m2 de demarcación. De no recibir respuesta, se declararán como exclusión.

Consulta 24

Texto actual: Ítems que se repiten. Solicitamos aclarar los pares 2.4.20 y 2.4.29 (baterías), 2.4.19 y 2.4.33 (HDPE DN375; este último sin unidad), 2.1.15 y 2.2.1 (escarpe), 2.1.29 y 2.5.2 (luminarias a trasladar) y 2.3.20 con 2.3.14 (resaltos). La celda E50 del itemizado suma metros cúbicos con metros cuadrados.

Texto propuesto: Ítems que se repiten. Solicitamos indicar, en cada par, cuál ítem se cotiza y cuál queda sin cantidad: 2.4.20 y 2.4.29 (baterías de sumideros); 2.4.19 y 2.4.33 (HDPE DN375; el 2.4.33 no tiene unidad y podría corresponder a la tubería dentro de las zanjas); 2.1.15 y 2.2.1 (escarpe); 2.1.29 y 2.5.2 (luminarias a trasladar; el 2.5.2 no tiene unidad); y 2.3.20 con 2.3.14 (resaltos).

Consulta 25

Texto actual: Árboles. La mayoría de los árboles se indican incluidos en paisajismo (4.1.50), pero la mora (2.1.23) no tiene nota. ¿Se cotiza su retiro?

Texto propuesto: Árboles y mora. La mayoría de los árboles se indican incluidos en paisajismo (4.1.50), pero la mora (2.1.23) no tiene nota y en planta es una zona, no una unidad. Solicitamos indicar si su retiro corresponde a esta partida y, si corresponde, la superficie a despejar y si incluye la extracción de raíces.

Consulta 28

Texto actual: Condiciones comerciales. Solicitamos indicar la forma y el plazo de pago de los estados de pago, el porcentaje de retención y cuándo se devuelve, las garantías exigidas (fiel cumplimiento, anticipo, buena ejecución), los seguros y las multas por atraso.

Texto propuesto: Condiciones comerciales. Solicitamos indicar la periodicidad de los estados de pago y su plazo de pago, el porcentaje de retención y cuándo se devuelve, las garantías exigidas (fiel cumplimiento, anticipo y buena ejecución) con su monto y vigencia, el plazo de garantía de las obras, los seguros exigidos y las multas por atraso, con su tope si lo hay.

Consulta 29

Texto actual: Mecánica de suelos. Solicitamos el informe de mecánica de suelos o, al menos, el CBR de diseño y la ubicación de las calicatas, porque la lámina 9/10 hace depender la estructura y un eventual reemplazo de suelo del CBR real.

Texto propuesto: Mecánica de suelos. Solicitamos el informe de mecánica de suelos o, al menos, el CBR de diseño, la ubicación y estratigrafía de las calicatas y la profundidad de napa, porque la lámina 9/10 hace depender la estructura del CBR real y de las condiciones de la subrasante, y el diseño de aguas lluvias supone que no hay napa freática.

Consulta 31

Texto actual: Botadero y tránsito. ¿El botadero de excedentes es por cuenta del subcontratista? ¿Quién tramita y paga el plan de desvío de tránsito y la señalización provisoria en Av. Santa María y Agua del Palo?

Texto propuesto: Botadero, tránsito y cierres. Solicitamos indicar: a) si el transporte de excedentes a botadero autorizado y su costo son de cargo del subcontratista y si se exigirán certificados de disposición; b) quién tramita y paga el plan de desvío de tránsito y la señalización provisoria en Av. Santa María y Av. Agua del Palo; y c) si se exigen cierres provisorios o cercos de faena, y de cargo de quién.

Cierre del correo

Texto actual: 'Quedamos atentos a sus respuestas.'

Texto propuesto: 'Para las consultas que no tengan respuesta antes del cierre, la oferta declarará el supuesto usado o la exclusión correspondiente. Solicitamos que esos supuestos y exclusiones formen parte del contrato. Quedamos atentos a sus respuestas.'

## Lo que no se revisó

- No remedí en el DWG el reparto de soleras por rótulo (405,8 / 28,4 / 5,2 / 577,6), el tramo de 155 m del corte 1-1, los 863,2 m de perfiles, las 33 señales, los 29 accesos ni las diferencias entre pav.dxf y all.dxf (R8): se aceptan de las auditorías anteriores.
- Las cifras de juntas (~6.000 ml), relleno estructurante (~490 m3) y arena de zanjas (550-650 m3) son estimaciones propias con supuestos escritos en el punto 2; sirven para la consulta, no para valorizar.
- Las láminas pav 2 a 7 y AALL 1 y 3 se revisaron por su texto extraído y no a la vista completa.
- No se pasó el texto por `revisar-textos`; conviene hacerlo antes de enviar.

## 8. Aplicación al correo (11-11-2026)

Se sobrescribió `correo_demetra.txt`: 55 consultas numeradas de corrido en las cinco secciones (Antecedentes 1-8, Pavimentación 9-18, Aguas lluvias 19-32, Alcance e itemizado 33-41, Oferta y condiciones 42-55). Pasó por `revisar-textos`: 2 señales, ambas falsas ('clave' como término técnico de la tubería); no se tocaron.

Aplicado (26 de 26 correcciones, con las salvedades de abajo): saludo (Aguas Lluvias); consultas 1, 2, 3, 4, 5, 7, 8, 9, 10, 11, 12, 13, 14, 17, 19, 20, 21, 22, 23, 24, 25, 28, 29, 31 y cierre. Las 25 consultas nuevas (32 a 56) y la consulta por separador de carril, acceso a trasladar y sumidero a trasladar (en la nueva 33 y en la 29). La consulta del proyecto sin aprobación SERVIU va primera, con la pregunta de quién asume los cambios.

Verificado en la fuente antes de cambiar: nota del CBR de la lámina 9/10 (texto en all/pav.dxf); un solo rótulo 'PILAR A RETIRAR'; 1.939,8 m2, 1.107,5 m2, 644,6 m2, 1.017 m, 9.745 cajas y 38/4/8 sumideros en la cubicación; cortes de la lámina 8/10 a la vista.

Cambios respecto de la propuesta y motivo (los números de este apartado son los de la auditoría; en el correo nuevo la numeración cambió: antiguas 32 a 56 son ahora 1, 3, 4, 16, 17, 13, 23, 24, 25, 31, 26, 33, 36, 38, 39, 40, 41, 44, 45, 46, 47, 49, 53, 54, 55 en ese orden de la auditoría):
- Corrección 8 (bandejón): no se aplicó el 'hasta 4,00 m'. En la lámina 8/10 los bandejones rotulados miden 3,00 a 3,50 m (el 4,00 de la auditoría suma bandejón y franja contigua del corte 2-2). Se aplicó el resto: franjas de hasta 3,00 m (5-5) y 5,70 m (4-4), calzadas de 9,50, 9,20 y 4,80 m y los 644,6 m2.
- Corrección 12 (suelo): la nota dice 'espesor indicado en las EETT y/o perfiles tipo', no solo EETT; se citó ambos. Se reemplazó la frase 'CBR menor a 12 %' por las condiciones reales de la nota.
- Corrección 3: 'pilar' quedó como '1 pilar (con 2 pilares dibujados)'; el '2 pilares dibujados' viene de la auditoría y no se remidió.
- Resto de correcciones: aplicadas sin cambio de fondo.
- Nota de la 22 (quitar la calzada asfáltica de la lámina 2/10): aplicada; el choque con la 5 queda resuelto, la 8 nueva pregunta por el material y la 34 solo por el alcance 63023.
- Corrección 1: se quitó el apartado 'gestión de la recepción SERVIU' (pasó a la consulta 54) para no duplicar.
- Consulta 32 (sin aprobación): se reemplazó 'dado que la solicitud de cotización no admite cambios de precio' por 'con qué mecanismo se ajustará el precio', porque esa afirmación sobre la solicitud no se pudo verificar.
- Consulta 33 (retiros): se agregó 'y a dónde' en el acceso a trasladar.

Fusiones y recortes por superposición: la 24 (ítems repetidos) y la 44 (filas incompletas) pasaron a una sola (36). Se quitaron de la 34 (servicios) los traslados y cruces, que ya cubre la 18; de la 24 (zanjas) la entibación y la cámara repartidora, que cubren la 27 y la 30; de la 26 (infiltración) la napa, que está en la 50; de la 48 el anticipo, que está en la 47; y de la 17 (empalmes) el límite del pavimento, que quedó en la 34. Se movió el texto de cierre sobre supuestos a la consulta 49 y el cierre quedó sin esa petición.

## Re-auditoría (11-11-2026)

Segunda revisión independiente del correo de 55 consultas (`correo_demetra.txt`), sin usar las conclusiones de la auditoría anterior. Fuentes contrastadas de nuevo: itemizado original, memoria Rev 1 (incluidas las tablas de verificación, que son imágenes y no se habían leído), láminas renderizadas (pav 1, 8, 9 y 10; AALL 2 y 4), textos de `all.dxf` y `pav.dxf` y conteo propio de bloques y largos con ezdxf. El correo no se modificó.

Veredicto: no está listo para enviar. Tiene 2 hallazgos de severidad alta (una premisa falsa y una discrepancia memoria-planos sin preguntar), 5 de severidad media y 11 de severidad baja. Con las correcciones de abajo aplicadas, queda listo.

### Verificado sin observaciones

Consultas 1 (Rev 1 'para aprobación SERVIU', recuadro en blanco), 5 (rasante 677,05 / terreno 676,64 en Km 0+400; 681,18 / 682,49 en Km 0+600), 7 (1.017 m en 52 polilíneas; 405,8 + 28,4 + 5,2 + 577,6 = 1.017,0), 11 (cortes 1-1 a 5-5 a la vista), 15 (resalto de 6,00 m, rejilla prefabricada a ambos lados), 16 (tres juntas, CSS-1, JAC-3405, cordón), 18 (texto completo de la nota), 19 (899; 21,3 + 8,0 y acumulado 31,3), 22 (2,4 m3 de 2 a 4 m en el colector 14), 25 (Atlantis 26 t/m2, Hidrocelda, nota del fabricante, 9.745 cajas), 29 (46 + 8 + 4 bloques; 38 + 4 + 16 = 58), 31 (nota de cálculo estructural; decantadora N°7 de 3,48 m), 32 (7 + 1 + 1 + 1 = 10 rótulos), 37, 38, 39, 40 y 10 (banda de 3,00 x 5,80 m). Trato formal correcto, sin voseo, sin comillas angulares ni guiones largos.

No remedido (se acepta de la cubicación): calzada HCV que difiere unos 20 m2 entre DWG (consulta 3), 644,6 m2 (11), 1.107,5 m2 (14), las cifras del proyecto 63023 (34) y el ancho dibujado de 1,64 m de las zanjas 7 y 8 (21).

### Hallazgos

**RC-1. Alta. Consulta 26: premisa falsa.** La consulta dice que la capacidad de infiltración 'no se informa en los antecedentes'. Las siete tablas de verificación de zanjas de la memoria (páginas 7 a 9) indican 'capacidad de infiltración del suelo: 70 mm/hr'. Demetra puede contestar 'está en la memoria' y la consulta queda sin efecto, además de mostrar una lectura incompleta.

Texto propuesto: '26. Capacidad de infiltración. Las verificaciones de las zanjas 1 a 7 de la memoria suponen una capacidad de infiltración del suelo de 70 mm/h, sin indicar el ensayo que la respalda. Solicitamos indicar si ese valor proviene de ensayos en terreno, si se exigirá verificarlo con un ensayo de infiltración antes de construir las zanjas y de cargo de quién, y cómo se pagarán las obras adicionales si el resultado obliga a ampliar o modificar el sistema.'

**RC-2. Alta. La memoria no corresponde a los planos de aguas lluvias vigentes y el correo no lo pregunta.** a) La memoria verifica la zanja N°7 con 29,4 m de largo, 0,8 m de ancho y 3,6 m de profundidad; la lámina 2/5 la rotula con 25,8 m, 2,05 m y 3,60 m (1.720 cajas). Son unas 900 cajas de diferencia, cerca del 10 % del sistema. b) La memoria verifica el colector 15 con 25,6 m de DN375 y 39,0 m de DN400; esos tramos están en `pav.dxf` ('COLECTOR N°14 HDPE DN 400 L=39.0m'), no en `all.dxf` (21,3 + 8,0 m DN375 a la zanja N°8). El itemizado no tiene ítem para DN400. Las zanjas 1 a 6 coinciden con la memoria (con redondeo).

Texto propuesto para la consulta 3, agregar antes de 'Solicitamos confirmar': 'La memoria tampoco coincide con el DWG de aguas lluvias: verifica el colector 15 con un tramo de 25,6 m DN375 y otro de 39,0 m DN400, que corresponden a la versión del DWG de pavimentación, y el itemizado no tiene ítem para tubería DN400.' Y reemplazar la frase final por: 'Solicitamos confirmar cuál archivo rige para pavimentos y cuál para aguas lluvias y si la memoria está vigente, o enviar una versión única vigente.'

Texto propuesto para la consulta 21: '21. Zanjas de infiltración N°7 y N°8. La zanja N°8 está rotulada en la lámina 2/5, pero la memoria solo verifica las zanjas 1 a 7 y la N°8 no tiene detalle propio. Además, la memoria verifica la zanja N°7 con 29,4 m de largo, 0,8 m de ancho y 3,6 m de profundidad, mientras la lámina 2/5 la rotula con 25,8 m, 2,05 m y 3,60 m (1.720 cajas), y en planta las zanjas 7 y 8 se dibujan con 1,64 m de ancho. Solicitamos el detalle de la N°8 y las dimensiones que rigen para las zanjas N°7 y N°8.'

**RC-3. Media. Barras de traspaso: el diámetro del itemizado no coincide con la lámina 10/10.** El ítem 2.3.18 dice 22 mm. La lámina 10/10 indica barra Ø25 lisa de 460 mm cada 300 mm (junta transversal de construcción, acero SAE 1020) y barra Ø12 con resalte de 650 mm cada 750 mm (junta longitudinal de construcción, A63-42H), ambas embebidas en perforaciones con Sikadur 32 o similar en el pavimento existente. La consulta 12 c) pide el criterio de medición sin señalar la diferencia.

Texto propuesto en la consulta 12, reemplazar 'de las barras de traspaso (2.3.18, en kg)' por: 'de las barras de traspaso (2.3.18, en kg, descrito como 22 mm, mientras la lámina 10/10 indica barra Ø25 lisa de 460 mm cada 300 mm en la junta transversal de construcción y barra Ø12 con resalte de 650 mm cada 750 mm en la junta longitudinal, ancladas con Sikadur 32 o similar en perforaciones en el pavimento existente; solicitamos indicar qué diámetro rige y si la perforación y el adhesivo se pagan en ese ítem)'.

**RC-4. Media. Consulta 13: se puede contestar sin resolver nada.** La simbología no confunde los dos tipos: la solera tipo A plinto 0,00 m es segmentada azul y la tipo C es segmentada roja, y el DWG tiene una capa propia para la tipo C (03_S2_Pav ext_Solera Tipo C, 15 tramos, 26,6 m, de los que unos 11 m son del proyecto 63023). Demetra puede responder 'se distinguen por color'. Lo que sí está abierto es el precio de las soleras de plinto 0,00 m y 0,05 m (esta última en el detalle de la banda de estacionamiento, lámina 10/10).

Texto propuesto: '13. Soleras rebajadas y solera tipo C. En planta hay unos 375 m de solera en línea segmentada en la capa de soleras tipo A, que según la simbología corresponden a solera tipo A plinto 0,00 m, y el detalle de la banda de estacionamiento (lámina 10/10) usa solera tipo A rebajada de plinto 0,05 m. La solera tipo C tiene su propia capa, con unos 27 m, de los que unos 11 m pertenecen al proyecto SERVIU 63023. Solicitamos confirmar que las soleras tipo A de plinto 0,00 m y 0,05 m se pagan en el ítem 2.3.3 al mismo precio que la de plinto 0,15 m, y que la solera tipo C de esa capa es la que va incluida en los dispositivos de rodado (2.3.21).'

**RC-5. Media. Consultas 15 y 36 preguntan lo que el itemizado ya contesta.** El itemizado dice en la fila 2.1.15 'Considerado en ítem 2.2.1' y en la 2.3.20 'Incluido en item 2.3.14'. Preguntar cuál de cada par se cotiza invita a responder 'ya está indicado'. Lo que no está resuelto es que el 2.3.14 es un dispositivo de rodado (por unidad) y el resalto se mide en m2 en el 2.3.20.

Texto propuesto para la consulta 36, primera oración: 'En cada uno de los siguientes pares solicitamos indicar cuál ítem se cotiza y cuál queda sin cantidad: 2.4.20 y 2.4.29 (baterías de sumideros); 2.4.19 y 2.4.33 (HDPE DN375; el 2.4.33 no tiene unidad y podría corresponder a la tubería dentro de las zanjas); y 2.1.29 y 2.5.2 (luminarias a trasladar; el 2.5.2 no tiene unidad).' El resto de la consulta se mantiene.

Texto propuesto para la consulta 15, reemplazar 'el resalto (2.3.14 o 2.3.20)' por: 'el resalto (el itemizado lo incluye en el ítem 2.3.14, dispositivo de rodado vereda continua, que se paga por unidad, mientras el 2.3.20 lo mide en m2; solicitamos indicar con qué unidad se paga)'.

**RC-6. Media. Las estimaciones propias revelan la base de costo y no aportan a la respuesta.** Las cifras de 650 a 1.290 m2 (consulta 5), 215 m3 (12), 6.000 ml (16), 490 m3 (23) y 550 a 650 m3 (24) no salen de los planos, sino de supuestos de Reinoso (anchos, espaciamientos, taludes). Demetra puede responder igual sin ellas; en cambio, quedan escritas como cantidades que Reinoso conocía al ofertar (pesa si el contrato resulta a suma alzada), muestran su base de precio y pueden circular a otros oferentes. Recomendación: quitarlas y dejar solo las cifras leídas en planos y cuadros. Las cifras del proyecto 63023 (consulta 34) sí conviene mantenerlas, porque son mediciones del plano y acotan el alcance.

Textos propuestos:
- Consulta 5 e): 'y e) si la preparación de subrasante (2.2.2) se mide también bajo las soleras y su cama.'
- Consulta 12: quitar ', del orden de 215 m3 en total'.
- Consulta 16: reemplazar 'El itemizado no tiene ítem para el corte y sello de juntas, que estimamos del orden de 6.000 ml en la calzada.' por 'El itemizado no tiene ítem para el corte y sello de juntas.'
- Consulta 23: reemplazar 'Para 899 m de DN375 y 385 m de DN300 estimamos unos 490 m3 de relleno estructurante.' por 'Esto afecta a los 899 m de DN375 y a los 385 m de DN300 del cuadro de cañerías.'
- Consulta 24: ver RC-10 (texto sin la estimación de arena).

**RC-7. Media. Consulta 14: mezcla accesos vehiculares con rebajes de vereda y deja sin ítem los rebajes.** La lámina 9/10 detalla el 'rebaje de vereda con espacio reducido de acera de esquina tipo II' (peatonal) y el DWG tiene 31 rebajes (capa 03_Pav proy_Rebaje de vereda), sin ítem en el itemizado. Además, la consulta da por hecho la base de 0,30 m en accesos, que la consulta 9 pregunta, y pregunta si el dispositivo incluye la solera tipo C, que el itemizado ya responde (nota del 2.3.21). La lámina 9/10 solo trae la isométrica del 'acceso tipo 1'.

Texto propuesto: '14. Accesos, dispositivos de rodado y rebajes de vereda. Hay 29 accesos vehiculares (1.107,5 m2 de pavimento HCV) y el itemizado pide cuatro tipos de dispositivo de rodado (2.3.11 a 2.3.14) sin indicar cuál corresponde a cada acceso; la lámina 9/10 solo trae la isométrica típica del acceso tipo 1. Además, hay 31 rebajes de vereda y la lámina 9/10 detalla el rebaje de vereda con espacio reducido de acera de esquina tipo II, sin ítem en el itemizado. Solicitamos: a) la cantidad de cada tipo de dispositivo; b) indicar si el precio de cada dispositivo incluye su pavimento, su base y la superficie antideslizante, o si estos se pagan en los ítems de calzada (2.3.5) y de base (2.3.6 o 2.3.7, según el espesor que rija conforme a la consulta 9); y c) si los 31 rebajes de vereda son peatonales o corresponden a los accesos, y en qué ítem se pagan.'

**RC-8. Baja. Consulta 20: el S-3 no se detalla 'con cámara decantadora'.** En la lámina 5/5 los títulos son 'sumideros tipo S-2 con cámara decantadora', 'sumidero tipo S-3' y 'batería sumidero con cámara decantadora y rejilla lateral'.

Texto propuesto: reemplazar 'Además, la lámina 5/5 detalla los sumideros S-2 y S-3 y las baterías 'con cámara decantadora'.' por 'Además, la lámina 5/5 detalla los sumideros S-2 y las baterías 'con cámara decantadora'.', y 'si la cámara decantadora de cada sumidero va incluida en los ítems 2.4.6, 2.4.7 y 2.4.29' por 'si la cámara decantadora de cada sumidero va incluida en los ítems 2.4.6 y 2.4.29, y si el sumidero S-3 (2.4.7) lleva cámara decantadora'.

**RC-9. Baja. Consulta 23: la descripción del relleno estructurante es inexacta.** '(grava y arena, tamaño máximo 1½")' describe solo el suelo clase II. La clase III es grava con arcilla o limo, arenas arcillosas o limosas (95 % de la D.M.C.S.), lo que podría cumplir el propio material de excavación. El relleno final exige además tamaño máximo de 75 mm (posible harneo).

Texto propuesto: '23. Relleno de zanjas de colectores. La sección típica de tubería HDPE de la lámina 5/5 exige relleno estructurante hasta 20 cm sobre la clave, de suelo clase II (grava, arenas gruesas y mezclas de grava y arena, tamaño máximo 1½", compactado a 90 % de la D.M.C.S.) o clase III (grava con arcilla o limo, arenas arcillosas o limosas, compactado a 95 %), y admite material de excavación solo en el relleno final, compactado a 95 % del Proctor modificado y con tamaño máximo de 75 mm. El itemizado indica que el relleno estructural (2.4.5) va incluido en el relleno con material de excavación (2.4.22). Esto afecta a los 899 m de DN375 y a los 385 m de DN300 del cuadro de cañerías. Solicitamos indicar en qué ítem y con qué unidad se paga el relleno estructurante si es de empréstito, si Demetra acepta usar el material de excavación cuando cumpla la clase II o III, y si el harneo del relleno final se paga en el ítem 2.4.22.'

**RC-10. Baja. Consultas 24 y 27: la excavación de 4,30 m no está acotada y el 2.4.25 no es global.** El detalle acota 0,50 m 'mín. a sello base' bajo el área verde proyectada, módulos de 3,60 m (4,05 m en la N°1) y 0,20 m de gravilla: 4,30 m es un mínimo calculado, más el espesor del área verde, y las paredes se dibujan con talud. El 2.4.25 (zanja N°8) tiene unidad N°, no gl.

Texto propuesto para la consulta 24: '24. Contenido del precio de cada zanja de infiltración. El detalle de la lámina 4/5 indica para cada zanja una excavación de al menos 4,30 m (4,75 m en la N°1), cama de gravilla bajo 1½" de 0,20 m, módulos envueltos en geotextil de polipropileno no tejido de 200 g/m2 y relleno lateral y superior de arena gruesa y limpia. Solicitamos confirmar qué incluye el precio de cada zanja (2.4.10 a 2.4.16, en gl, y 2.4.25, en N°): excavación, agotamiento, gravilla, geotextil, módulos, arena, tubería interior, relleno, retiro de excedentes y reposición del área verde sobre la zanja.'

Texto propuesto para la consulta 27, primera oración: 'Según el detalle de la lámina 4/5, las zanjas de infiltración se excavan a al menos 4,30 m (4,75 m en la N°1: 0,50 m de recubrimiento mínimo bajo el área verde, módulos de 3,60 a 4,05 m y 0,20 m de gravilla), con las paredes dibujadas en talud, y las decantadoras llegan a 3,48 m.'

**RC-11. Baja. Consulta 35: '33 señales' no se puede sostener y la última frase repite el cierre.** En `pav.dxf` la capa 00_Señal proy 01 tiene 31 bloques con nombre de señal y otros anónimos; en `all.dxf`, 26. La frase 'De no recibir respuesta, se declararán como exclusión.' duplica el párrafo de cierre del correo.

Texto propuesto: reemplazar 'El DWG trae unas 33 señales en la capa de señales proyectadas' por 'El DWG trae señales en la capa de señales proyectadas', y eliminar 'De no recibir respuesta, se declararán como exclusión.'

**RC-12. Baja. Consulta 6: las señales no son 'a demoler'.** Los 2 rótulos dicen 'señal a trasladar' (ítem 2.1.25).

Texto propuesto: reemplazar '2 señales y 2 resaltos a demoler' por '2 señales a trasladar y 2 resaltos a demoler'.

**RC-13. Baja. Consultas 29 y 33: el itemizado no trae cantidades.** '1 unidad' y '2 unidades' son conteos de rótulos de Reinoso, no del itemizado.

Texto propuesto: en la 29, reemplazar '(1 unidad, sin código)' por '(sin código ni cantidad; hay 1 rótulo)'; en la 33 b), reemplazar '(2 unidades, sin código)' por '(sin código ni cantidad; hay 2 rótulos)'.

**RC-14. Baja. Consulta 4: 'tuberías de 300 y 500 mm' cuenta dos veces el colector de 500 mm.** La topografía rotula 'colector ALL existente D=500mm' y 'D. 300 mm'.

Texto propuesto: reemplazar '(colector de aguas lluvias D=500 mm, tuberías de 300 y 500 mm, un pozo y cámaras' por '(un colector de aguas lluvias D=500 mm, una tubería de 300 mm, un pozo y cámaras'.

**RC-15. Baja. Cobertura: sumideros existentes.** La topografía (capa Z-SUM) tiene 12 sumideros existentes, 4 de ellos a menos de 9 m del pavimento HCV nuevo, y solo uno está rotulado 'a trasladar'. Si quedan bajo la calzada, su retiro o anulación no tiene ítem.

Texto propuesto, agregar al final de la consulta 29: 'La topografía muestra además sumideros existentes junto a la calzada proyectada, de los que solo uno está rotulado a trasladar. Solicitamos indicar si los demás se retiran, se anulan o se mantienen, y en qué ítem se paga.'

**RC-16. Baja. Cobertura: escalines y satélites de refuerzo.** El resumen de cámaras de la lámina 2/5 cuenta 59 escalines y 37 satélites de refuerzo, sin ítem.

Texto propuesto, agregar al final de la consulta 31: 'El resumen de cámaras de la lámina 2/5 incluye además 59 escalines y 37 satélites de refuerzo, sin ítem: solicitamos confirmar que van incluidos en el precio de cada cámara.'

**RC-17. Baja. Consulta 50: no usa que la memoria cita el informe.** La memoria (capítulo 4) dice que el CBR de 12 % es 'de acuerdo a lo indicado en el informe de Mecánica de Suelos'; el informe existe y no está en la carpeta.

Texto propuesto: reemplazar 'Solicitamos el informe de mecánica de suelos o, al menos,' por 'La memoria (capítulo 4) indica que el CBR de diseño de 12 % proviene del informe de mecánica de suelos, que no está en los antecedentes. Solicitamos ese informe o, al menos,'.

**RC-18. Baja. Cobertura: demolición de veredas.** La consulta 8 pregunta material, espesor, base y botadero solo para la calzada; los 569,7 m2 de vereda a demoler (2.1.1, 7 rótulos 'vereda a demoler') tienen la misma duda.

Texto propuesto, en la consulta 8 reemplazar 'y si la demolición incluye la base existente y el transporte a botadero.' por 'y si la demolición de calzada (2.1.2) y de veredas (2.1.1) incluye la base existente y el transporte a botadero.'

### Riesgo de redacción (resumen)

Además de RC-6, no hay frases que comprometan a Reinoso: la consulta 1 deja abierto el ajuste de precio, la 6 y la 19 piden pago por cantidad ejecutada como alternativa, la 44 pregunta la modalidad del contrato y el cierre reserva supuestos y exclusiones. La frase 'no se incluyeron en nuestras cantidades' (34) es aceptable porque define el alcance.

### Lo que no se revisó

Láminas pav 2 a 7 y AALL 1, 3 y 5 solo por su texto extraído; el cuadro de sumideros no se releyó fila por fila; no se verificó la ubicación de los 12 sumideros existentes respecto de la calzada más allá de la distancia a vértices del hatch; los 97 círculos de la capa 01_Dem Ext_Transl_niv.anillo no se identificaron (podrían ser más cámaras a nivelar que los 10 rótulos; la consulta 32 ya pide la cantidad exacta).

### Aplicación de las correcciones (11-11-2026)

Aplicados los 18 RC en el correo (55 consultas). Ninguno quedó sin aplicar. Decisiones: RC-9 incluye el cambio de RC-6 en la consulta 23; RC-10 reemplaza la estimación de arena de la consulta 24 (RC-6); RC-5 saca de la consulta 36 el par 2.1.15 y 2.2.1 y el par de resaltos, ya cubiertos por el itemizado y por la consulta 15; RC-7 quita de la 14 la solera tipo C, que la 13 (RC-4) ya trata, sin contradicción. Además se retiraron todas las estimaciones propias (6.000 ml, 490 m3, 215 m3, 550 a 650 m3, 650 a 1.290 m2); se mantienen las cifras medidas en planos y las del proyecto 63023. RC-1 a RC-3 se aplicaron según las lecturas de la re-auditoría (tablas de la memoria, que son imágenes); no se releyeron. revisar-textos: 2 señales iniciales (consulta 23), corregidas; quedan 0.

## Depuración

Correo reducido de 55 a 34 consultas (11-11-2026): tono de confirmación de alcance, sin señalar errores del mandante; respaldo previo en correo_demetra_eugenio.txt. revisar-textos: 1 señal (consulta 3), se mantiene porque es la redacción pedida por Eugenio.

Eliminadas:
- 13 (soleras rebajadas plinto 0,00 y 0,05, solera tipo C): sutil, no mueve el precio.
- 28 (rejillas de batería 8 o 16, conexiones DN375): sutil.
- 29 (tipos de sumidero y sumideros existentes): diferencias de conteo con efecto menor.
- 32 (cámaras a nivelar): conteo de rótulos; la autorización de compañías ya está en la consulta de notas de la lámina 9/10.
- 33 (separador de carril, acceso a trasladar, pirca y talud): conteo de rótulos, monto menor.
- 36 (ítems repetidos y filas sin código): códigos de fila, no mueve el precio.
- 37 (mora): sutil.
- 38 (canal proyectado): ya resuelto en la memoria, que lo deja en tramitación aparte.
- 41 (materiales del mandante): obvia.
- 46 (formato del análisis de precios y leyes sociales): Demetra ya entregó el formato con el itemizado.
- 49 (supuestos y exclusiones como parte del contrato): sonaba a exigencia; integrada con suavidad en el párrafo final.
- 51 (instalación de faenas, agua, energía, acopio): obvia, de cargo del contratista.
- 52 (botadero y certificados, plan de desvío, cierres de faena): obvia.
- 54 (responsabilidades ante SERVIU): obvia.
- 55 (horario, restricciones municipales y accesos a vecinos): obvia.

Fundidas:
- 7 (soleras a retirar) en 6 (demoliciones y retiros): mismo catastro; sin los 17 m duplicados ni los rótulos.
- 12 (soleras): queda solo el respaldo; las barras de traspaso pasan a juntas; salen cama 0,15 contra 0,10, mortero y esquinas agudas por sutiles.
- 17 (empalmes) en 16 (juntas): misma faena sobre el pavimento existente.
- 22 (excavaciones de aguas lluvias) en 23 (relleno de zanjas): mismo criterio de medición; sale el colector 14 (2,4 m3) y el harneo.
- 30 (cámara repartidora) en 24 (contenido de cada zanja); las junturas de dilatación salen por sutiles.
- 40 (demolición de casas) en 53 (entrega del terreno): quedan empalmes y asbesto; salen permiso de demolición y visita a terreno por obvios.
- 48 (condiciones comerciales) con 47 (anticipo y vigencia).
- 42 (cierre y formato): queda solo la fecha de cierre, en tono cordial; formato y medio de envío salen por estar resueltos en la solicitud.

Recortes dentro de consultas que se conservan: 2 (topografía, ensayos de autocontrol, as built), 3 (20 m2 de HCV y 31 contra 32 rebajes), 6 (1 pilar contra 2, resaltos dibujados), 8 (transporte a botadero), 19 (acumulado del colector 15), 20 (decantadoras dobles y S-3), 31 (escalines y satélites), 45 (IVA), 50 (CBR de diseño, ya dado en la memoria).

## Auditoría de obviedades (11-11-2026)

Revisión independiente del correo de 34 consultas, con criterio de subcontratista de pavimentación SERVIU y aguas lluvias. No se modificó el correo. Criterio: OBVIA = la responde la práctica habitual, las EETT SERVIU, la memoria, la solicitud o el itemizado; SUTIL = no mueve el precio de forma relevante; ÚTIL = cambia cantidad, precio o riesgo. Cifras contrastadas por muestreo contra la memoria (CBR 12 %, base 15 cm, capítulo 6 EETT SERVIU), los DXF (Atlantis, Hidrocelda, 26 t, G35, Sikadur, JAC, 63023) y el itemizado de `Cubicacion LoRecabarren.xlsx` (2.3.8, 2.3.11 a 2.3.14, 2.3.22 sin cantidad; 2.3.20 incluido en 2.3.14 según nota de Demetra; señalización y demarcación sin ítem).

Resultado: 4 OBVIAS, 7 SUTILES y 23 ÚTILES. Se proponen 8 eliminaciones (2, 9, 11, 13, 16, 26, 31, 32), 3 fusiones (22 en 33, 29 en 34, 13 en 12), 1 traslado al cierre (28) y recortes en 15 consultas. El correo quedaría en 23 consultas.

| N° | Veredicto | Qué sacar y por qué |
|---|---|---|
| 1 | ÚTIL | Sacar cómo se valorizan las obras por observaciones SERVIU y el mecanismo de ajuste: es aumento de obra a precio unitario de contrato y lo cubre la 30. |
| 2 | OBVIA | Eliminar: la memoria (capítulo 6) ya fija las EETT SERVIU vigentes; además 'no encontramos especificaciones particulares' insinúa un faltante. |
| 3 | ÚTIL | Sin cambio: DN400 sin ítem y descarga distinta del colector 15 mueven cantidad. |
| 4 | ÚTIL | Sacar de cargo de quién son las calicatas (siempre del contratista) y la reparación de servicios no catastrados (va como supuesto en la oferta; la 15 trata las redes). |
| 5 | ÚTIL | Sacar esponjamiento (factor propio del oferente) y espesor de escarpe (EETT SERVIU y terreno); sacar 'el terreno está acotado cada 100 m', que suena a reparo. |
| 6 | ÚTIL | Dejar solo el catastro de los ítems globales; sacar tipo de cada tramo de solera, ítem de la solera tipo A (el retiro cuesta lo mismo) y pago por cantidad ejecutada (lo cubre la 30). |
| 7 | ÚTIL | Sin cambio: material y espesor de 1.939,8 m2 cambian el precio de demolición. |
| 8 | ÚTIL | Sin cambio: 15 contra 30 cm de base en accesos y 155 m del corte 1-1 mueven del orden de 300 m3 de base. |
| 9 | SUTIL | Eliminar: G30 contra G35 en una banda pequeña es diferencia menor de precio; la cantidad de 2.3.8 se oferta como precio unitario. |
| 10 | ÚTIL | Sacar los anchos de calzada (la cantidad la da el itemizado y el riesgo lo cubre la 30) y la frase 'mientras que la memoria menciona', que contrasta documentos. |
| 11 | OBVIA | Eliminar: en SERVIU la solera colocada incluye cama y respaldo de hormigón. |
| 12 | ÚTIL | Sacar superficie antideslizante (incluida en el precio) y el ítem de los 31 rebajes (parte de la vereda); se le agrega el conteo de resaltos de la 13. |
| 13 | SUTIL | Fundir en la 12 solo el conteo de resaltos: Demetra ya anotó que 2.3.20 va en 2.3.14 y la rejilla tiene su ítem 2.3.22. |
| 14 | ÚTIL | Sacar ítem de corte y sello (incluido en el HCV según EETT SERVIU), espaciamiento (lo fija la EETT), diámetro (se paga por kg) y forma de unión (está en el detalle). Quedan perforación con adhesivo y reposición de losas existentes. |
| 15 | ÚTIL | Sacar cortadora mecánica y antideslizante: métodos incluidos en el precio, no riesgos. |
| 16 | SUTIL | Eliminar: 35,8 m de DN375 solo importan a suma alzada, que pregunta la 30; además contrasta cuadro contra perfiles. |
| 17 | ÚTIL | Sin cambio: define en qué ítem se pagan 8 decantadoras de hasta 3,48 m. |
| 18 | ÚTIL | Sacar 'si existe, enviarnos el detalle de la N°8', que insinúa un faltante; basta con las dimensiones. |
| 19 | ÚTIL | Sacar si se acepta el material de excavación clase II o III (la lámina ya lo admite) y el criterio de medición de excavación, cama y excedentes (EETT SERVIU); acortar la descripción de suelos. |
| 20 | ÚTIL | Sacar la lista de componentes (un global incluye todo lo del detalle) y el agotamiento (la memoria considera sin napa). Quedan área verde y cámara repartidora. |
| 21 | ÚTIL | Sin cambio: 9.745 cajas son la mayor partida de aguas lluvias. |
| 22 | SUTIL | Fundir en la 33: el ensayo de infiltración cuesta poco, quién lo paga y cómo se valorizan adicionales son obvios. |
| 23 | ÚTIL | Sacar si se exige entibación o talud: es método del contratista según NCh 349 y la mecánica de suelos. Queda cómo se paga 2.5.3 por mes. |
| 24 | ÚTIL | Sin cambio: armaduras de cámaras de hasta 3,48 m y de la repartidora cambian el precio. |
| 25 | ÚTIL | Sin cambio: unos 376 m2 de ciclovía y 194 m2 de HCV definen el alcance. |
| 26 | SUTIL | Eliminar: señales y demarcación no tienen ítem; se declaran como exclusión en la oferta. |
| 27 | ÚTIL | Sacar quién tramita (es del contratista); dejar quién paga los cargos de la distribuidora y la municipalidad, que no se pueden cotizar. |
| 28 | SUTIL | Pasar al párrafo de cierre como una frase; no es una consulta técnica. |
| 29 | SUTIL | Fundir en la 34: el plazo lo propone el oferente según la solicitud; solo importa la fecha estimada de inicio. |
| 30 | ÚTIL | Sacar cómo se valorizan aumentos y obras extraordinarias (precios unitarios del contrato) y 'incluidas las que resulten de las respuestas a estas consultas', que anticipa faltantes. |
| 31 | OBVIA | Eliminar: pesos según el itemizado; el reajuste lo propone el oferente en sus condiciones. |
| 32 | OBVIA | Eliminar: la solicitud pide al oferente proponer anticipo, forma y plazo de pago, estados de pago y vigencia; retención, garantías, seguros y multas son del contrato tipo de Demetra. |
| 33 | ÚTIL | Sin recorte; absorbe la capacidad de infiltración de la 22. |
| 34 | ÚTIL | Sacar empalmes cortados (trámite del propietario antes de entregar); absorbe la fecha de inicio de la 29. |

### Textos propuestos

1. Aprobación del proyecto. Las 15 láminas corresponden a la revisión 1, de septiembre de 2025, emitida para aprobación del SERVIU. Les agradeceríamos indicar si el proyecto ya cuenta con la aprobación del Servicio de Vivienda y Urbanización (SERVIU) o si el trámite sigue en curso.

4. Servicios existentes. Las láminas muestran instalaciones existentes cercanas a las obras: un colector de aguas lluvias de D=500 mm, una tubería de 300 mm, un pozo y cámaras de alcantarillado, y redes de agua potable, electricidad y teléfonos. Les agradeceríamos enviarnos el catastro de servicios con que cuente el mandante, con sus cotas si las tiene.

5. Movimiento de tierra. En el perfil longitudinal de las láminas 5/10 y 6/10, la rasante queda 1,31 m bajo el terreno en el Km 0+600 y 0,41 m sobre él en el Km 0+400. Para valorizar el corte y el relleno, les agradeceríamos enviarnos los perfiles transversales o la cubicación de tierra, si se dispone de ellos, e indicarnos si el material de corte puede usarse en los terraplenes.

6. Demoliciones y retiros. Los ítems 2.1.6 a 2.1.14 y 2.1.31 consideran cercos, rejas, pircas, muros y recintos. ¿Podrían enviarnos el catastro de demoliciones con sus cantidades?

10. Bandejón y franjas. Los cortes de la lámina 8/10 muestran bandejones de 3,00 a 3,50 m y franjas sin pavimento de 1,00 a 1,30 m, que llegan a 3,00 m en el corte 5-5 y a 5,70 m en el corte 4-4. Les agradeceríamos confirmar si el bandejón y las franjas, con su relleno, tierra vegetal o paisajismo, forman parte de esta partida, y si le corresponde rellenar los 644,6 m2 de superficie demolida que no se vuelven a pavimentar.

12. Dispositivos de rodado y resaltos. Hay 29 accesos vehiculares, con 1.107,5 m2 de pavimento HCV, y el itemizado considera cuatro tipos de dispositivo de rodado (2.3.11 a 2.3.14). Les agradeceríamos indicar cuántos dispositivos corresponden a cada tipo y si su precio incluye el pavimento y la base, o si estos se consideran en los ítems de calzada (2.3.5) y de base (2.3.6 o 2.3.7). Quisiéramos saber también cuántos resaltos como el de la lámina 10/10 considera la partida.

14. Juntas y empalmes. La lámina 10/10 indica barras con resalte Ø12 de 650 mm cada 750 mm en la junta longitudinal, ancladas con Sikadur 32 o similar en perforaciones en el pavimento existente. Quisiéramos confirmar si la perforación y el adhesivo se incluyen en el ítem 2.3.18 y en qué ítem se considera la reposición de losas, soleras o veredas existentes que resulten afectadas en los empalmes con Av. Santa María y Av. Agua del Palo.

15. Notas de la lámina 9/10. Las notas de esta lámina asignan al contratista algunas obligaciones cuyo tratamiento quisiéramos confirmar: los costos de modificar o trasladar redes de servicios no integradas al proyecto; las autorizaciones, aprobaciones, inspecciones y recepciones de las compañías de servicios; el rediseño de la estructura de pavimento si el CBR real difiere del 12 % de diseño, y el reemplazo del suelo natural por subbase granular si la subrasante tiene suelos orgánicos o arcillas expansivas, si no alcanza el 95 % del Proctor modificado o si la base no llega a un CBR de 60 %. Para cada una, les agradeceríamos indicar si la asume Demetra, si se paga con un precio unitario adicional, por ejemplo por m3 de reemplazo de suelo con el espesor que debamos considerar, o si corresponde dejarla como exclusión de la oferta.

18. Zanjas de infiltración N°7 y N°8. La memoria considera la zanja N°7 con 29,4 m de largo, 0,8 m de ancho y 3,6 m de profundidad, y la lámina 2/5 la rotula con 25,8 m, 2,05 m y 3,60 m, con 1.720 cajas. En planta, las zanjas 7 y 8 tienen 1,64 m de ancho. Para cotizar sobre la versión vigente, ¿podrían confirmarnos qué dimensiones rigen para las zanjas N°7 y N°8?

19. Relleno de zanjas de colectores. La sección típica de tubería HDPE de la lámina 5/5 considera, hasta 20 cm sobre el tubo, un relleno estructurante de suelo clase II o clase III, y según el itemizado el relleno estructural (2.4.5) va incluido en el relleno con material de excavación (2.4.22), para los 899 m de DN375 y los 385 m de DN300. Les agradeceríamos indicar en qué ítem y con qué unidad se considera el relleno estructurante cuando el material de excavación no cumpla y deba ser de empréstito.

20. Contenido del precio de cada zanja de infiltración. El itemizado mide las zanjas como global en los ítems 2.4.10 a 2.4.16 y por número en el ítem 2.4.25, y la lámina 4/5 ubica una cámara repartidora a la entrada del sistema, detallada en la lámina 5/5. Les agradeceríamos confirmar si el precio de cada zanja incluye la reposición del área verde sobre ella y la cámara repartidora, y cuántas cámaras repartidoras son.

23. Entibaciones. Las zanjas de infiltración se excavan a al menos 4,30 m, y a 4,75 m en la N°1, y las decantadoras llegan a 3,48 m. Les agradeceríamos indicar cómo se mide y paga el ítem 2.5.3, cuya unidad es el mes: por número de meses, por metros entibados o según el equipo considerado.

27. Luminarias y postes. El itemizado considera trasladar 7 luminarias (2.1.29) y 1 poste de fierro, y retirar 1 poste de madera con luminaria. ¿Incluye el traslado la fundación, la canalización, el cableado y la reconexión? Les agradeceríamos indicar también si los cargos de la distribuidora eléctrica y de la Municipalidad de Vitacura son de cargo de Demetra, y si existe un proyecto de alumbrado que debamos considerar.

30. Modalidad del contrato. ¿Será el contrato a suma alzada sobre las cantidades de la oferta o a precios unitarios, con pago de las cantidades realmente ejecutadas?

33. Mecánica de suelos e infiltración. Según el capítulo 4 de la memoria, el CBR de diseño de 12 % proviene del informe de mecánica de suelos; la lámina 9/10 relaciona la estructura con el CBR real y las condiciones de la subrasante, y el diseño de aguas lluvias considera que no hay napa freática y una capacidad de infiltración de 70 mm/h. Les agradeceríamos enviarnos ese informe o, al menos, la ubicación y la estratigrafía de las calicatas y la profundidad de la napa, e indicarnos si se exigirá un ensayo de infiltración antes de construir las zanjas.

34. Inicio y entrega del terreno. Quisiéramos conocer la fecha estimada de inicio de la partida y saber si la faja de la obra se entregará completa, con los predios desocupados y las cesiones resueltas, o por tramos, y en ese caso con qué fechas. Respecto de la casa principal y la casa secundaria de los ítems 2.1.7 y 2.1.31, les agradeceríamos indicar si hay antecedentes de materiales con asbesto que requieran retiro especial.

Cierre, primera frase propuesta (reemplaza la consulta 28): Les agradeceríamos además confirmarnos la fecha de cierre para la recepción de la oferta.

### Tono

Frases que todavía insinúan un error o faltante del mandante: 'en la carpeta compartida no encontramos especificaciones particulares del proyecto' (2); 'y el terreno está acotado cada 100 m' (5); 'mientras que la memoria menciona anchos de 7,50, 7,00 y 6,50 m' (10); 'El ítem 2.3.8 considera HCV G30' como contraste (9); 'El ítem 2.3.18 describe barras de 22 mm' como contraste (14); 'la suma de los perfiles da 863,2 m' (16); 'si existe, enviarnos el detalle de la N°8' (18); 'incluidas las que resulten de las respuestas a estas consultas' (30). Todas desaparecen con los textos propuestos o con la eliminación de la consulta. Los contrastes que quedan en 3, 8 y 18 son la pregunta misma y están redactados como confirmación de versión vigente. Aparte del tono, la introducción mezcla 'les enviamos' con 'que nos envió': conviene 'que nos enviaron'.

### Lo que no se revisó

La solicitud de Demetra no estaba en los antecedentes: se usó la descripción del encargo (antecedentes de la empresa, APU, alcance, plazo y condiciones comerciales). Si la solicitud trae la fecha de cierre, la frase del cierre también sobra. Las tablas de infiltración de la memoria son imágenes y no se releyeron; las cifras de las consultas se tomaron como verificadas por las auditorías anteriores salvo el muestreo indicado.

### Aplicado (11-11-2026)

Se aplicaron al correo los textos propuestos, con las excepciones de Eugenio: la 9 (grado G35 contra G30) y la 16 (largo DN375, 899 m contra 863,2 m) se mantienen como consultas cortas y cordiales; la 14 conserva la pregunta del ítem de corte y sello de juntas; la 28 (fecha de cierre) se mantiene como consulta, porque la solicitud de Demetra no trae fecha. Eliminadas 2, 11, 26, 31 y 32; fundidas 13 en 12, 22 en 33 y 29 en 34; recortes y frases de tono según la tabla; 'que nos envió' cambiado por 'que nos enviaron'. Renumerado de corrido: el correo queda en 26 consultas, con secciones, párrafo final y firma intactos. Respaldo previo: correo_demetra_34.txt. revisar-textos: 0 señales.
