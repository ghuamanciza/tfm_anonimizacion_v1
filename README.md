# README: Anonimizador de Sentencias y Resoluciones Judiciales (Poder Judicial del Perú)

---

Este proyecto de Inteligencia Artificial tiene como objetivo **anonimizar automáticamente los datos personales sensibles** presentes en las sentencias y autos de resoluciones emitidas por las diversas cortes e instancias del Poder Judicial del Perú. Su implementación busca fortalecer la protección de la privacidad de los ciudadanos y asegurar el cumplimiento de la Ley de Protección de Datos Personales (Ley N° 29733) y su reglamento en el contexto judicial.

---

## 🚀 Características Principales

* **Identificación de Entidades Nombradas (NER) Avanzada:** Utiliza modelos de IA para detectar y clasificar con alta precisión nombres de personas, números de DNI, direcciones, números de teléfono, correos electrónicos, y cualquier otra información que pueda identificar a individuos en los documentos judiciales.
* **Anonimización Robusta:** Aplica técnicas de sustitución, eliminación o generalización para anonimizar la información personal identificada, garantizando que los datos originales no puedan ser inferidos.
* **Soporte Multilingüe (Español):** Diseñado específicamente para el idioma español, con un enfoque en la terminología y estructuras utilizadas en el contexto legal peruano.
* **Escalabilidad:** Capaz de procesar grandes volúmenes de documentos judiciales de manera eficiente.
* **Auditoría y Trazabilidad:** Incluye mecanismos para registrar las acciones de anonimización realizadas, facilitando la auditoría y el cumplimiento normativo.
* **Integración Potencial:** Arquitectura modular que permite su futura integración con sistemas existentes del Poder Judicial del Perú.

---

## 🎯 Objetivos del Proyecto

* **Garantizar la Privacidad:** Proteger los datos personales de los ciudadanos involucrados en procesos judiciales.
* **Cumplimiento Normativo:** Asegurar la adhesión a la Ley de Protección de Datos Personales del Perú.
* **Transparencia con Resguardo:** Permitir la publicación de documentos judiciales para fines de transparencia y análisis sin comprometer la identidad de las partes.
* **Optimización de Recursos:** Automatizar un proceso que actualmente podría requerir una revisión manual intensiva, liberando recursos humanos para tareas de mayor valor.
* **Promover la Justicia Abierta:** Facilitar el acceso a la información judicial de manera responsable y ética.

---

## 🛠️ Tecnologías Utilizadas (Propuesta)

* **Lenguaje de Programación:** Python
* **Frameworks de IA/ML:**
    * **Procesamiento de Lenguaje Natural (PNL):** SpaCy, Transformers (Hugging Face)
    * **Deep Learning:** PyTorch o TensorFlow
* **Gestión de Datos:** (Pendiente de definir, según la infraestructura del PJ)
* **Control de Versiones:** Git
* **Ambiente de desarrollo y pruebas AWS SageMaker Studio Lab**

---

## 🚀 Configuración y Uso (Ejemplo Básico)

### Requisitos

* Python 3.8+
* `pip` (gestor de paquetes de Python)

### Instalación

1.  **Clonar el repositorio:**
    ```bash
    git clone [https://github.com/tu-usuario/nombre-del-proyecto.git](https://github.com/tu-usuario/nombre-del-proyecto.git)
    cd nombre-del-proyecto
    ```
2.  **Crear un entorno virtual (recomendado):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # En Linux/macOS
    # venv\Scripts\activate   # En Windows
    ```
3.  **Instalar las dependencias:**
    ```bash
    pip install -r requirements.txt
    ```
4.  **Descargar modelos de SpaCy (ejemplo):**
    ```bash
    python -m spacy download es_core_news_lg
    ```

### Uso Básico

```python
# Ejemplo de uso (se necesitará una implementación más completa)
from anonymizer import Anonymizer

# Cargar un documento de sentencia o resolución
documento_judicial = """
En la ciudad de Lima, a los 25 días del mes de junio de 2025, el Juez Dr. Juan Pérez López, del Juzgado Civil de Lima, resolvió el caso N° 123-2024. La demandante, María Elena Gonzales Rojas, con DNI 12345678, residente en Av. Los Pinos 456, San Isidro, presentó una demanda contra la empresa XYZ S.A. Su abogado fue el Dr. Carlos Alberto Ramirez Soto.
"""

anonimizador = Anonymizer()
documento_anonimizado = anonimizador.anonymize_text(documento_judicial)

print("--- Documento Original ---")
print(documento_judicial)
print("\n--- Documento Anonimizado ---")
print(documento_anonimizado)
