# Gestor Inteligente de Recetas

Aplicación web en Streamlit para generar, guardar, consultar, editar, eliminar, buscar y exportar recetas de cocina usando SQLite e IA.

## Herramienta de extracción de operativos

Abre `extractor_operativos.html` en el navegador para pegar notas de operativos policiales y generar automáticamente la tabla estructurada con procedencia, personas, motocicletas, vehículos, armas, puntos de drogas y nacionales haitianos detenidos. La herramienta también permite copiar la tabla o descargarla como CSV.

Para crear el archivo CSV directamente en esta carpeta, abre `abrir_extractor_csv.bat` y usa el boton `Crear CSV en carpeta`. El archivo se guarda como `operativos_extraidos.csv`.

## Estructura recomendada

```text
.
├── app.py
├── requirements.txt
├── recetas.db                  # Se crea automáticamente al ejecutar la app
└── .streamlit/
    └── secrets.toml            # Opcional para usar OpenAI
```

## Instalación

```bash
pip install -r requirements.txt
```

## Configuración opcional de OpenAI

Crea `.streamlit/secrets.toml` con:

```toml
OPENAI_API_KEY = "tu_api_key"
OPENAI_MODEL = "gpt-4o-mini"
```

Si no configuras una API key, la aplicación usa una función simulada para generar recetas.

## Ejecución

```bash
streamlit run app.py
```
