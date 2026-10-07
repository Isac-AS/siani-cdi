# Resumen: Introducción y Tipos de Datos en Ciencia de Datos

## 1. Definición de Ciencia de Datos
Proceso interdisciplinar para extraer conocimiento útil de datos mediante descubrimiento,
formulación de hipótesis y análisis (NIST, 2015). Combina estadística, minería de datos,
aprendizaje automático y analítica predictiva (Liu, 2015).

---

## 2. Contexto y Crecimiento de Datos
Desde los años 80, el almacenamiento de datos crece exponencialmente:

| Año | Volumen Mundial |
|-----|-----------------|
| 2023 | ~120 ZB |
| 2025 (proyección) | ~181 ZB |
| 2029 (proyección) | ~3x el volumen de 2025 |

El **90%** de los datos existentes se generaron en los últimos 2 años.

Ejemplos destacables:
- **YouTube**: 500 horas de vídeo subidas por minuto
- **Instagram**: 1.300M de imágenes compartidas diariamente
- **LHC (CERN)**: 1 Petabyte de datos por día
- **Event Horizon Telescope**: 15 Petabytes por campaña de observación

Unidades: Byte → KB → MB → GB → TB → PB → EB → ZB → YB (cada paso x1024).

---

## 3. Clasificación por Cantidad de Información (Dorian Pyle, 1999)

| Tipo | Características | Operaciones permitidas | Ejemplo |
|------|----------------|------------------------|---------|
| **Nominal** | Símbolos/etiquetas sin orden | Igualdad (=) | Color: rojo, azul, negro |
| **Ordinal** | Valores con orden transitivo | Orden (<, >) | frío < templado < calor |
| **Continuo/Racional** | Medidas numéricas con cero absoluto | Todas (+, −, ×, ÷) | Temperatura °C, ventas |

Notas:
- Los nominales también se llaman **categóricos** (caso especial: dicotómicos o booleanos).
- Los ordinales también se llaman **enumerados** o discretos.
- Los racionales también se llaman **numéricos** o continuos.
- Un dato nominal puede ser numérico sin implicar orden: código postal 35001 NO es menor que 35002.
- En los racionales importa la **unidad de medida** (dato dimensional) salvo datos adimensionales
  (p.e. coeficiente de Poisson).

---

## 4. Clasificación por Estructura

| Tipo | Descripción | Ejemplos |
|------|-------------|----------|
| **Estructurados** | Organizados en tabla (filas/columnas) | CSV, Excel, BD relacionales |
| **Semi-estructurados** | Contienen etiquetas semánticas propias | XML, JSON, HTML |
| **No estructurados** | Sin estructura, ~80% de los datos | Texto, imágenes, audio, vídeo |

### Terminología de tablas (DataFrame en Pandas)
- Tabla → **Conjunto de Datos**
- Registro → **Muestra o instancia**
- Campo → **Atributo, variable o característica** (xi)
- Nº de atributos → **Dimensión del problema**
- Atributo clase y: nominal → **Clasificación**; racional → **Regresión**
- Divisiones: entrenamiento, validación y test

### Almacenamiento según estructura
- **Estructurados**: CSV (texto plano, problemas de codificación), hojas de cálculo (XLSX),
  BD relacionales (Oracle, SQL Server, DB2, PostgreSQL, MySQL) con esquema a priori y SQL.
- **Semi-estructurados**: XML (estructura de árbol, elemento raíz, extensible, distingue
  mayúsculas; metadatos como atributos, datos como elementos) y JSON (pares nombre-valor
  entre llaves; listas entre corchetes; admite strings, números, true/false/null, objetos
  y listas anidadas).
- **No estructurados**: archivos en carpetas y BD No-SQL.

### Bases de datos No-SQL
| Tipo | Descripción | Ejemplos |
|------|-------------|----------|
| **Clave-Valor** | Clave única → valor binario (más popular, eficiente) | Redis, DynamoDB |
| **Documentales** | Documentos JSON/XML con búsqueda por pares clave-valor | MongoDB, CouchDB, Firestore |
| **Grafo** | Nodos y aristas; consultas por patrones | Neo4j, ArangoDB, Virtuoso |

No usan SQL, no se basan en relaciones, no suelen permitir JOIN, arquitecturas distribuidas.

---

## 5. Metodologías de Proyectos

**¿Por qué estandarizar?** Proceso fiable y repetible, madurez de la disciplina,
replicabilidad de proyectos y facilidad de planificación y gestión.

### CRISP-DM (la más popular)
1. **Business Understanding** – Objetivos del negocio, criterios de éxito, evaluación de la
   situación, objetivos técnicos y plan del proyecto.
2. **Data Understanding** – Colección inicial, descripción, exploración y verificación de
   calidad de los datos.
3. **Data Preparation** – Selección, limpieza, construcción, integración y formateo.
   Consume ~**80% del tiempo**.
4. **Modeling** – Selección de técnica, diseño de prueba (train/validation/test),
   construcción y validación del modelo.
5. **Evaluation** – Resultados frente a factores de éxito, revisión del proceso y
   siguientes pasos.
6. **Deployment** – Plan de implantación, monitorización y mantenimiento, informe final
   y revisión del proyecto.

### Otras metodologías
- **IBM Data Science Methodology** (2016).
- **TDSP** (Microsoft, 2017): ágil. Ciclo: Conocimiento del negocio → Adquisición y
  comprensión de datos → Modelado → Despliegue → Aceptación del cliente. Incluye
  estructura estandarizada de proyectos, infraestructura compartida y herramientas.

---

## 6. Perfil del Científico de Datos (Diagrama de Venn, Drew Conway)
Intersección de tres competencias:
- **Habilidades de programación/informática**
- **Conocimiento matemático y estadístico**
- **Experiencia en el dominio del problema**

La ausencia de alguna produce análisis deficientes: aplicar métodos sin comprender
resultados, comprender el método sin entender el negocio, o análisis sin rigor técnico.

---

**Bibliografía clave**: Pyle (1999), NIST (2015), Liu (2015), IBM SPSS CRISP-DM Guide.