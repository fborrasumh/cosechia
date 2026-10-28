# CosechIA

Del semillero a la cosecha: sistemas de producción de cultivos de ciclo corto. Aplicación web de un solo fichero.

**Usar la app:** https://fborrasumh.github.io/cosechia/

**Método de cálculo:** FAO-56 (Allen et al., 1998) para Ra, Kc y lámina de riego; Hargreaves para la ETo; USDA-SCS para la lluvia efectiva; balance de nutrientes para la fertilización.

**Idiomas:** español (por defecto), inglés, portugués; selector en la barra superior (o `?lang=en` / `?lang=pt` en la URL).

## Qué hace

Acompaña la asignatura **Sistemas de Producción de Cultivos de Ciclo Corto** (ASPUPPP25) en seis pasos y tres secciones:

1. **Atlas de 17 cultivos** de las tres unidades del sílabo (hortalizas; raíces y tubérculos; cereales andinos): taxonomía, morfología, órgano cosechado, requisitos de temperatura, altitud y pH, curva de Kc, indicadores de cosecha y extracción de nutrientes, con su aptitud y su ciclo en la finca del usuario.
2. **Diagnóstico agrometeorológico de la finca (UPA):** temperatura y lluvia mensuales (con tres perfiles ilustrativos o datos propios), ETo de Hargreaves con la radiación extraterrestre de FAO-56 según la latitud, lluvia efectiva (USDA-SCS), climograma con los meses secos y ranking de aptitud de los 17 cultivos.
3. **Plan de cultivo:** densidad, semilla o tubérculo-semilla, plántulas y bandejas de semillero; fenología por grados-día con la temperatura de cada mes (diagrama de Gantt y fecha de cosecha); riego con balance diario de agua en la zona de raíces (Kc por etapa FAO-56, lámina neta y bruta, número de riegos, volumen y tiempo de goteo); fertilización por balance de nutrientes, orgánica (gallinaza, bocashi, compost, humus, estiércol) o mineral (fosfato diamónico, urea, cloruro de potasio).
4. **Matriz de costos de producción** generada desde el plan y editable: costos directos, mano de obra e indirectos, costo unitario, ingreso, utilidad, relación beneficio/costo y punto de equilibrio con gráficos.
5. **Retos con solución calculada:** ocho tipos de problemas (densidad, semilla, grados-día, gradiente térmico, dosis de N, abono para la parcela, intervalo de riego y beneficio/costo) con datos propios para cada alias, corrección con margen del 2 % y diagnóstico del error típico cometido. El profesorado imprime hojas individuales y descarga el solucionario en CSV; el mismo alias y la misma serie dan siempre los mismos datos.
6. **Bitácora, informe técnico y tríptico:** registro fenológico y de labores culturales, informe técnico en Word con la estructura del sílabo (generado en el navegador, sin red) y tríptico de dos caras para imprimir o guardar en PDF. Proyecto exportable e importable en JSON.

Secciones: **evaluación diagnóstica** (18 preguntas con explicación, seis por unidad), **sílabo y prácticas** con la bibliografía y **glosario**.

Hay un ejemplo completo (finca ilustrativa, papa, bitácora de un grupo y una revisión de IA precalculada) que funciona sin clave ni conexión.

## Cómo se usa la IA

La IA es **opcional** y no calcula nada: todas las cifras salen de código determinista. Solo interviene en la **revisión formativa del informe**, con la propia clave de OpenAI, Google Gemini o Anthropic Claude (guardada solo en el navegador; no hace falta servidor). La IA devuelve comentarios sin notas; cada comentario debe citar literalmente el texto del estudiante y el código comprueba la cita (las no encontradas se marcan con ⚠), avisa de las cifras que no están en el texto ni en los datos calculados y marca los comentarios que contienen notas o porcentajes.

## Privacidad

Finca, plan, costos, bitácora, respuestas y clave se guardan solo en el navegador (IndexedDB y localStorage). Solo si se pide la revisión formativa salen hacia el proveedor de IA los textos del estudiante y un resumen de los datos calculados, con correos, documentos de identidad, teléfonos y el alias del autor enmascarados; antes del primer envío se muestra exactamente lo que sale y se pide confirmación. Los retos piden un alias, no el nombre ni la cédula.

## Límites

- Los datos de los cultivos (temperaturas, franjas de altitud, grados-día, Kc, distancias, extracciones, rendimientos), los perfiles de finca y los precios son **valores orientativos redondeados para la docencia**, no recomendaciones técnicas: deben sustituirse por los de la estación meteorológica, el análisis de suelo, la variedad y el mercado locales.
- El modelo de grados-día es lineal y usa la temperatura media mensual; la ETo de Hargreaves es una aproximación cuando no hay radiación ni viento medidos; la temperatura estimada por altitud solo sirve como primer valor.
- La aptitud (0-100) combina temperatura, altitud y pH; no considera heladas, plagas, variedad ni mercado.
- La revisión de la IA es orientativa, puede equivocarse y no sustituye la corrección del profesor. La verificación de citas confirma que el fragmento existe en el texto, no que el comentario sea acertado.
- Se probó con IA simulada de los tres proveedores (incluidas citas inventadas, cifras nuevas y notas), en escritorio y móvil y en los tres idiomas; no se probó con claves reales.

## Autoría

Fernando Borrás Rocher (Universidad Miguel Hernández de Elche) y Segundo Ramiro Mora Quilismal (Universidad Politécnica Estatal del Carchi).

A partir del sílabo de Sistemas de Producción de Cultivos de Ciclo Corto (ASPUPPP25, nivel IV, Carrera de Agropecuaria, UPEC) del profesor Segundo Ramiro Mora Quilismal: sus tres unidades (hortalizas; raíces y tubérculos; cereales), las prácticas en el Centro Experimental San Francisco, el informe técnico y el tríptico del cultivo.

ORCID: Fernando Borrás Rocher [0000-0002-5519-4573](https://orcid.org/0000-0002-5519-4573) · Segundo Ramiro Mora Quilismal [0000-0003-0487-4883](https://orcid.org/0000-0003-0487-4883)

## Cómo citar

Borrás Rocher, F. y Mora Quilismal, S. R. (2026). *CosechIA* (v1.0.0) [Software]. (DOI en trámite)

## Licencia

MIT. Véase [LICENSE](LICENSE).
