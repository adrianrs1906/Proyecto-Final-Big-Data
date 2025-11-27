Requisitos del Sistema
Para ejecutar AutoNavigator necesitas:

Python 3.8 o versión superior instalado en tu sistema

Un micrófono funcionando correctamente

Conexión a internet activa (para el reconocimiento de voz y acceso a sitios web)

Proceso de Instalación
Paso 1: Descargar el Proyecto
Primero, descarga el archivo BD11.py desde el repositorio de GitHub y guárdalo en una carpeta de tu preferencia.

Paso 2: Crear Entorno Virtual (Recomendado)
Abre tu terminal o línea de comandos y navega hasta la carpeta donde guardaste el archivo. Luego crea un entorno virtual ejecutando: python -m venv venv

Para activar el entorno virtual:

En Windows: venv\Scripts\activate

En Linux/Mac: source venv/bin/activate

Paso 3: Instalar Dependencias
Con el entorno virtual activado, instala las librerías necesarias ejecutando: pip install PyQt5 speechrecognition

Para mejorar el rendimiento del audio, puedes instalar adicionalmente: pip install pyaudio

Si encuentras problemas instalando pyaudio en Windows, puedes usar: pip install pipwin seguido de pipwin install pyaudio

En sistemas Linux, si tienes dificultades, prueba instalando: sudo apt-get install python3-pyaudio portaudio19-dev

Ejecución del Programa
Una vez completada la instalación, ejecuta el programa con el comando: python BD11.py

La aplicación se iniciará mostrando una ventana con la interfaz automovilística.

Guía de Uso
Búsqueda por Voz
Haz clic en el botón grande "🎤 ACTIVAR COMANDO DE VOZ"

Espera a que el indicador visual cambie a rojo y veas el mensaje "Estado: escuchando..."

Di claramente el nombre de la marca que deseas buscar (por ejemplo: "ferrari", "lamborghini", "porsche")

El sistema procesará tu voz, detectará la marca y abrirá automáticamente el sitio web oficial

Búsqueda por Texto
Escribe el nombre de la marca en el campo de texto ubicado en la parte izquierda de la interfaz

Presiona la tecla Enter o haz clic en el botón "ABRIR"

El sistema buscará la marca y abrirá su sitio web oficial

Selección Manual Rápida
En la sección inferior derecha de la interfaz encontrarás botones con todas las marcas disponibles

Haz clic directamente en cualquier botón de marca para acceder instantáneamente a su sitio web

Usa la opción "VER TODAS LAS URLS" del menú para ver un listado completo

Marcas Disponibles
El sistema incluye 30 marcas organizadas en tres categorías:

Marcas Deportivas: Ferrari, Lamborghini, Bugatti, McLaren, Porsche, Koenigsegg, Pagani, Aston Martin, Rimac, Maserati

Marcas de Lujo: Mercedes-Benz, BMW, Audi, Lexus, Bentley, Rolls-Royce, Jaguar, Land Rover, Volvo, Infiniti

Marcas Generales: Toyota, Honda, Nissan, Ford, Chevrolet, Dodge, Subaru, Alfa Romeo, Citroën, Acura

Solución de Problemas Comunes
Si el Reconocimiento de Voz No Funciona:
Verifica que el micrófono esté correctamente conectado y configurado

Comprueba los permisos de la aplicación para acceder al micrófono

Asegúrate de tener conexión a internet activa

Habla claramente y en un entorno con poco ruido ambiental

Si persisten los problemas, usa el método de búsqueda por texto

Si la Aplicación No Inicia:
Confirma que tienes Python 3.8 o superior instalado

Verifica que todas las dependencias estén correctamente instaladas

Asegúrate de que el archivo BD11.py esté completo y sin modificaciones

Si el Audio Presenta Problemas:
En Windows, intenta usar pipwin para instalar pyaudio

En Linux, instala las dependencias del sistema mencionadas anteriormente

Verifica que los controladores de audio estén actualizados
