🏎️ Supercar Voice System - Ultimate Edition
Sistema de consulta de información de superautos mediante reconocimiento de voz, desarrollado en Python con interfaz gráfica moderna.

🚀 Características Principales
Reconocimiento de Voz: Búsqueda por comandos de voz en español

Base de Datos Integrada: 13 superautos con información detallada

Interfaz Moderna: Diseño elegante con temática automovilística

Búsqueda por Texto: Alternativa tradicional de búsqueda

Animaciones y Efectos: Experiencia de usuario mejorada

📋 Requisitos del Sistema
Python 3.7 o superior

Micrófono funcionando

Conexión a internet (para reconocimiento de voz)

🔧 Instalación
Paso 1: Clonar o descargar el proyecto
bash
git clone <url-del-repositorio>
cd supercar-voice-system
Paso 2: Crear entorno virtual (recomendado)
bash
python -m venv venv
# En Windows:
venv\Scripts\activate
# En Linux/Mac:
source venv/bin/activate
Paso 3: Instalar dependencias
bash
pip install -r requirements.txt
Si no tienes el archivo requirements.txt, instala manualmente:

bash
pip install PyQt5 speechrecognition pyaudio
Nota para Windows:
Si tienes problemas con pyaudio, prueba:

bash
pip install pipwin
pipwin install pyaudio
Nota para Linux:
Puede que necesites instalar dependencias del sistema:

bash
sudo apt-get install python3-pyaudio portaudio19-dev
🎯 Ejecución
bash
python BD4.py
🎤 Uso del Sistema
Búsqueda por Voz:
Haz clic en "🎤 BUSCAR POR VOZ"

Espera el mensaje "Escuchando..."

Di claramente el nombre del auto (ej: "ferrari 488 gtb")

El sistema mostrará automáticamente la información

Búsqueda por Texto:
Escribe el nombre en el campo de búsqueda

Haz clic en "📝 BUSCAR POR TEXTO" o presiona Enter

Selección Directa:
Haz clic en cualquier auto de la lista

🗂️ Autos Disponibles
Ferrari 488 GTB

Lamborghini Huracán Evo

Bugatti Chiron

McLaren P1

Porsche 918 Spyder

Koenigsegg Agera RS

Pagani Huayra

Aston Martin Valkyrie

Rimac Nevera

Ferrari SF90 Stradale

Lamborghini Aventador SVJ

Bugatti Divo

Maserati MC20

🛠️ Solución de Problemas
Error de Micrófono:
Verifica que el micrófono esté conectado

Revisa los permisos de la aplicación

Prueba en un entorno silencioso

Error de Reconocimiento:
Habla claramente y a un ritmo normal

Usa nombres completos (marca + modelo)

Verifica tu conexión a internet

La aplicación no inicia:
Asegúrate de tener Python 3.7+

Verifica que todas las dependencias estén instaladas

Revisa que el archivo BD4.py esté completo
