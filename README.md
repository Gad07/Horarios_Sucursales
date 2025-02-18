Descripción (Breve)
Aplicación en Flask para generar, organizar y visualizar horarios de colaboradores, con exportación a Excel y PDF. Incluye una vista de consultor para acceder a los archivos organizados por zona.

# Generador de Horarios en Flask

Este proyecto proporciona una herramienta para:
1. **Generar** horarios de colaboradores con turnos de apertura y cierre.
2. **Administrar** descansos y horas de comida de forma automatizada.
3. **Exportar** los horarios en formato Excel.
4. **Generar PDF** con la vista previa de horarios y almacenarlos organizados por zonas.
5. **Ofrecer** una interfaz de consultor para visualizar y descargar los archivos.

## Características

- **Flask**: Sirve como base para levantar el servidor web y manejar rutas.
- **html2canvas + jsPDF**: Generan capturas del DOM en PDF.
- **OpenPyXL**: Facilita la escritura de datos en una plantilla de Excel.
- **Organización por Zonas**: Según la sucursal seleccionada, se generan y guardan archivos en carpetas clasificadas.

## Requisitos

- Python 3.7 o superior
- Pipenv o virtualenv para administrar dependencias (opcional pero recomendado)
- Paquetes de Python: `Flask`, `openpyxl`, etc. (ver sección Instalación)

## Instalación

1. **Clonar el repositorio**:
   ```bash
   git clone https://github.com/tu-usuario/tu-repositorio.git
   cd tu-repositorio
Crear entorno virtual (opcional pero recomendado):

bash
Copiar código
python -m venv venv
source venv/bin/activate     # En Linux / Mac
# o 
venv\Scripts\activate        # En Windows
Instalar dependencias:

bash
Copiar código
pip install -r requirements.txt
Si tienes Pipenv, puedes usar: pipenv install en su lugar.

Ejecutar la aplicación:

bash
Copiar código
python app.py
La aplicación se ejecutará en http://127.0.0.1:5000/ por defecto.

Uso
Generación de horarios:

Accede a http://127.0.0.1:5000/.
Llena el formulario con la sucursal, número de colaboradores y datos de entrada/salida.
Al dar clic en Generar Excel, se descargará un archivo con los horarios en .xlsx.
Generar y almacenar PDF:

Tras visualizar la tabla de horarios, presiona Generar y almacenar PDF.
Se creará un PDF con la previsualización de horarios y se almacenará en la carpeta correspondiente a la zona.
Interfaz Consultor:

Ingresa a http://127.0.0.1:5000/consultor.
Allí verás las zonas y los archivos generados (tanto PDF como Excel).
Puedes previsualizarlos en el navegador y/o descargarlos.
Estructura de Archivos
php
Copiar código
tu-repositorio/
├── horarios/                       # Carpeta donde se almacenan los archivos generados (por zona)
├── templates/
│   ├── index.html                 # Formulario para generar horarios
│   └── consultor.html             # Vista del consultor
├── static/                        # Archivos estáticos (CSS, JS, imágenes si aplica)
├── Horarios_Plantilla.xlsx        # Plantilla de Excel para los horarios
├── app.py                         # Archivo principal Flask
├── requirements.txt               # Dependencias
└── README.md

Personalización
Zonas y Sucursales: Si quieres modificar la clasificación de las sucursales, ajusta la función obtener_zona_por_sucursal(sucursal) en app.py.
Plantilla Excel: Para cambiar la estructura o el diseño, edita Horarios_Plantilla.xlsx.
Vista en PDF: Se utilizan librerías JavaScript (html2canvas, jsPDF) para capturar y generar el PDF. Puedes modificar el estilo y formato en index.html.

Contribuciones
¡Las contribuciones son bienvenidas! Puedes abrir issues para reportar bugs o sugerir mejoras, y enviar pull requests con tus cambios.

Licencia
Este proyecto se distribuye bajo la LICENCIA MIT, por favor revisa el archivo de licencia para más detalles.
