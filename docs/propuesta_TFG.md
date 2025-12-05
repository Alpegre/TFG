# Propuesta de Trabajo de Fin de Grado

## Red Neuronal Generadora de Trazos del Alfabeto: Modernización de Simulador y Modelo Generativo

---

## 1. Título Propuesto

**Red Neuronal Generadora de Trazos del Alfabeto: Modernización e Integración con Entornos Multimedia Interactivos**

---

## 2. Resumen / Abstract

El presente Trabajo de Fin de Grado (TFG) tiene como objetivo principal el diseño, desarrollo e implementación de un sistema basado en redes neuronales capaz de generar trazos de caracteres alfabéticos de forma autónoma. Este trabajo surge de la necesidad de modernizar herramientas educativas existentes, específicamente un simulador desarrollado en Max/MSP que utiliza software deprecated (JavaNNS), adaptándolo a tecnologías actuales de aprendizaje automático y deep learning.

La motivación principal de este proyecto es doble: por un lado, dar continuidad a trabajos previos de investigación docente en el ámbito de la inteligencia artificial y la música generativa; por otro lado, explorar las capacidades de las redes neuronales generativas para la creación de trazos vectoriales que representen caracteres del alfabeto, frente al enfoque tradicional de generación de imágenes rasterizadas.

El contexto de este trabajo se enmarca en la intersección entre la inteligencia artificial, el procesamiento de secuencias temporales y los entornos multimedia interactivos. Se trabajará con datasets de patrones de letras existentes (letterstrain.pat, lettersval.pat) y se desarrollarán nuevos conjuntos de datos que capturen la información temporal y espacial de los trazos manuscritos.

Los resultados esperados incluyen: un modelo neuronal entrenado capaz de generar secuencias de puntos que representen trazos de letras, una integración funcional con Max/MSP mediante protocolos de comunicación (OSC/WebSocket), documentación técnica completa y una demostración interactiva que permita visualizar y evaluar los resultados del modelo.

Este TFG contribuirá tanto al ámbito académico como práctico, sirviendo como material didáctico actualizado para asignaturas de Inteligencia Artificial y como punto de partida para futuras investigaciones en generación de contenido artístico mediante redes neuronales.

**Palabras clave**: Redes neuronales, generación de trazos, alfabeto, Max/MSP, deep learning, RNN, LSTM, OSC, modernización de software.

---

## 3. Objetivos

### 3.1 Objetivo General

Diseñar e implementar un sistema basado en redes neuronales que sea capaz de generar trazos de caracteres alfabéticos, integrándolo con entornos multimedia interactivos (Max/MSP) para su uso educativo y artístico.

### 3.2 Objetivos Específicos

1. **Analizar el estado del arte** en generación de caracteres manuscritos y secuencias temporales mediante redes neuronales (RNN, LSTM, Transformers, modelos generativos).

2. **Estudiar y documentar el sistema legacy** existente (simulador Max/MSP + JavaNNS) para comprender su funcionamiento y requisitos de integración.

3. **Diseñar una arquitectura neuronal** adecuada para la generación de secuencias de puntos que formen trazos de letras, considerando aspectos como la variabilidad estilística y la coherencia visual.

4. **Crear o adaptar un dataset** de trazos de letras en formato secuencial (coordenadas x, y, estado del lápiz), partiendo de los archivos .pat existentes y/o datasets públicos como QuickDraw o IAM Handwriting.

5. **Implementar el modelo neuronal** utilizando frameworks modernos (TensorFlow/PyTorch), incluyendo preprocesamiento de datos, entrenamiento y evaluación.

6. **Desarrollar un módulo de comunicación** que permita la integración del modelo con Max/MSP mediante protocolos OSC o WebSocket.

7. **Crear una demostración interactiva** que permita generar trazos en tiempo real y visualizar los resultados.

8. **Evaluar cuantitativamente y cualitativamente** los resultados obtenidos, comparándolos con el sistema original cuando sea posible.

9. **Documentar exhaustivamente** todo el proceso: código, datasets, modelos entrenados, guías de uso e integración.

10. **Elaborar la memoria final del TFG** siguiendo las normativas académicas establecidas.

---

## 4. Problemas Abordados

Este TFG aborda una serie de retos técnicos y educativos que se detallan a continuación:

### 4.1 Retos Técnicos

| Problema | Descripción | Impacto |
|----------|-------------|---------|
| **Software deprecated** | JavaNNS es un software de redes neuronales descontinuado, con dependencias obsoletas (Java antiguo) y limitaciones en arquitecturas modernas | Impide el uso de técnicas actuales de deep learning y dificulta el mantenimiento |
| **Generación de trazos vs. imágenes** | Los modelos generativos populares (GANs, VAEs) producen imágenes rasterizadas; se requiere generar secuencias de puntos (trazos vectoriales) | Mayor complejidad en el modelado de secuencias temporales y estados del lápiz |
| **Integración con Max/MSP** | El simulador original está acoplado a JavaNNS; se necesita una capa de comunicación moderna | Requiere diseño de protocolos de comunicación (OSC/WebSocket) y posible refactorización del parche Max |
| **Dataset específico** | Los archivos .pat existentes tienen un formato específico de JavaNNS y pueden no contener información temporal de los trazos | Necesidad de crear o adaptar datasets con información secuencial (x, y, pen_state) |
| **Variabilidad en la generación** | Las letras deben ser reconocibles pero con cierta variabilidad natural, simulando escritura humana | Requiere técnicas de generación estocástica controlada |

### 4.2 Retos Educativos

| Problema | Descripción |
|----------|-------------|
| **Material didáctico obsoleto** | Los recursos actuales de la asignatura utilizan herramientas que ya no reciben soporte |
| **Brecha teórico-práctica** | Los estudiantes aprenden conceptos modernos de IA pero practican con software antiguo |
| **Documentación insuficiente** | El sistema actual carece de documentación actualizada que facilite su comprensión y extensión |

---

## 5. Resultados Previstos

Al finalizar este TFG se entregarán los siguientes resultados:

### 5.1 Código Fuente

- **Modelo neuronal** implementado en Python (TensorFlow o PyTorch)
- **Scripts de preprocesamiento** para transformación de datos
- **Módulo de comunicación** OSC/WebSocket para integración con Max/MSP
- **Scripts de entrenamiento y evaluación**
- **API/servidor** para inferencia en tiempo real
- **Tests unitarios y de integración**

### 5.2 Datasets

- Dataset de entrenamiento con trazos de letras en formato secuencial
- Dataset de validación
- Dataset de test
- Documentación del formato y proceso de creación

### 5.3 Modelos Entrenados

- Modelo(s) preentrenado(s) con diferentes configuraciones
- Checkpoints de entrenamiento
- Logs de entrenamiento (TensorBoard u equivalente)

### 5.4 Integración con Max/MSP

- Parche Max/MSP actualizado o nuevo parche de demostración
- Documentación de la API de comunicación
- Ejemplos de uso

### 5.5 Demostración Interactiva

- Aplicación web o desktop para generación de trazos en tiempo real
- Interfaz de visualización de resultados

### 5.6 Documentación

- README con instrucciones de instalación y uso
- Documentación técnica de la arquitectura
- Guía de integración con Max/MSP
- Jupyter notebooks explicativos

### 5.7 Memoria Final del TFG

- Documento académico completo siguiendo normativa de la universidad
- Anexos con código, diagramas y resultados experimentales

### 5.8 Métricas de Evaluación Propuestas

| Tipo | Métrica | Descripción |
|------|---------|-------------|
| Cuantitativa | **Pérdida de reconstrucción** | Error medio entre trazos generados y reales |
| Cuantitativa | **Inception Score adaptado** | Medida de calidad y diversidad |
| Cuantitativa | **Accuracy de reconocimiento** | Porcentaje de letras correctamente reconocidas por un clasificador externo |
| Cualitativa | **Evaluación visual** | Puntuación humana de legibilidad y naturalidad |
| Cualitativa | **Test de Turing simplificado** | Distinción humano/máquina en los trazos |
| Funcional | **Latencia de generación** | Tiempo de respuesta para uso interactivo |

---

## 6. Metodología y Plan de Trabajo

### 6.1 Metodología

Se seguirá una metodología iterativa e incremental, combinando:

- **Investigación bibliográfica** continua
- **Desarrollo ágil** con sprints de 2-3 semanas
- **Experimentación científica** documentada
- **Control de versiones** con Git/GitHub
- **Revisiones periódicas** con la tutora

### 6.2 Cronograma (Estimación total: 300-350 horas)

| Fase | Descripción | Duración Est. | Horas |
|------|-------------|---------------|-------|
| **Fase 1** | Análisis y Estado del Arte | Semanas 1-3 | 40h |
| | - Revisión bibliográfica (papers, tutoriales) | | 20h |
| | - Estudio del sistema legacy (Max/MSP + JavaNNS) | | 15h |
| | - Definición de requisitos y alcance | | 5h |
| **Fase 2** | Diseño de la Arquitectura | Semanas 4-5 | 35h |
| | - Selección de arquitectura neuronal (RNN/LSTM/Transformer) | | 15h |
| | - Diseño del pipeline de datos | | 10h |
| | - Diseño de la interfaz de comunicación | | 10h |
| **Fase 3** | Preparación del Dataset | Semanas 6-8 | 45h |
| | - Análisis de datasets existentes (QuickDraw, IAM) | | 10h |
| | - Conversión/adaptación de archivos .pat | | 15h |
| | - Creación de dataset propio si es necesario | | 15h |
| | - Preprocesamiento y normalización | | 5h |
| **Fase 4** | Implementación del Modelo | Semanas 9-14 | 80h |
| | - Implementación de la arquitectura base | | 25h |
| | - Entrenamiento inicial y ajuste de hiperparámetros | | 30h |
| | - Experimentación con variantes | | 15h |
| | - Optimización del modelo | | 10h |
| **Fase 5** | Integración con Max/MSP | Semanas 15-17 | 45h |
| | - Implementación del servidor OSC/WebSocket | | 20h |
| | - Desarrollo/adaptación del parche Max | | 15h |
| | - Pruebas de integración | | 10h |
| **Fase 6** | Demostración y Evaluación | Semanas 18-19 | 35h |
| | - Desarrollo de demo interactiva | | 15h |
| | - Evaluación cuantitativa | | 10h |
| | - Evaluación cualitativa (tests con usuarios) | | 10h |
| **Fase 7** | Documentación y Memoria | Semanas 20-24 | 70h |
| | - Redacción de la memoria | | 45h |
| | - Documentación técnica y README | | 15h |
| | - Preparación de la presentación | | 10h |

### 6.3 Diagrama de Gantt Simplificado

```
Mes 1    |████████████░░░░░░░░░░░░|  Fase 1: Análisis
Mes 2    |░░░░░░░░████████████░░░░|  Fase 2: Diseño
Mes 2-3  |░░░░░░░░░░░░████████████|  Fase 3: Dataset
Mes 3-4  |████████████████████░░░░|  Fase 4: Modelo
Mes 5    |░░░░████████████████░░░░|  Fase 5: Integración
Mes 5-6  |░░░░░░░░░░░░████████████|  Fase 6: Demo/Evaluación
Mes 6    |████████████████████████|  Fase 7: Documentación
```

---

## 7. Recursos y Herramientas Propuestas

### 7.1 Lenguajes de Programación

| Lenguaje | Uso |
|----------|-----|
| **Python 3.10+** | Desarrollo del modelo, preprocesamiento, servidor |
| **JavaScript** | Posible interfaz web de demostración |
| **Max/MSP** | Integración con entorno multimedia |

### 7.2 Frameworks y Librerías

| Herramienta | Versión | Uso |
|-------------|---------|-----|
| **PyTorch** | 2.x | Framework principal de deep learning |
| **TensorFlow/Keras** | 2.x | Alternativa para experimentación |
| **NumPy** | 1.24+ | Operaciones numéricas |
| **Matplotlib/Seaborn** | Latest | Visualización de resultados |
| **python-osc** | Latest | Comunicación OSC |
| **websockets** | Latest | Comunicación WebSocket |
| **Flask/FastAPI** | Latest | API REST para inferencia |
| **Jupyter** | Latest | Notebooks de experimentación |

### 7.3 Hardware

| Recurso | Especificación | Uso |
|---------|----------------|-----|
| **GPU** | NVIDIA con CUDA (ej. RTX 3060+) | Entrenamiento acelerado |
| **RAM** | Mínimo 16GB | Procesamiento de datasets |
| **Almacenamiento** | SSD con 100GB+ libres | Datasets y checkpoints |
| **Alternativa cloud** | Google Colab Pro / Kaggle | Si no hay GPU local |

### 7.4 Software y Herramientas

| Herramienta | Uso |
|-------------|-----|
| **Git/GitHub** | Control de versiones |
| **VS Code / PyCharm** | IDE de desarrollo |
| **Max/MSP 8** | Entorno multimedia |
| **Docker** | Contenedorización (opcional) |
| **Weights & Biases / MLflow** | Tracking de experimentos |
| **LaTeX / Word** | Redacción de memoria |

### 7.5 Repositorios y Datasets de Referencia

| Recurso | URL | Descripción |
|---------|-----|-------------|
| Google QuickDraw | [quickdraw.withgoogle.com](https://quickdraw.withgoogle.com/data) | Dataset de dibujos rápidos |
| IAM Handwriting DB | [fki.tic.heia-fr.ch](https://fki.tic.heia-fr.ch/databases/iam-handwriting-database) | Escritura manuscrita |
| EMNIST | [nist.gov/itl/products-and-services/emnist-dataset](https://www.nist.gov/itl/products-and-services/emnist-dataset) | Caracteres manuscritos |
| Sketch-RNN | [github.com/magenta/magenta](https://github.com/magenta/magenta/tree/main/magenta/models/sketch_rnn) | Modelo de referencia de Google |

### 7.6 Bibliografía Provisional

1. Graves, A. (2013). *Generating Sequences With Recurrent Neural Networks*. arXiv:1308.0850.

2. Ha, D., & Eck, D. (2018). *A Neural Representation of Sketch Drawings*. ICLR 2018.

3. Vaswani, A. et al. (2017). *Attention Is All You Need*. NeurIPS 2017.

4. Goodfellow, I., Bengio, Y., & Courville, A. (2016). *Deep Learning*. MIT Press.

5. Chollet, F. (2021). *Deep Learning with Python*, 2nd Ed. Manning.

6. Cycling '74. (2023). *Max 8 Documentation*. [docs.cycling74.com](https://docs.cycling74.com/)

7. Wright, M. (2005). *Open Sound Control: an enabling technology for musical networking*. Organised Sound.

---

## 8. Criterios de Evaluación y Validación

### 8.1 Criterios de Éxito del Proyecto

El proyecto se considerará exitoso si cumple los siguientes criterios:

#### 8.1.1 Criterios Funcionales

- [ ] El modelo genera secuencias de puntos que forman letras reconocibles del alfabeto
- [ ] La integración con Max/MSP permite comunicación bidireccional
- [ ] La demo interactiva funciona en tiempo real (latencia < 500ms)
- [ ] El código es reproducible siguiendo la documentación

#### 8.1.2 Métricas Cuantitativas

| Métrica | Umbral Mínimo | Umbral Óptimo |
|---------|---------------|---------------|
| **Accuracy de reconocimiento** (clasificador externo) | >70% | >85% |
| **Pérdida de reconstrucción** | < baseline | Mejora >20% vs baseline |
| **Diversidad de generación** | >0.5 (escala 0-1) | >0.7 |
| **Latencia de inferencia** | <1s | <200ms |
| **Cobertura del alfabeto** | 26 letras (mayúsculas) | +26 minúsculas + números |

#### 8.1.3 Métricas Cualitativas

| Aspecto | Método de Evaluación |
|---------|---------------------|
| **Legibilidad** | Encuesta a 10+ personas: "¿Qué letra es?" |
| **Naturalidad** | Puntuación 1-5 de aspecto manuscrito |
| **Variabilidad** | ¿Las muestras son diversas pero consistentes? |
| **Usabilidad** | Test de usuario de la demo interactiva |

### 8.2 Pruebas con el Sistema Original

Cuando sea posible, se realizarán pruebas comparativas con el simulador Max/MSP + JavaNNS original:

1. **Test de equivalencia funcional**: ¿El nuevo sistema produce resultados comparables?
2. **Test de rendimiento**: ¿El nuevo sistema es más rápido/eficiente?
3. **Test de facilidad de uso**: ¿La integración es más sencilla?

### 8.3 Validación Académica

- Revisión continua con la tutora del TFG
- Cumplimiento de la normativa de TFG de la universidad
- Presentación y defensa ante tribunal

---

## 9. Riesgos y Mitigación

| ID | Riesgo | Probabilidad | Impacto | Estrategia de Mitigación |
|----|--------|--------------|---------|--------------------------|
| R1 | **Dificultad para conseguir un dataset adecuado** | Media | Alto | Usar datasets públicos (QuickDraw) como plan B; crear herramienta de captura de trazos si es necesario |
| R2 | **El modelo no converge o genera resultados pobres** | Media | Alto | Comenzar con arquitecturas probadas (Sketch-RNN); iterar con diferentes hiperparámetros; reducir scope si es necesario |
| R3 | **Problemas de compatibilidad con Max/MSP** | Baja | Medio | Usar protocolos estándar (OSC); documentar versiones; tener alternativa WebSocket |
| R4 | **Falta de acceso a GPU para entrenamiento** | Baja | Medio | Usar Google Colab/Kaggle; optimizar modelo para CPU si es necesario |
| R5 | **Retrasos en el cronograma** | Media | Medio | Planificar con buffer; priorizar funcionalidades core; comunicar proactivamente con tutora |
| R6 | **Complejidad mayor a la esperada en integración** | Media | Medio | Modularizar el desarrollo; tener interfaz de comunicación independiente del modelo |
| R7 | **Pérdida de datos o código** | Baja | Alto | Uso riguroso de Git; backups periódicos; checkpoints frecuentes |
| R8 | **El sistema legacy no funciona para comparación** | Media | Bajo | Documentar el intento; basarse en documentación existente; reducir peso de esta comparación en evaluación |

### Plan de Contingencia General

Si el proyecto enfrenta bloqueos críticos:
1. Reducir el scope a generación offline (sin tiempo real)
2. Limitar el alfabeto a un subconjunto de letras
3. Sustituir Max/MSP por una interfaz web propia
4. Priorizar documentación y memoria sobre funcionalidades adicionales

---

## 10. Entregables y Formato

### 10.1 Lista de Entregables

| ID | Entregable | Formato | Fecha Orientativa |
|----|------------|---------|-------------------|
| E1 | Propuesta de TFG aprobada | PDF/MD | Semana 1 |
| E2 | Informe de análisis y estado del arte | PDF/MD | Semana 3 |
| E3 | Documento de diseño de arquitectura | PDF/MD + diagramas | Semana 5 |
| E4 | Dataset preparado y documentado | Archivos + README | Semana 8 |
| E5 | Código del modelo (v1.0) | Repositorio GitHub | Semana 14 |
| E6 | Módulo de integración Max/MSP | Código + parche Max | Semana 17 |
| E7 | Demo interactiva | Aplicación ejecutable | Semana 19 |
| E8 | Informe de evaluación | PDF/MD | Semana 19 |
| E9 | Documentación técnica completa | README + docs/ | Semana 22 |
| E10 | Borrador de memoria TFG | PDF/Word | Semana 22 |
| E11 | **Memoria final TFG** | PDF | Semana 24 |
| E12 | Presentación para defensa | PPT/PDF | Semana 24 |

### 10.2 Formato de Entrega

- **Código**: Repositorio GitHub público/privado con estructura estándar
  ```
  /
  ├── README.md
  ├── requirements.txt
  ├── setup.py
  ├── src/
  │   ├── model/
  │   ├── data/
  │   ├── communication/
  │   └── demo/
  ├── notebooks/
  ├── tests/
  ├── docs/
  ├── data/
  │   ├── raw/
  │   └── processed/
  ├── models/
  │   └── checkpoints/
  └── max/
      └── patches/
  ```

- **Documentación**: Markdown en el repositorio + PDF para entregas formales
- **Memoria**: Formato académico según normativa de la universidad (LaTeX o Word)
- **Datasets**: Archivos comprimidos con documentación de formato y licencia

### 10.3 Hitos Clave

```
[Hito 1] ──────► Propuesta aprobada (Semana 1)
                │
[Hito 2] ──────► Dataset listo (Semana 8)
                │
[Hito 3] ──────► Modelo funcional (Semana 14)
                │
[Hito 4] ──────► Integración completa (Semana 17)
                │
[Hito 5] ──────► Demo + Evaluación (Semana 19)
                │
[Hito 6] ──────► ENTREGA FINAL (Semana 24)
```

---

## Notas Adicionales

- Este documento se actualizará según avance el proyecto
- Las fechas son orientativas y están sujetas al calendario académico
- Cualquier cambio significativo en el alcance será comunicado y aprobado por la tutora
- El repositorio de referencia contiene material legacy (parches Max, JavaNNS) que será analizado en la Fase 1

---

*Documento generado para el TFG - Grado en Ingeniería Informática*

*Última actualización: Diciembre 2024*
