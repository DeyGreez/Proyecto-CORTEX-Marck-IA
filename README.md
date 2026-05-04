# Proyecto-CORTEX-Marck-AI
# Mision: Asistente AI diseñado para la ayuda de medico optométricos 
# Integrantes: Juan David Leal Carmona, Erick Fabian Cardenas Bello
# 1.Perfil del Agente
<img width="1238" height="777" alt="Captura de pantalla 2026-02-19 105853" src="https://github.com/user-attachments/assets/3a1c5006-5e7f-425c-99cd-aa173eb01626" />

# 2.Grafico de Radar del Agente

<img width="1575" height="806" alt="Captura de pantalla 2026-02-26 102949" src="https://github.com/user-attachments/assets/88da2547-6d66-40b3-811e-93056ca8a101" />

# Argumentaciòn del porque de estos Valores:

Atención = 10
Porque en medicina no se puede distraer. O sea, un pequeño error en una graduación o en un dato del paciente puede afectar el tratamiento. Entonces el sistema tiene que fijarse en todo, hasta en los detalles pequeños. No puede estar “medio atento”, tiene que estar full concentrado.

Memoria = 10
También necesita recordar el historial del paciente, las consultas pasadas, si tiene diabetes, si toma medicamentos, cosas así. Si no recuerda eso, podría dar una recomendación mal. Entonces la memoria tiene que estar al máximo porque la consulta no es solo lo que pasa en ese momento, sino todo lo que viene de antes.

Lenguaje = 10
Esto es importante porque el asistente tiene que explicar cosas técnicas de forma clara. No todos los pacientes entienden términos médicos. Además, tiene que ayudar a redactar informes bien hechos. Si se comunica mal, puede haber confusiones, y en salud eso es grave.

Emoción = 2
Aquí es donde cambia la cosa. No queremos que la IA tome decisiones por emoción. No debería “sentir lástima” o exagerar algo porque suena grave. Tiene que ser objetiva. Pero tampoco cero emoción total, porque si responde súper fría puede parecer rara. Entonces un nivel bajo está bien: un poco humano, pero sin que afecte las decisiones.

En resumen, el agente está pensado para ser súper fuerte en lo técnico (atención, memoria y lenguaje), pero mantener la emoción controlada para que no interfiera. O sea, que piense como profesional, no como alguien que se deja llevar por lo que siente.


# Inputs Brainstrom 

<img width="1919" height="881" alt="Captura de pantalla 2026-03-12 104457" src="https://github.com/user-attachments/assets/28169808-3693-4b0a-b148-7bc76b88be57" />

# El Flujo Del Procesamiento 

Procesamiento
Arriba-Abajo (TopDown) y Patrones

![image](https://github.com/user-attachments/assets/fb3b0ad1-802d-4949-bf88-ac8d16b323d7)

Miro:


<img width="1020" height="865" alt="Captura de pantalla 2026-03-19 100023" src="https://github.com/user-attachments/assets/26ee89a2-dfd1-4399-ae0b-449d097350a2" />

# El Filtro de Atenciòn

Atenciòn selectiva y Carga Cognitiva

![ollEG](https://github.com/user-attachments/assets/acffaa02-67b9-4d5c-b9f8-e71a948a318c)

Miro:

<img width="1014" height="853" alt="Captura de pantalla 2026-03-19 100733" src="https://github.com/user-attachments/assets/65632649-5872-4aef-9f65-2867c1560a23" />

# El Disco Duro

Memoria a Largo Plazo (LTM): Semántica y Episódica.


![BaHL0](https://github.com/user-attachments/assets/e34a2578-4085-4d90-8591-89b653a0a6b8)

| Carpeta / Categoría                  | Tipo de Memoria     | Descripción                                                                 | Ejemplos para Mark-AI (Optometría)                              |
|--------------------------------------|---------------------|-----------------------------------------------------------------------------|-----------------------------------------------------------------|
| Anatomía y Fisiología Ocular         | Semántica           | Conceptos básicos y hechos permanentes del ojo y sistema visual            | Estructura de retina, cristalino, nervio óptico, vías visuales |
| Fórmulas y Cálculos Optométricos     | Semántica           | Ecuaciones y constantes clínicas que nunca cambian                         | Fórmula de lensmaker, Snellen, equivalentes esféricos, dioptrías |
| Patologías y Diagnósticos            | Semántica           | Enfermedades, signos y criterios diagnósticos                              | Miopía, hipermetropía, astigmatismo, glaucoma, catarata        |
| Protocolos y Guías Clínicas          | Semántica           | Procedimientos estandarizados y mejores prácticas                          | Examen refractivo completo, normas de prescripción, ISO 9001   |
| Catálogo de Lentes y Productos       | Semántica           | Información técnica de materiales y tratamientos                           | Tipos de lentes (monofocales, progresivos, fotocromáticos)     |
| Leyes y Regulaciones                 | Semántica           | Normativa legal y ética en salud ocular                                    | Leyes colombianas de optometría, consentimiento informado      |
| Historial Clínico (anonimizado)      | Episódica           | Casos y evoluciones de pacientes (solo patrones y lecciones aprendidas)    | Seguimientos de graduación, respuestas a tratamientos          |
| Investigación y Avances              | Semántica           | Estudios científicos y evidencia actualizada                               | Últimos papers sobre IA en optometría, nuevas tecnologías      |

Miro:

<img width="1511" height="876" alt="Opera Instantánea_2026-03-26_103039_miro com" src="https://github.com/user-attachments/assets/37800a0e-7f5f-4554-8808-adf057dc030b" />


# La Ram Cognitiva

Memoria de Trabajo y Carga Cognitiva (El número mágico 7±2).

![36ykO](https://github.com/user-attachments/assets/cb5822c9-5412-429d-8879-803a8c1ef751)

| Componente                  | Descripción                                                                 | Límite Recomendado          | Razón (Carga Cognitiva)                                      |
|-----------------------------|-----------------------------------------------------------------------------|-----------------------------|-------------------------------------------------------------|
| Ventana de Contexto         | Memoria de Trabajo / RAM Cognitiva del bot                                  | 7 ± 2 mensajes / turnos     | Número mágico de Miller (evita sobrecarga cognitiva)        |
| Mensaje actual              | Consulta o mensaje más reciente del usuario                                 | Siempre incluido            | Prioridad máxima (Atención = 10)                            |
| Mensajes anteriores         | Historial inmediato de la conversación                                      | Hasta 6 mensajes previos    | Mantiene contexto clínico reciente sin saturar la RAM       |
| Mensajes descartados        | Mensajes que salen de la ventana                                            | A partir del mensaje -8     | Se archivan en Memoria a Largo Plazo (LTM)                  |
| Límite superior             | Máximo de tokens / mensajes retenidos                                       | 7 ± 2                       | Evita olvido del inicio de la consulta y sobrecarga         |
| Recuperación desde LTM      | Cuando se necesita información antigua                                      | Solo si es relevante        | Se activa mediante Memoria=10 (Top-Down)                    |

**Notas de la Ventana de Contexto:**
- El bot mantiene **solo los últimos 7 ± 2 mensajes** en Memoria de Trabajo.
- Superado el límite, los mensajes más antiguos se descartan automáticamente de la RAM.
- La información antigua sigue disponible mediante la Memoria a Largo Plazo (LTM).
- Esto equilibra precisión clínica, atención selectiva y eficiencia computacional.

Miro:

<img width="1524" height="867" alt="Opera Instantánea_2026-03-26_103414_miro com" src="https://github.com/user-attachments/assets/afd912d5-8a30-4528-b8ad-df3638396b73" />

# El Bilbliotecario

Procesos de recuperacion y olvido

| Paso | Fase del Flujo                          | Descripción                                                                 | Acción del Bot                                      | Componente Usado                  | Nota / Regla                          |
|------|-----------------------------------------|-----------------------------------------------------------------------------|-----------------------------------------------------|-----------------------------------|---------------------------------------|
| 1    | Entrada de Pregunta                     | Recibe la consulta del usuario (Fase 2)                                     | Aplica Gatekeeper (filtro de ruido)                | Atención Selectiva = 10           | Filtra todo lo no clínico             |
| 2    | Verificación en Contexto Inmediato      | Revisa si la información ya está disponible                                 | Busca dentro de la Ventana de Contexto             | RAM Cognitiva (7 ± 2 mensajes)    | Si está → Responder directamente      |
| 3    | Búsqueda en Memoria Permanente          | Si no está en RAM, consulta la base de conocimiento                        | Recupera datos relevantes usando patrón Top-Down   | LTM (Memoria a Largo Plazo)       | Memoria = 10 + Atención = 10          |
| 4    | Recuperación y Priorización             | Extrae solo la información útil y actual                                    | Prioriza entidades clínicas y contexto histórico   | Lenguaje = 10                     | Evita sobrecarga cognitiva            |
| 5    | Integración y Respuesta                 | Combina contexto reciente + conocimiento recuperado                         | Genera respuesta objetiva y precisa                | Procesamiento final               | Emoción = 2 (siempre objetivo)        |

**Regla de Olvido (Documentada en GitHub - README.md)**

- **Condición**: Si pasan **10 minutos de inactividad** en la conversación.
- **Acción**: Limpiar completamente la Ventana de Contexto (RAM Cognitiva).
- **Consecuencia**: Los mensajes antiguos salen de la RAM, pero permanecen seguros y accesibles en LTM.
- **Objetivo**: Evitar sobrecarga cognitiva, reducir consumo de tokens y garantizar privacidad de datos del paciente.

cuadro:

![image](https://github.com/user-attachments/assets/715b8177-2016-4d00-b812-4b516f329ba0)


miro:

<img width="1920" height="1032" alt="Captura de pantalla 2026-04-09 103944" src="https://github.com/user-attachments/assets/cb82fb0e-fd50-4be7-845d-049a321041dd" />


## Semana 13 - Árbol de Decisión (Decision Tree)

### Algoritmo Maestro de Razonamiento Deductivo - Mark-AI

**Nodo Raíz:**  
¿El usuario realiza una consulta relacionada con salud visual / optometría?

- **NO** → Responder educadamente y redirigir al tema optométrico o finalizar.
- **SÍ** → Continuar al siguiente nodo.

**Nivel 1 - Tipo de Consulta:**
- ¿La consulta requiere evaluación clínica / diagnóstico?  
  - **SÍ (Evaluación clínica)**  
    → ¿Tengo suficiente información del historial reciente y datos del paciente?  
      - **SÍ** → Aplicar reglas clínicas + cruzar con LTM → Generar respuesta preliminar + recomendaciones.  
      - **NO** → Preguntar datos faltantes (síntomas específicos, graduación anterior, enfermedades sistémicas, medicamentos, etc.).

  - **NO (Información general)**  
    → ¿La pregunta es sobre conceptos básicos, lentes/productos o protocolos?  
      - Conceptos básicos → Responder desde Memoria Semántica (LTM).  
      - Lentes o productos → Consultar Catálogo de Productos.  
      - Protocolos → Consultar sección de Guías Clínicas.
   
<img width="1168" height="784" alt="imagen" src="https://github.com/user-attachments/assets/d547420b-6567-4f27-a694-1f0d3f21b7f5" />



## Semana 14

## 5. Protocolo de Razonamiento y Ética

### Sesgo Cognitivo Mitigado: Sesgo de Confirmación (Confirmation Bias)

**Descripción del sesgo:**  
Tendencia a buscar, interpretar o priorizar información que confirma nuestras creencias iniciales, ignorando evidencia que las contradice.

**Riesgo en Mark-AI:**  
Podría llevar a diagnósticos prematuros o recomendaciones sesgadas (ej. asumir rápidamente “solo es miopía” sin considerar otras patologías).

### Contra-Medida Implementada:

**Regla Anti-Confirmación:**

1. Ante cualquier hipótesis inicial, Mark-AI **debe buscar activamente** al menos **dos evidencias** que puedan contradecir o limitar esa hipótesis.
2. Siempre cruzar la información con al menos dos categorías diferentes de la Memoria a Largo Plazo (historial clínico + protocolos/guías clínicas).
3. Si se encuentran datos contradictorios, deben ser mencionados de forma clara y neutral.
4. Nunca emitir una conclusión clínica final sin haber realizado esta verificación activa.

**Ejemplo aplicado:**
- Usuario: “Veo borroso de lejos desde hace un mes”
- Hipótesis inicial: Miopía progresiva
- Verificación obligatoria: Revisar historial de diabetes, edad del paciente, presencia de dolor de cabeza, cambios recientes en visión cercana, etc.

Este protocolo fuerza al bot a utilizar un razonamiento más lento y analítico (Sistema 2), aumentando la seguridad clínica.


<img width="1168" height="784" alt="imagen" src="https://github.com/user-attachments/assets/32897747-0168-42e0-8f76-099be91b8058" />



## Semana 15 - Prueba Lógica y Debugging (Dry Run)

### Caso de Prueba Real:
**Paciente:** Mujer de 52 años dice: “Últimamente veo borroso para leer y a veces me duele la cabeza”.

**Recorrido del Árbol de Decisión:**

1. Consulta optométrica → Sí
2. Requiere evaluación clínica → Sí
3. ¿Suficiente información? → No (falta graduación anterior y antecedentes)
   → Pregunta datos faltantes: edad, síntomas adicionales, enfermedades sistémicas.
4. Usuario responde: 52 años, diabetes tipo 2, visión borrosa de cerca.
5. Hipótesis inicial: Presbicia + posible retinopatía diabética
6. Verificación Anti-Confirmación: Busca evidencias contradictorias → Encuentra posible componente de astigmatismo y fatiga visual.
7. Respuesta final: Recomienda examen refractivo completo + control de retina por posible retinopatía + sugerencia de lentes progresivos.

**Resultado del Dry Run:**  
No se encontraron ramas sin salida ni callejones lógicos.  
El protocolo anti-sesgo funcionó correctamente al obligar al bot a considerar múltiples posibilidades.

**Versión Final:** Árbol de Decisión V2 aprobado.


<img width="1168" height="784" alt="imagen" src="https://github.com/user-attachments/assets/bd8f5245-a280-4221-bd8f-c0455180e8d3" />

