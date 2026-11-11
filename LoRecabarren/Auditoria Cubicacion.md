# Auditoría de la cubicación Lo Recabarren (AUD-2026-11-10)

Fecha: 10-11-2026. Objeto: `LoRecabarren/Cubicacion LoRecabarren.xlsx` (oferta Reinoso a Demetra, partida 2 Pavimentación y Aguas Lluvias). Método: `~/.orquestador/regla-auditorias.md` (evidencia, cobertura, destino). El xlsx no se modificó.

Vara usada: itemizado original `~/Downloads/13.08.26 - Presupuesto Lo Recabarren.xlsx`, láminas Rev 1 (pav 1-10, all 1-5), memoria Rev 1 y DXF `antecedentes/dxf/pav.dxf` y `all.dxf`. Mediciones propias con ezdxf 1.4.5 y shapely 2.2 (venv del scratchpad), con scripts nuevos, sin reutilizar los del autor. Las bases de licitación o la carta de Demetra no están en la carpeta: el punto 8 se audita contra la lista de requisitos que entregó Eugenio.

## Veredicto

**No apta para valorizar.** Las cantidades medidas se reproducen con diferencias de 0,05 % o menos, pero hay 4 hallazgos de severidad alta abiertos: una zanja de infiltración completa omitida, base de 0,30 m sin cubicar, 36 de 77 ítems sin cantidad y ninguna de las piezas de la oferta que pide Demetra.

Resumen por severidad: 4 altas, 9 medias y 5 bajas (18 hallazgos).

## 1. Integridad frente al itemizado original (verificado)

- Comparación celda a celda de las columnas B a H en las 192 filas: 0 diferencias. Las celdas combinadas (17 rangos) y los nombres definidos (`termino`, `vuelta`) son iguales. No hay filas ocultas, perdidas ni movidas. El autor solo agregó las columnas I-K (Fuente, Método, Observación), las cantidades en E y la hoja 'Consultas Demetra'.
- Subtotales intactos: G43 `=SUM(G9:G42)`, G51 `=SUM(G45:G49)`, G76 `=SUM(G53:G75)`, G111 `=SUM(G78:G110)`, G117 `=SUM(G113:G116)`, G118 suma de los cinco. Ver AUD-2026-11-10-6 sobre el uso de la columna G.
- De los 20 rótulos '[INCLUIDO SEGÚN DEMETRA]', 18 corresponden a una nota real de Demetra en la fila (F31-F37, F39-F42, E46, H72, E73, E82, E101, E107, E108). Los otros 2 están en encabezados de sección (AUD-2026-11-10-5).

## 2. Mediciones propias en el DXF (verificado)

| Cantidad | Autor | Medición propia | Diferencia |
|---|---|---|---|
| 2.3.5 Calzada HCV (hatch SWAMP color 256 + 150) | 17.300,2 m2 | 17.302,7 m2 (unión) | +0,01 % |
| 2.3.1 Vereda e=0,07 (DOTS color 256) | 4.349,7 m2 | 4.348,7 m2 | -0,02 % |
| 2.3.3 Solera tipo A (capa 03_Pav proy_Solera Tipo A, a 35 m o menos del eje) | 4.305,6 ml | 4.305,6 ml (3.930,3 continua + 375,3 punteada) | 0,00 % |
| 2.1.2 Demolición calzada (01_Dem Ext_Asfalto) | 1.939,8 m2 | 1.939,3 m2 | -0,03 % |
| 2.1.1 Demolición vereda (01_Dem Ext_Vereda HC) | 569,7 m2 | 569,9 m2 | +0,04 % |
| 2.2.2 Subrasante (calzada + vereda + reforzada + baldosa) | 21.786,1 m2 | 21.787,7 m2 | +0,01 % |
| 2.3.15 Vereda reforzada (CROSS) | 96,7 m2 | 96,7 m2 | 0,00 % |
| 2.4.18 HDPE DN300 | 385 ml (cuadro) | 384,5 ml (suma del cuadro de sumideros) y 388,9 ml (DWG) | -0,1 % / +1,0 % |
| 2.4.19 HDPE DN375 | 899 ml (cuadro) | 862,0 ml (37 rótulos de tramo) y 869,1 ml (45 polilíneas DWG) | -4,1 % / -3,3 % |

Coherencia de espesores: 2.3.2 = 4.349,7 x 0,05 = 217,5 m3 (cuadra). 2.3.6 = 17.300,2 x 0,15 = 2.595,0 m3 (cuadra aritméticamente, pero usa la base equivocada en accesos y en el corte 1-1, ver AUD-2026-11-10-2). Escarpe (2.2.1), excavación (2.2.3) y terraplenes (2.2.4) no tienen cantidad, así que no hay coherencia que verificar (AUD-2026-11-10-4).

Límite de independencia: uso las mismas capas y la misma herramienta que el autor. El acuerdo prueba que la aritmética es reproducible, no que la capa sea la correcta. Por eso las capas se contrastaron con las leyendas de las láminas 1, 7, 8 y 9 de pavimentación.

## 3. Hallazgos

### AUD-2026-11-10-1. Zanja de infiltración N° 8 omitida. Severidad ALTA
- Evidencia: lámina AALL 2/5 (planta, junto a la C.I. 37): 'ZANJA DE INFILTRACION N°8 ANCHO 2.05m (5 CAJAS) ALTO 3.60m (8 CAJAS) LARGO 12.6m (21 CAJAS)' y 'CAMARA DECANTADORA N°8 CA=685.03 H Total=1.92m'. En all.dxf: 8 polilíneas en la capa 00_S2_All ext_Zanja y 8 círculos en 3-PROY-ALL C Decantador (el autor dice 7). La memoria solo verifica las zanjas 1 a 7; ese es el origen del error.
- Impacto: el ítem 2.4.25 dice 0 y debe ser 1 (840 cajas, el 8,6 % de las 9.745 cajas del sistema, unos 93 m3 de módulos más la excavación); el ítem 2.4.1 dice 7 y debe ser 8. Orden de magnitud: CLP 17-30 millones (supuesto de CLP 20.000-35.000 por caja instalada con excavación, geotextil y relleno; se debe validar con costos de Reinoso). Si la oferta se adjudica con 0, ese costo lo asume Reinoso.
- Acción: 2.4.25 = 1 y 2.4.1 = 8. Reescribir la consulta 10: la zanja 8 existe en el plano, pero no tiene verificación en la memoria ni detalle propio (se asume el detalle 5x8 de las zanjas 2 y 7). Las láminas sí acotan el largo de cada zanja (7,80 / 13,8 / 11,4 / 17,4 / 21,6 / 19,8 / 25,8 / 12,6 m), así que la nota 'largo no explícito' de 2.4.10 a 2.4.16 es falsa y se corrige.
- Destino: T1b. Estado: abierto.

### AUD-2026-11-10-2. Base de 0,30 m sin cubicar y base de 0,15 m sobreestimada. Severidad ALTA
- Evidencia: lámina pav 8/10, 'Corte tipo acceso vehicular': el pavimento HCV G35 e=0,15 del acceso va sobre 'base granular e=0,30m'. En el 'Corte 1-1' (ubicado en y≈6.305.395, tramo sur hacia Av. Santa María), la calzada de 6,50 m va sobre base de 0,30 m. La memoria dice base de 15 cm para los accesos: la lámina y la memoria se contradicen.
- Impacto: los accesos (hatch color 150, 1.107,5 m2) llevan 166 m3 más de base. El corte 1-1, con un largo supuesto de 190 m (entre Santa María y el inicio de la curva), lleva otros 185 m3 aproximados (rango de 100 a 270 m3). Faltan en total cerca de 350 m3 de base, unos CLP 10-14 millones (supuesto de CLP 30.000-40.000 por m3). Hoy 2.3.6 cuenta esos m3 a 0,15 y 2.3.7 está vacío.
- Acción: separar la superficie de accesos en 2.3.7 (1.107,5 x 0,30 = 332,3 m3) y descontarla de 2.3.6. Medir el tramo del corte 1-1 en el DWG. Consultar a Demetra la contradicción entre memoria y lámina (consulta 5 reescrita con cifras).
- Destino: T1b y T1d. Estado: abierto.

### AUD-2026-11-10-3. Vereda reforzada con base de 0,10 sí existe. Severidad MEDIA
- Evidencia: lámina pav 9/10, 'Detalle tipo vereda HC reforzada': 'VEREDA H.C. PROYECTADA e=0.10m GRE=G25' sobre 'BASE ESTABILIZADA e=0.10m'.
- Impacto: 2.3.16 = 96,7 x 0,10 = 9,7 m3 (vacío). 2.3.15 (96,7 m2) tiene respaldo en el detalle, no es una estimación. La consulta 6 ('no hay base de 0,10 m') es falsa y quedaría mal ante Demetra.
- Acción: llenar 2.3.16 y eliminar la consulta 6.
- Destino: T1b y T1d. Estado: abierto.

### AUD-2026-11-10-4. 36 de 77 ítems sin cantidad. Severidad ALTA
- Evidencia: columna E vacía en 2.1.4-2.1.11, 2.1.13, 2.1.31, 2.2.1, 2.2.3, 2.2.4, 2.3.4, 2.3.7, 2.3.8, 2.3.11-2.3.14, 2.3.16-2.3.19, 2.3.22, 2.4.4, 2.4.20-2.4.22, 2.4.24, 2.4.30, 2.4.31, 2.4.33 y 2.5.1-2.5.3.
- Impacto: los más pesados son el movimiento de tierra y la reposición de soleras. La excavación hasta subrasante ronda 17.300 x 0,30 + 4.446 x 0,12, es decir unos 5.700 m3, sin contar el escarpe. Hay 1.017 ml de solera a retirar sin desglose entre 2.1.4 y 2.1.5. Faltan además los rellenos y excedentes de AALL y los 4 tipos de rodado (29 accesos y 31 rebajes).
- Acción: cerrar cada uno con criterio escrito o con consulta. Mientras quede uno vacío con precio, la oferta no se puede valorizar completa.
- Destino: T1c. Estado: abierto.

### AUD-2026-11-10-5. Dos 'incluido' falsos en encabezados. Severidad MEDIA
- Evidencia: K77 (encabezado 2.4 Aguas Lluvias) y K112 (encabezado 2.5 Otros) dicen '[INCLUIDO SEGÚN DEMETRA]', pero esas filas no tienen ninguna nota de Demetra.
- Impacto: si al valorizar se filtra por esa etiqueta, se dejan fuera secciones completas.
- Acción: borrar K77 y K112.
- Destino: T1b. Estado: abierto.

### AUD-2026-11-10-6. La columna G no tiene fórmulas de total por ítem. Severidad MEDIA
- Evidencia: G9:G115 están vacías tanto en el original como en la cubicación, así que los subtotales suman celdas vacías y hoy dan 0. E50 `=SUM(E45:E49)` suma m3 con m2 (viene así del original de Demetra).
- Acción: al valorizar, agregar `=E*F` por ítem sin mover filas. Avisar a Demetra lo de E50 en la consulta de ítems.
- Destino: T1e. Estado: abierto.

### AUD-2026-11-10-7. Largo del colector DN375 con tres cifras. Severidad MEDIA
- Evidencia: el cuadro de cañerías (AALL 2/5) dice 899 ml; la suma de los 37 rótulos de tramo 'COLECTOR N°x HDPE DN 375 L=' da 862,0 ml; mi medición del DWG da 869,1 ml (45 polilíneas). La cifra del autor, 903,7 ml en 44 polilíneas, no se reproduce.
- Impacto: 37 ml (4,1 %). Ofertar 899 es lo conservador para Reinoso.
- Acción: mantener 899, corregir 903,7 en la Fuente y fusionar las consultas 2 y 16.
- Destino: T1b y T1d. Estado: abierto.

### AUD-2026-11-10-8. Exclusión de 1.992 ml de solera fuera de la obra: correcta. Severidad BAJA
- Evidencia: de los 1.992,3 ml, 1.922 ml (96 %) coinciden con soleras de la obra al trasladarlos 1.000 o 1.100 m en Y; son copias del trazado para otras láminas. Los 70,7 ml restantes están en el mismo grupo copiado (y mayor a 6.306.950), lejos de la obra.
- Acción: dejar la exclusión y eliminar la consulta 21, porque pregunta por un artefacto del dibujo.
- Destino: T1d. Estado: abierto.

### AUD-2026-11-10-9. Exclusión del proyecto SERVIU 63023: correcta como criterio, pero incompleta. Severidad MEDIA
- Evidencia: las láminas pav 7 y 8 tienen la leyenda 'PROYECTO SERVIU CODIGO N°63023' en magenta (calzada HCV, vereda HC, solera tipo A, separación y demarcación de ciclovía), que coincide con el color 210 del DWG en Santa María y Agua del Palo. Al autor le falta el hatch SWAMP color 210 de 375,9 m2 en la capa Lot_ET1_ 8-DEM EXT DEMARCACION CICLOVIA (Agua del Palo), 10,6 ml de solera tipo C color 210 y 24,1 m2 de demolición dentro de la zona 63023.
- Impacto: si Demetra responde que 63023 sí es parte del alcance, faltan unos 570 m2 de HCV y vereda, 74 ml de solera y la ciclovía.
- Acción: completar la consulta 17 con estas cifras y declarar la exclusión en la oferta.
- Destino: T1d. Estado: abierto.

### AUD-2026-11-10-10. Banda de estacionamiento con e=0,17 metida en la calzada de 0,15. Severidad MEDIA
- Evidencia: corte 6-6 (lámina pav 8/10, ubicado en y≈6.305.920): banda de 3,00 m con 'PAVIMENTO H.C.V. GRE=G35 e=0.17m', más solera rebajada de plinto 0,05. El ítem 2.3.8 está vacío y el área está dentro de 2.3.5.
- Impacto: 3,00 m x largo de la banda, con 13 % más de hormigón que lo cubicado.
- Acción: medir el largo de la banda en el DWG y mantener la consulta 18.
- Destino: T1b. Estado: abierto.

### AUD-2026-11-10-11. Señalización y demarcación proyectadas sin ítem ni consulta. Severidad MEDIA
- Evidencia: pav.dxf, a 35 m o menos del eje, tiene 33 señales en la capa 00_Señal proy 01 (RO-13b, RO-06a, PO-14, entre otras), 91 bloques en 00_Demarc_Señal Proyectada y 6 bolardos de ciclovía (1-Dem-Proy-Bolardo Ciclovia).
- Impacto: alcance no definido. Si la partida lo incluye y no se consulta, el costo lo asume el oferente.
- Acción: consultar si la señalización y la demarcación son de otra partida; si no se responde, declararlas como exclusión.
- Destino: T1d. Estado: abierto.

### AUD-2026-11-10-12. Riesgos de las notas de la lámina 9/10 sin ítem. Severidad MEDIA
- Evidencia (notas de la lámina pav 9/10):
  - 'Será responsabilidad exclusiva del contratista... los costos derivados de modificaciones y traslado de redes de servicios públicos que no hayan sido integradas en el proyecto... así como la obtención de todas las autorizaciones, aprobaciones, inspecciones y recepciones'.
  - Si la subrasante no cumple CBR 12 %, se reemplaza el suelo por subbase.
  - Los cortes de vereda deben hacerse con cortadora mecánica.
- Impacto: ninguno de estos riesgos tiene ítem ni consulta, así que hoy los asume Reinoso.
- Acción: consultar y, en todo caso, declararlos como exclusión o con precio aparte en la oferta.
- Destino: T1d y T1e. Estado: abierto.

### AUD-2026-11-10-13. La subrasante mide solo la huella del pavimento. Severidad BAJA (latente)
- Evidencia: 2.2.2 = unión de los hatch. El perímetro de la calzada (4.309 ml) es casi igual al largo de solera, lo que indica que la huella no incluye la faja de solera ni el sobreancho de base. La nota de la lámina 9 exige escarificar 0,20 m.
- Impacto: de 650 a 1.290 m2 (entre 3 y 6 %) si se mide bajo las soleras.
- Acción: fijar el criterio en la consulta de movimiento de tierra.
- Destino: T1d. Estado: abierto.

### AUD-2026-11-10-14. Resaltos proyectados y canaleta sin cuantificar. Severidad BAJA
- Evidencia: la lámina pav 10/10 trae el 'Detalle resalto, lomo de toro plano con paso de cebra'. Demetra dice que 2.3.20 está incluido en 2.3.14 (rodado de vereda continua), y esa relación es dudosa. 2.3.22 está vacío y no hay número de resaltos.
- Acción: consultar el número de resaltos y el ítem que los paga.
- Destino: T1d. Estado: abierto.

### AUD-2026-11-10-15. La hoja 'Consultas Demetra' tiene errores, duplicados y vacíos. Severidad MEDIA
- Mal planteadas:
  - La 10 dice que el proyecto tiene 7 zanjas y que el largo no es explícito; ambas cosas son falsas.
  - La 6 dice que no hay base de 0,10.
  - La 3 no menciona la decantadora N° 8.
- Sobran: la 21 (copias del dibujo) y la 12 (los nombres S-1 y S-4 son genéricos del itemizado y no cambian el precio).
- Duplicadas: la 2 con la 16 (largos del colector) y parte de la 4.
- Faltan:
  - espesor de escarpe y criterio de movimiento de tierra (la observación de 2.2.1 dice 'ver consultas', pero no hay ninguna sobre eso);
  - base de 0,30 en accesos (lámina contra memoria);
  - mortero de pega y cama de soleras (2.3.4 y 2.3.17);
  - barras de traspaso y esquinas agudas (2.3.18 y 2.3.19);
  - señalización y demarcación;
  - notas de la lámina 9 (redes, recepciones, reemplazo de suelo);
  - número de resaltos;
  - conexión del sumidero 2 a una 'C.I. Existente';
  - ensayos, topografía, recepción SERVIU y planos as built.
- Además, ESTADO.md (T1d) dice 15 consultas y la hoja tiene 23.
- Acción: reescribir la hoja antes de enviarla a Demetra y revisarla con `revisar-textos` (la leerá un tercero).
- Destino: T1d. Estado: abierto.

### AUD-2026-11-10-16. Faltan todas las piezas de la oferta que pide Demetra. Severidad ALTA
- Evidencia: en `LoRecabarren/` solo están la cubicación y los antecedentes. Hay 0 de 6 piezas: APU por ítem, qué incluye y excluye, alcance técnico, plazo con rendimientos, condiciones comerciales y antecedentes de la empresa. La columna F (PU) está vacía. ESTADO.md registra como pendientes los costos de Reinoso y los datos de la empresa.
- Impacto: la oferta no se puede enviar.
- Acción: armar los APU cuando lleguen los costos, junto con una hoja de inclusiones y exclusiones que recoja AUD-2026-11-10-9, -11 y -12, el plazo con programa y rendimientos, y las condiciones comerciales (validez, forma de pago, retenciones, reajuste).
- Destino: T1e. Estado: abierto (backlog, depende de las preguntas a Eugenio).

### AUD-2026-11-10-17. Inconsistencias menores en aguas lluvias. Severidad BAJA
- Evidencia:
  - Las zanjas 7 y 8 están dibujadas con 1,64 m de ancho, pero su rótulo dice 2,05 m (5 cajas).
  - El colector 14 tiene 2,4 m3 de excavación de 2 a 4 m. Con la nota de Demetra en 2.4.27 ('para drenes'), esa excavación queda sin ítem.
  - Hay 8 bloques s3 en el DWG contra 4 S-3 en el cuadro (consulta 22, correcta).
  - Recuentos verificados contra los cuadros de la lámina 2/5: cámaras 1 a + 11 b + 25 especiales = 37; sumideros 38 S-2 + 4 S-3 + 8 baterías (16) = 58; tapas 37, escalines 59 y satélites 37 (sin ítem propio, se asumen dentro del precio de la cámara).
- Acción: agregar estas inconsistencias a la consulta 10 o 22.
- Destino: T1d. Estado: abierto.

### AUD-2026-11-10-18. Demolición fuera del pavimento nuevo. Severidad BAJA
- Evidencia: 644,6 m2 de demolición (calzada más vereda) quedan fuera de la huella nueva. 24,1 m2 caen en la zona 63023 y el resto en el bandejón y las franjas del tramo sur (y entre 6.305.350 y 6.305.560).
- Impacto: después de demoler esas superficies hay que rellenarlas, y ese relleno no tiene ítem. Es probable que sea paisajismo.
- Acción: agregarlo a la consulta 7 (bandejón y franjas).
- Destino: T1d. Estado: abierto.

## Lo que no se revisó

- Los volúmenes de excavación de los perfiles AALL (2.4.26 = 1.226,6 m3): las láminas 3 y 4 de AALL son vectoriales, sin texto extraíble, y no se releyeron a mano.
- Los conteos de elementos a trasladar y retirar (luminarias, separadores, pilares, señales) se aceptaron por coincidir bloques con rótulos; no se recorrieron en las láminas 1 y 2.
- No se revisaron EETT porque no existen en la carpeta, ni las bases de licitación de Demetra porque no están en la carpeta.
- Los montos en pesos son órdenes de magnitud con precios supuestos y se deben recalcular con los costos de Reinoso.

## Estado de la corrección (10-11-2026)

Corregido en `Cubicacion LoRecabarren.xlsx`: 46 de 77 ítems con cantidad, 31 A VERIFICAR, 21 consultas.

| AUD | Estado | Cifra nueva o destino |
|---|---|---|
| 1 | corregido | 2.4.25 = 1 (zanja N°8: 2,05 x 3,60 x 12,6 m, 840 cajas); 2.4.1 = 8 decantadoras; largos de zanjas 1 a 8 en la Observación; consulta 10 reescrita |
| 2 | corregido y consulta | 2.3.7 = 332,3 m3 (accesos 1.107,5 m2 x 0,30); 2.3.6 = 2.428,9 m3 (sin accesos). Tramo del corte 1-1 no ubicable en planos: consulta 5 |
| 3 | corregido | 2.3.16 = 9,7 m3; 2.3.15 = 96,7 m2 respaldado por detalle; consulta 6 reemplazada |
| 4 | consulta | De 36 a 31 ítems A VERIFICAR: llenados 2.1.4 (983,4 ml), 2.1.5 (5,2 ml), 2.2.3 (5.723,7 m3), 2.3.7, 2.3.16, 2.4.25; el resto con consulta |
| 5 | corregido | Rótulos de K77 y K112 eliminados |
| 6 | pendiente | Fórmulas `=E*F` se agregan al valorizar (T1e); E50 incluido en consulta 4 |
| 7 | corregido | Se mantiene 899 ml; fuentes: DWG all 869,1 ml (45 polilíneas), rótulos 862,0, perfiles 863,2; consultas 2 y 16 fusionadas (error: se había medido en el DWG pav, que es una versión anterior, con 903,7) |
| 8 | corregido | Exclusión mantenida; consulta 21 eliminada |
| 9 | corregido | Consulta 8 con ciclovía 375,9 m2, solera 63,8 m + 10,6 m tipo C, demolición 24,1 m2; la exclusión se declara en la oferta (T1e) |
| 10 | consulta | Banda sin capa ni rótulo ubicable en el DWG; no medible. Consulta 14 |
| 11 | consulta | Consulta 17 (33 señales, 91 demarcaciones, 6 bolardos) |
| 12 | consulta | Consulta 18 (redes, autorizaciones, CBR, cortadora) |
| 13 | consulta | Criterio de subrasante en consulta 16 (650-1.290 m2 más); 2.2.2 sigue en 21.786,1 m2 |
| 14 | consulta | Consulta 19 (número de resaltos y ítem que los paga) |
| 15 | corregido | Hoja reescrita con 21 consultas: 6, 10 corregidas; 12 y 21 eliminadas; 2 y 16 fusionadas; agregadas base de accesos, mortero y pasadores, señalización, notas lám 9, resaltos, movimiento de tierra y ensayos. Falta pasarla por `revisar-textos` antes de enviar |
| 16 | pendiente | Depende de costos de Reinoso, datos de la empresa y plazo (T1e) |
| 17 | corregido | Incluido en consultas 10 y 15 |
| 18 | corregido | 644,6 m2 de demolición fuera de huella en consulta 7 |

Resumen: 10 corregidos, 6 por consulta, 2 pendientes (AUD 6 y 16).

## Re-auditoría (10-11-2026)

Auditor independiente. No usé los scripts ni las mediciones del autor ni de la primera auditoría: extraje de nuevo `antecedentes/dxf/all.dxf` y `pav.dxf` (ezdxf 1.4.5 y shapely, en el venv existente del scratchpad), leí los cuadros de la lámina AALL 2/5 y los detalles de las láminas pav 5, 8 y 9 en imágenes a 300 dpi, y revisé el xlsx sin modificarlo. Los cuadros de la lámina AALL 2/5 son objetos OLE dentro del DWG, así que su fuente es el PDF y no el DXF.

### Veredicto

**Apta solo en parte.** Se pueden valorizar las cantidades de aguas lluvias y las superficies de pavimento y demolición. No se puede valorizar 2.2.3 (5.723,7 m3), porque el perfil longitudinal muestra que la rasante no sigue al terreno. Las bases 2.3.6 y 2.3.7 quedan sujetas a la consulta 5, cuyo tramo sí se puede medir. De los 10 AUD marcados 'corregido', confirmo 8 y rechazo 2 (AUD-2 en parte y AUD-15). Hallazgos nuevos: 1 alto, 4 medios y 4 bajos.

### 1. AUD marcados 'corregido'

| AUD | Veredicto | Evidencia propia |
|---|---|---|
| 1 | Confirmado | all.dxf tiene 8 rótulos MULTILEADER 'ZANJA DE INFILTRACION N°1..8', 8 polilíneas en 00_S2_All ext_Zanja y 8 círculos en 3-PROY-ALL C Decantador. La suma de cajas da 9.745 y la zanja 8 tiene 5x8x21 = 840. 2.4.25 = 1 y 2.4.1 = 8 están bien. Los largos de las zanjas 1 a 8 coinciden con los rótulos y con las polilíneas (7,83 / 13,8 / 11,4 / 17,41 / 21,6 / 19,8 / 25,8 / 12,6 m). |
| 2 | Rechazado en parte | Los accesos están bien: el hatch color 150 mide 1.107,6 m2, así que 2.3.7 = 332,3 m3 y 2.3.6 = 2.428,9 m3 cuadran, y el corte tipo acceso de la lámina 8/10 dice 'BASE GRANULAR e=0.30m'. Pero el corte 1-1 sí se puede ubicar (ver R2), así que la cifra no está cerrada. |
| 3 | Confirmado | La lámina 9/10, 'Detalle tipo vereda HC reforzada', dice 'e=0.10m' sobre 'BASE ESTABILIZADA e=0.10m'. 96,7 x 0,10 = 9,7 m3. |
| 5 | Confirmado | K77 y K112 están vacías. |
| 7 | Confirmado | En all.dxf, la capa 00_All ext_Colector tiene 45 polilíneas y 869,1 m. Los 37 rótulos de tramo suman 862,0 m y los 15 perfiles 863,2 m. El cuadro de cañerías dice 899 m. Mantener 899 es lo conservador. |
| 8 | Confirmado | La consulta 21 actual trata de los árboles; la de copias del dibujo ya no está. |
| 9 | Confirmado | Valores propios: HCV 210 = 193,8 m2, vereda 210 = 38,0 m2 (unión), baldosa 210 = 8,3 m2, solera 210 = 63,8 ml, solera C 210 = 10,6 ml y ciclovía = 375,8 m2. Coinciden con la consulta 8. |
| 15 | Rechazado | La hoja se reescribió, pero tiene tres consultas mal planteadas y le faltan otras (R3 y R4). |
| 17 | Confirmado | Las zanjas 7 y 8 están dibujadas con 1,64 y 1,65 m de ancho, contra 2,05 m del rótulo. El colector 14 tiene 2,4 m3 entre 2 y 4 m. Hay 46 bloques SUMIDEROS2, 8 s3 y 4 de otro tipo. Todo está en las consultas 10 y 15. |
| 18 | Confirmado | Está en la consulta 7. |

### 2. Aguas lluvias, medido de nuevo en all.dxf y en las láminas AALL

| Cantidad | xlsx | Medición propia | Resultado |
|---|---|---|---|
| Cámaras a / b / especiales (2.4.2, 2.4.3, 2.4.17) | 1 / 11 / 25 | Conteo de las 37 filas del cuadro de cámaras de la lámina 2/5: 1 / 11 / 25. Hay 37 bloques CAMARA en 00_All ext_Camara y la suma de escalines da 59. | Coincide |
| Decantadoras (2.4.1) | 8 | 8 círculos y 8 rótulos (H total de 1,92 a 3,48 m) | Coincide |
| Sumideros S-2 / S-3 / baterías (2.4.6, 2.4.7, 2.4.29) | 38 / 4 / 8 | Conteo del cuadro de sumideros: 38 / 4 / 8 (16 sumideros). En el DXF hay 58 bloques. | Coincide |
| Rejillas S-2 / S-3 (2.4.8, 2.4.9) | 38 / 4 | Una por sumidero | Coincide |
| Zanjas 1 a 8 (2.4.10 a 2.4.16 y 2.4.25) | 1 cada una | 8 zanjas | Coincide |
| HDPE DN300 (2.4.18) | 385 | La suma de las 50 filas del cuadro da 384,50; los 49 rótulos 'DESCARGA SUM' dan 384,0 y las 50 polilíneas DASHED de 00_All ext_Descarga sum, 388,9 m | Coincide (+1,0 % en el DWG) |
| HDPE DN375 (2.4.19) | 899 | Cuadro 899; perfiles 863,2; DWG 869,1 | Se acepta 899 (consulta 2) |
| Excavación de 0 a 2 m (2.4.26) | 1.226,6 | Suma de la fila 'VOLUMEN DE EXCAVACION 0-2' de los 15 perfiles: 1.226,6 m3; de 2 a 4 m, 2,4 m3; de 4 a 6 m, 0 | Coincide. El punto que la primera auditoría dejó sin revisar ya está verificado. |

En aguas lluvias no quedan cifras que dependan de pav.dxf. Las fuentes del xlsx citan el DWG all o las láminas AALL, y las cifras coinciden con all.dxf.

### 3. Hallazgos nuevos

#### AUD-2026-11-10-R1. Movimiento de tierra 2.2.3 subestimado: la rasante no es igual al terreno. Severidad ALTA
- Evidencia: perfil longitudinal de las láminas pav 5 y 6 (Km 0+000 a 1+140,58). Leí en pav.dxf (capa TEXTOS-PERFILES) las filas 'ELEVACION TERRENO' y 'ELEVACION RASANTE' y las contrasté a ojo con la lámina 5. La diferencia entre rasante y terreno va de -1,31 m (Km 0+600, corte) a +0,41 m (Km 0+400, relleno): Km 0+100 -0,77; 0+300 +0,21; 0+600 -1,31; 0+700 +0,31; 0+900 -0,37; 1+100 -0,44. Integrado cada 1 m con interpolación lineal, da 247,7 m2 de perfil en corte y 152,3 m2 en relleno.
- Impacto: con un ancho de faja de 15 a 19 m (21.786 m2 de subrasante sobre 1.140 m de eje), faltan entre 3.700 y 4.700 m3 de corte, además de los 5.723,7 m3 (+65 a +82 %), y hay entre 2.300 y 2.900 m3 de terraplén sin cantidad (2.2.4 está vacío). Al mismo 2.2.3 le faltan otros 166,1 m3 de los accesos (base de 0,30 m, que el autor anotó pero no sumó) y 7,7 m3 de la vereda reforzada (0,20 m de estructura y no 0,12). Es una estimación gruesa: el terreno está cada 100 m y no hay perfiles transversales, y en la lámina 5 se ven lomas entre estaciones (Km 0+560 a 0+620) que la elevan.
- Acción: no ofertar 5.723,7 m3. Cubicar corte y terraplén con el perfil longitudinal (estaciones de la lámina) por el ancho de cada sección tipo, o pedir los perfiles transversales. Reescribir la consulta 16 sin el supuesto 'rasante igual al terreno', porque el plano lo contradice.
- Destino: T1c. Estado: abierto.

#### AUD-2026-11-10-R2. El tramo del corte 1-1 sí se puede medir. Severidad MEDIA
- Evidencia: en pav.dxf, la capa 03_Pav ext_Linea de Corte ubica el corte 1-1 en y = 6.305.392. Corté el hatch de calzada (03_Pav ext_HCV, color 256) cada 10 m. La sección del corte 1-1 (calzadas de 7,52 y 6,52 m) se mantiene entre y ≈ 6.305.380 y 6.305.535, unos 155 m, hasta el cruce en el que las calzadas se invierten (6,52 y 7,52 m desde y = 6.305.560).
- Impacto: si rige la base de 0,30 m de la lámina, faltan 6,52 x 155 x 0,15 = 152 m3 de base en 2.3.7, sobran los mismos m3 en 2.3.6 y faltan otros 152 m3 de excavación. Una salvedad: en el corte, la base de 0,30 está dibujada con el mismo espesor que la de 0,15, así que el rótulo podría ser un error del proyectista.
- Acción: en la consulta 5, quitar 'no ubicable' y dar la cifra (tramo de unos 155 m entre el corte 1-1 y el cruce, 152 m3).
- Destino: T1d. Estado: abierto.

#### AUD-2026-11-10-R3. La cama de soleras sí está acotada y el hormigón de respaldo no tiene ítem. Severidad MEDIA
- Evidencia: lámina pav 9/10, 'Colocación de soleras tipo A' (plinto 0,15 y 0,00). La solera va sobre 'BASE CBR≥60%' de 0,10 + 0,16 + 0,08 = 0,34 m de ancho; el espesor está acotado en 0,15, aunque el dibujo mide unos 0,10. Además lleva respaldo de 'HORMIGON DE 170 Kg. cem./m3 H-10'.
- Impacto: 2.3.17 = 4.305,6 x 0,34 x 0,15 = 219,6 m3 (146,4 m3 con 0,10). Hoy está vacío y la Observación dice 'el detalle no entrega espesor de cama', lo que es falso. El respaldo H-10 suma unos 0,05 m3/ml, es decir, del orden de 200 m3 sin ítem, salvo que vaya dentro del precio de la solera.
- Acción: llenar 2.3.17 con 219,6 m3 y explicar el criterio. Reescribir la consulta 6 para preguntar solo si el respaldo H-10 va dentro de 2.3.3, y no 'el espesor de cama'.
- Destino: T1b y T1d. Estado: abierto.

#### AUD-2026-11-10-R4. Ítems 'A VERIFICAR' y riesgos sin consulta. Severidad MEDIA
- Evidencia: recorrí los 31 ítems 'A VERIFICAR' contra las 21 consultas, por código y por tema. Cuatro no tienen consulta:
  - 2.4.30, rejillas de batería (8 o 16);
  - 2.4.31, conexiones DN375 (no hay criterio);
  - 2.5.1, cámaras a nivelar (al menos 10 rótulos, uno de ellos en plural);
  - 2.5.3, entibaciones.
- Hay además dos riesgos del oferente que tampoco tienen consulta:
  - 2.1.3, resaltos a demoler (2 rótulos contra 3 hatch);
  - profundidad de las obras de infiltración. Los módulos de las zanjas tienen 3,60 a 4,05 m de alto y las decantadoras llegan a 3,48 m de altura total, así que la excavación pasa de 4 m. Eso hace probable la entibación, y el ítem 2.5.3 se mide por mes.
- Acción: agregar estas consultas, o declarar en la oferta el criterio que se asume.
- Destino: T1d. Estado: abierto.

#### AUD-2026-11-10-R5. Riesgo de doble conteo entre accesos y dispositivos de rodado. Severidad MEDIA
- Evidencia: 2.3.5 incluye los 29 accesos HCV (1.107,5 m2), 2.3.7 cubica su base (332,3 m3) y 2.3.11 a 2.3.14 cobran los dispositivos de rodado por unidad (29 accesos y 31 rebajes). Demetra dice además que los resaltos (2.3.20) van 'incluidos en 2.3.14'.
- Impacto: si el precio unitario del rodado incluye su pavimento, como es habitual en los ítems SERVIU, los 1.107,5 m2 y los 332,3 m3 se cobrarían dos veces, o se descontarían dos veces si Demetra lo entiende al revés.
- Acción: definir en los APU qué incluye la unidad de rodado y preguntarlo dentro de la consulta 15.
- Destino: T1d y T1e. Estado: abierto.

#### AUD-2026-11-10-R6. E50 ahora da un número. Severidad BAJA
- Evidencia: `=SUM(E45:E49)` vale 27.509,8 (21.786,1 m2 + 5.723,7 m3). En el original daba 0 porque las celdas estaban vacías. Otros puntos que vienen del original: las filas 28, 29, 30 y 41 tienen descripción y cantidad o nota, pero no código de ítem; 2.4.33 y 2.5.2 no tienen unidad; 2.3.9 (fila 62) no tiene descripción. Las fórmulas G43, G51, G76, G111, G117 y G118 están intactas, y la comparación con el original da 0 celdas originales alteradas (298 diferencias, todas de vacío a valor).
- Acción: no usar E50. Al valorizar, dar precio a las filas sin código.
- Destino: T1e. Estado: abierto.

#### AUD-2026-11-10-R7. Solera a retirar: tramos dibujados dos veces y 28,4 ml sin ítem. Severidad BAJA
- Evidencia: la capa 01_Dem Ext_Solera tipo A de pav.dxf tiene 52 polilíneas y 1.017,1 m, igual que el autor. Pero 16,7 m de esas polilíneas quedan a 0,15 m o menos de otra polilínea de la misma capa, y lo más probable es que estén dibujados dos veces. 983,4 + 5,2 + 28,4 = 1.017,0 cuadra. Los 577,6 ml que se asumen Manquehue no tienen rótulo.
- Impacto: hasta 16,7 ml de más en 2.1.4. Los 28,4 ml de tipo A quedan sin ítem (consulta 13).
- Acción: revisar en el DWG si esos 16,7 m están dibujados dos veces.
- Destino: T1b. Estado: abierto.

#### AUD-2026-11-10-R8. all.dxf y pav.dxf no son la misma versión del pavimento. Severidad BAJA
- Evidencia: las capas de pavimento dentro de all.dxf dan un HCV color 256 de 16.175,9 m2 y 32 rebajes. pav.dxf da 16.196,5 m2 y 31 rebajes, una diferencia de 20,6 m2 (0,1 %). El resto de los hatch (vereda, accesos, baldosa, 63023) es igual en los dos archivos.
- Acción: dejar escrito en la Fuente que el pavimento se mide en pav.dxf y que aguas lluvias se mide en all.dxf.
- Destino: T1b. Estado: abierto.

#### AUD-2026-11-10-R9. Notas de la lámina 9 que no recoge la consulta 18. Severidad BAJA
- Evidencia: la lámina 9 dice que, si el CBR real difiere del de diseño, 'deberá rediseñar la estructura de pavimento', y que la intersección entre acceso y vereda debe tener una 'superficie antideslizante' prolongada 1,00 m a cada lado. Ninguna de las dos cosas tiene ítem.
- Acción: agregar ambas notas a la consulta 18 o a las exclusiones.
- Destino: T1d. Estado: abierto.

### 4. Hoja 'Consultas Demetra'

Cubre 27 de los 31 ítems 'A VERIFICAR'; faltan 2.4.30, 2.4.31, 2.5.1 y 2.5.3 (R4). Tres consultas preguntan algo que el plano ya responde:
- la 5 dice que el corte 1-1 'no es ubicable' (R2);
- la 6 pide el espesor de la cama (R3);
- la 16 supone que la rasante es igual al terreno (R1).

Además, la 13 mezcla las casas con las soleras. La hoja tampoco pasó por `revisar-textos`.

### Lo que no se revisó en esta re-auditoría

- No conté a mano en las láminas 1 y 2 los retiros puntuales (luminarias, pilares, separadores, señales).
- La estimación de corte y terraplén de R1 es de orden de magnitud: usé el terreno cada 100 m del perfil longitudinal y no hay perfiles transversales.
- No revisé las piezas comerciales de la oferta (AUD-16) ni los APU.

## Estado de la corrección de la re-auditoría (10-11-2026)

xlsx: 48 de 77 ítems con cantidad (29 cubicados, 19 estimados), 29 A VERIFICAR, 26 consultas.

| Id | Estado | Cifra nueva o destino |
|---|---|---|
| AUD-2 | corregido | 2.3.7 = 151,6 m3 (corte 1-1: 6,52 m x 155 m x 0,15 adicional); los accesos (332,3 m3) pasan a rodados; 2.3.6 = 2.277,3 m3 |
| AUD-15 | corregido | Consultas 5, 6, 13, 15, 16 y 18 reescritas; 13 separada de las casas (nueva 25); 26 consultas en total |
| R1 | corregido (estimado) y consulta | 2.2.3 = 10.271 m3 (5.723,7 + 166,1 + 7,7 + 152,1 + corte 4.221; rango 9.800-10.800); 2.2.4 = 2.591 m3 (rango 2.286-2.896); consulta 16 pide perfiles transversales |
| R2 | corregido | 151,6 m3 en 2.3.7 y menos 151,6 en 2.3.6; consulta 5 con tramo y cifra |
| R3 | corregido y consulta | 2.3.17 = 219,6 m3 (146,4 con 0,10 m); hormigón de respaldo H-10 (~215 m3) en consulta 6 |
| R4 | corregido | Consultas 22 (2.4.30 y 2.4.31), 23 (2.5.1), 24 (2.5.3 y profundidad de infiltración) y 26 (resaltos a demoler) |
| R5 | corregido | 2.3.5 = 16.192,7 m2 (sin 1.107,5 m2 de accesos); los accesos y su base de 332,3 m3 van en los rodados; consulta 15 |
| R6 | corregido | E50 vaciada y anotada en K50 |
| R7 | corregido | 2.1.4 = 966,7 ml (menos 16,7 ml dibujados dos veces; por el método propio salen 21,7 ml) |
| R8 | corregido | Fuente aclara pav.dxf (pavimento) y all.dxf (aguas lluvias) |
| R9 | corregido | Rediseño por CBR y superficie antideslizante agregados a la consulta 18 |

Resumen: 9 R corregidos, 0 pendientes. R1 sigue como estimación gruesa hasta tener perfiles transversales.
