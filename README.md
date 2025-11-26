
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Supercar Voice System - Documentación</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Arial, sans-serif;
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a1a 50%, #2a2a2a 100%);
            color: #ffffff;
            line-height: 1.6;
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 40px 20px;
        }

        .header {
            text-align: center;
            margin-bottom: 60px;
            padding: 40px 0;
            background: linear-gradient(135deg, #ff1a1a 0%, #cc0000 100%);
            border-radius: 20px;
            position: relative;
            overflow: hidden;
        }

        .header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="grid" width="10" height="10" patternUnits="userSpaceOnUse"><path d="M 10 0 L 0 0 0 10" fill="none" stroke="rgba(255,255,255,0.1)" stroke-width="1"/></pattern></defs><rect width="100" height="100" fill="url(%23grid)"/></svg>');
        }

        .title {
            font-size: 3.5em;
            font-weight: 800;
            margin-bottom: 10px;
            text-shadow: 3px 3px 0px rgba(0,0,0,0.3);
            position: relative;
        }

        .subtitle {
            font-size: 1.4em;
            opacity: 0.9;
            font-weight: 300;
            position: relative;
        }

        .section {
            background: rgba(30, 30, 30, 0.8);
            border-radius: 15px;
            padding: 40px;
            margin-bottom: 30px;
            border: 1px solid #333;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .section:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 40px rgba(255, 26, 26, 0.2);
        }

        .section-title {
            font-size: 2em;
            color: #ff6666;
            margin-bottom: 25px;
            border-bottom: 2px solid #ff1a1a;
            padding-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .section-title i {
            font-size: 1.2em;
        }

        .feature-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
            margin-top: 20px;
        }

        .feature-card {
            background: rgba(255, 26, 26, 0.1);
            padding: 25px;
            border-radius: 12px;
            border: 1px solid #333;
            transition: all 0.3s ease;
        }

        .feature-card:hover {
            background: rgba(255, 26, 26, 0.2);
            border-color: #ff6666;
            transform: scale(1.02);
        }

        .feature-icon {
            font-size: 2.5em;
            margin-bottom: 15px;
        }

        .feature-title {
            font-size: 1.3em;
            color: #ff6666;
            margin-bottom: 10px;
            font-weight: 600;
        }

        .code-block {
            background: #1a1a1a;
            border: 1px solid #333;
            border-radius: 10px;
            padding: 25px;
            margin: 20px 0;
            overflow-x: auto;
            font-family: 'Courier New', monospace;
            position: relative;
        }

        .code-block::before {
            content: '📋';
            position: absolute;
            top: 10px;
            right: 15px;
            font-size: 1.2em;
            cursor: pointer;
        }

        .code-block code {
            color: #00ff00;
            font-size: 0.95em;
            line-height: 1.5;
        }

        .step {
            display: flex;
            align-items: flex-start;
            margin-bottom: 25px;
            padding: 20px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
            transition: background 0.3s ease;
        }

        .step:hover {
            background: rgba(255, 255, 255, 0.1);
        }

        .step-number {
            background: #ff1a1a;
            color: white;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            margin-right: 20px;
            flex-shrink: 0;
        }

        .step-content {
            flex: 1;
        }

        .car-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .car-card {
            background: rgba(255, 255, 255, 0.05);
            padding: 20px;
            border-radius: 10px;
            text-align: center;
            transition: all 0.3s ease;
            border: 1px solid #333;
        }

        .car-card:hover {
            background: rgba(255, 26, 26, 0.1);
            border-color: #ff6666;
            transform: translateY(-3px);
        }

        .car-icon {
            font-size: 2em;
            margin-bottom: 10px;
        }

        .warning-box {
            background: rgba(255, 165, 0, 0.1);
            border: 1px solid #ffa500;
            border-radius: 10px;
            padding: 20px;
            margin: 20px 0;
            position: relative;
        }

        .warning-box::before {
            content: '⚠️';
            position: absolute;
            top: 15px;
            left: 15px;
            font-size: 1.2em;
        }

        .warning-content {
            margin-left: 40px;
        }

        .troubleshooting-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .issue-card {
            background: rgba(255, 26, 26, 0.05);
            padding: 20px;
            border-radius: 10px;
            border-left: 4px solid #ff1a1a;
        }

        .issue-symptom {
            color: #ff6666;
            font-weight: 600;
            margin-bottom: 10px;
        }

        .solution-list {
            list-style-type: none;
            padding-left: 0;
        }

        .solution-list li {
            margin-bottom: 8px;
            padding-left: 25px;
            position: relative;
        }

        .solution-list li::before {
            content: '✅';
            position: absolute;
            left: 0;
        }

        @media (max-width: 768px) {
            .container {
                padding: 20px 15px;
            }
            
            .title {
                font-size: 2.5em;
            }
            
            .section {
                padding: 25px;
            }
            
            .feature-grid {
                grid-template-columns: 1fr;
            }
        }

        .text-justify {
            text-align: justify;
        }
    </style>
</head>
<body>
    <div class="container">
        <header class="header">
            <h1 class="title">🏎️ Supercar Voice System</h1>
            <p class="subtitle">Sistema de consulta por voz - Ultimate Edition</p>
        </header>

        <section class="section">
            <h2 class="section-title">🚀 Características Principales</h2>
            <div class="feature-grid">
                <div class="feature-card">
                    <div class="feature-icon">🎤</div>
                    <h3 class="feature-title">Reconocimiento de Voz</h3>
                    <p class="text-justify">Búsqueda avanzada por comandos de voz en español con tecnología de inteligencia artificial integrada para un reconocimiento preciso y natural.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🗂️</div>
                    <h3 class="feature-title">Base de Datos Integrada</h3>
                    <p class="text-justify">Acceso inmediato a información detallada de 13 superautos de alta gama con especificaciones técnicas completas y actualizadas.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🎨</div>
                    <h3 class="feature-title">Interfaz Moderna</h3>
                    <p class="text-justify">Diseño elegante con temática automovilística, animaciones fluidas y experiencia de usuario optimizada para máxima inmersión.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🔍</div>
                    <h3 class="feature-title">Búsqueda Múltiple</h3>
                    <p class="text-justify">Flexibilidad total con búsqueda por voz, texto tradicional y selección directa desde la lista interactiva de vehículos disponibles.</p>
                </div>
            </div>
        </section>

        <section class="section">
            <h2 class="section-title">📋 Requisitos del Sistema</h2>
            <div class="text-justify">
                <p>Para garantizar el funcionamiento óptimo del Supercar Voice System, asegúrese de que su sistema cumple con los siguientes requisitos mínimos:</p>
                
                <div class="feature-grid" style="margin-top: 25px;">
                    <div class="feature-card">
                        <div class="feature-icon">🐍</div>
                        <h3 class="feature-title">Python 3.7+</h3>
                        <p>Versión 3.7 o superior del intérprete de Python instalado y configurado correctamente en el PATH del sistema.</p>
                    </div>
                    <div class="feature-card">
                        <div class="feature-icon">🎙️</div>
                        <h3 class="feature-title">Micrófono</h3>
                        <p>Dispositivo de captura de audio funcional con permisos adecuados para aplicaciones de terceros.</p>
                    </div>
                    <div class="feature-card">
                        <div class="feature-icon">🌐</div>
                        <h3 class="feature-title">Conexión a Internet</h3>
                        <p>Conexión estable a internet para el servicio de reconocimiento de voz mediante Google Speech API.</p>
                    </div>
                </div>
            </div>
        </section>

        <section class="section">
            <h2 class="section-title">🔧 Instalación</h2>
            
            <div class="step">
                <div class="step-number">1</div>
                <div class="step-content">
                    <h3>Descargar el Proyecto</h3>
                    <p class="text-justify">Comience por obtener el código fuente del proyecto mediante clonación del repositorio o descarga directa del archivo principal.</p>
                    <div class="code-block">
                        <code>git clone &lt;url-del-repositorio&gt;<br>cd supercar-voice-system</code>
                    </div>
                </div>
            </div>

            <div class="step">
                <div class="step-number">2</div>
                <div class="step-content">
                    <h3>Crear Entorno Virtual (Recomendado)</h3>
                    <p class="text-justify">Aísle las dependencias del proyecto creando un entorno virtual que garantice la compatibilidad y evite conflictos con otras instalaciones.</p>
                    <div class="code-block">
                        <code># Windows<br>python -m venv venv<br>venv\Scripts\activate<br><br># Linux/Mac<br>python3 -m venv venv<br>source venv/bin/activate</code>
                    </div>
                </div>
            </div>

            <div class="step">
                <div class="step-number">3</div>
                <div class="step-content">
                    <h3>Instalar Dependencias</h3>
                    <p class="text-justify">Instale todas las librerías y paquetes necesarios para el correcto funcionamiento del sistema mediante el gestor de paquetes pip.</p>
                    <div class="code-block">
                        <code># Con archivo requirements.txt<br>pip install -r requirements.txt<br><br># Instalación manual<br>pip install PyQt5 speechrecognition pyaudio</code>
                    </div>
                </div>
            </div>

            <div class="warning-box">
                <div class="warning-content">
                    <h3>⚠️ Notas de Instalación Específicas</h3>
                    <p class="text-justify"><strong>Windows:</strong> Si experimenta problemas con pyaudio, utilice pipwin para una instalación más robusta:</p>
                    <div class="code-block">
                        <code>pip install pipwin<br>pipwin install pyaudio</code>
                    </div>
                    <p class="text-justify" style="margin-top: 10px;"><strong>Linux (Ubuntu/Debian):</strong> Instale las dependencias del sistema necesarias:</p>
                    <div class="code-block">
                        <code>sudo apt-get install python3-pyaudio portaudio19-dev</code>
                    </div>
                </div>
            </div>
        </section>

        <section class="section">
            <h2 class="section-title">🎯 Ejecución</h2>
            <p class="text-justify">Una vez completada la instalación, ejecute la aplicación principal utilizando el intérprete de Python. El sistema se inicializará automáticamente y estará listo para su uso inmediato.</p>
            <div class="code-block">
                <code>python BD4.py</code>
            </div>
            <p class="text-justify">La interfaz gráfica se cargará en segundos, presentando una pantalla principal con todos los controles y opciones disponibles para comenzar a explorar el mundo de los superautos.</p>
        </section>

        <section class="section">
            <h2 class="section-title">🎤 Uso del Sistema</h2>
            
            <div class="feature-grid">
                <div class="feature-card">
                    <div class="feature-icon">🎤</div>
                    <h3 class="feature-title">Búsqueda por Voz</h3>
                    <p class="text-justify"><strong>1.</strong> Haga clic en el botón "🎤 BUSCAR POR VOZ"<br>
                    <strong>2.</strong> Espere el mensaje de confirmación "Escuchando..."<br>
                    <strong>3.</strong> Pronuncie claramente el nombre del auto (ej: "ferrari 488 gtb")<br>
                    <strong>4.</strong> El sistema procesará y mostrará automáticamente la información</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">📝</div>
                    <h3 class="feature-title">Búsqueda por Texto</h3>
                    <p class="text-justify"><strong>1.</strong> Escriba el nombre completo o parcial en el campo de búsqueda<br>
                    <strong>2.</strong> Haga clic en "📝 BUSCAR POR TEXTO" o presione Enter<br>
                    <strong>3.</strong> La información se cargará instantáneamente en el panel principal</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">👆</div>
                    <h3 class="feature-title">Selección Directa</h3>
                    <p class="text-justify">Simplemente haga clic en cualquier auto de la lista desplegada para acceder inmediatamente a toda su información técnica detallada, incluyendo especificaciones de rendimiento y precio.</p>
                </div>
            </div>
        </section>

        <section class="section">
            <h2 class="section-title">🗂️ Autos Disponibles</h2>
            <p class="text-justify">El sistema incluye una base de datos completa con 13 de los superautos más exclusivos y tecnológicamente avanzados del mercado, cada uno con información técnica verificada y actualizada.</p>
            
            <div class="car-grid">
                <div class="car-card">
                    <div class="car-icon">🚗</div>
                    <h3>Ferrari 488 GTB</h3>
                </div>
                <div class="car-card">
                    <div class="car-icon">🚗</div>
                    <h3>Lamborghini Huracán Evo</h3>
                </div>
                <div class="car-card">
                    <div class="car-icon">🚗</div>
                    <h3>Bugatti Chiron</h3>
                </div>
                <div class="car-card">
                    <div class="car-icon">🚗</div>
                    <h3>McLaren P1</h3>
                </div>
                <div class="car-card">
                    <div class="car-icon">🚗</div>
                    <h3>Porsche 918 Spyder</h3>
                </div>
                <div class="car-card">
                    <div class="car-icon">🚗</div>
                    <h3>Koenigsegg Agera RS</h3>
                </div>
                <div class="car-card">
                    <div class="car-icon">🚗</div>
                    <h3>Pagani Huayra</h3>
                </div>
                <div class="car-card">
                    <div class="car-icon">🚗</div>
                    <h3>Aston Martin Valkyrie</h3>
                </div>
                <div class="car-card">
                    <div class="car-icon">🚗</div>
                    <h3>Rimac Nevera</h3>
                </div>
                <div class="car-card">
                    <div class="car-icon">🚗</div>
                    <h3>Ferrari SF90 Stradale</h3>
                </div>
                <div class="car-card">
                    <div class="car-icon">🚗</div>
                    <h3>Lamborghini Aventador SVJ</h3>
                </div>
                <div class="car-card">
                    <div class="car-icon">🚗</div>
                    <h3>Bugatti Divo</h3>
                </div>
                <div class="car-card">
                    <div class="car-icon">🚗</div>
                    <h3>Maserati MC20</h3>
                </div>
            </div>
            
            <p class="text-justify" style="margin-top: 20px;">Cada vehículo incluye información completa sobre: marca, modelo específico, año de fabricación, velocidad máxima alcanzable, tiempo de aceleración de 0 a 100 km/h, y precio estimado en el mercado actual.</p>
        </section>

        <section class="section">
            <h2 class="section-title">🛠️ Solución de Problemas</h2>
            
            <div class="troubleshooting-grid">
                <div class="issue-card">
                    <div class="issue-symptom">Error de Micrófono</div>
                    <ul class="solution-list">
                        <li>Verifique que el micrófono esté físicamente conectado y funcionando</li>
                        <li>Revise los permisos de la aplicación para acceso al micrófono</li>
                        <li>Pruebe en un entorno con menor ruido ambiental</li>
                        <li>Reinicie la aplicación y vuelva a intentar</li>
                    </ul>
                </div>
                
                <div class="issue-card">
                    <div class="issue-symptom">Error de Reconocimiento</div>
                    <ul class="solution-list">
                        <li>Hable claramente y mantenga un ritmo de pronunciación normal</li>
                        <li>Utilice nombres completos (marca + modelo) para mejor precisión</li>
                        <li>Verifique que su conexión a internet esté activa y estable</li>
                        <li>Espere entre frases para permitir un procesamiento adecuado</li>
                    </ul>
                </div>
                
                <div class="issue-card">
                    <div class="issue-symptom">La aplicación no inicia</div>
                    <ul class="solution-list">
                        <li>Asegúrese de tener Python 3.7 o superior instalado</li>
                        <li>Verifique que todas las dependencias estén correctamente instaladas</li>
                        <li>Ejecute desde línea de comandos para ver mensajes de error específicos</li>
                        <li>Confirme que el archivo BD4.py esté completo y sin corrupciones</li>
                    </ul>
                </div>
                
                <div class="issue-card">
                    <div class="issue-symptom">Problemas de Rendimiento</div>
                    <ul class="solution-list">
                        <li>Cierre otras aplicaciones que consuman recursos del sistema</li>
                        <li>Verifique que tenga al menos 4GB de RAM disponibles</li>
                        <li>Reinicie la aplicación periódicamente durante sesiones prolongadas</li>
                        <li>Actualice los controladores de audio y gráficos</li>
                    </ul>
                </div>
            </div>
        </section>

        <section class="section">
            <h2 class="section-title">📞 Soporte</h2>
            <p class="text-justify">Si después de seguir todas las indicaciones anteriores continúa experimentando problemas técnicos o tiene sugerencias para mejorar el sistema, no dude en contactar a nuestro equipo de desarrollo especializado. Proporcione la mayor cantidad de detalles posible sobre el problema encontrado, incluyendo mensajes de error específicos, configuración de su sistema y pasos exactos para reproducir el incidente.</p>
            <p class="text-justify" style="margin-top: 15px;">Nuestro compromiso es garantizar la mejor experiencia posible con el Supercar Voice System y valoramos enormemente los comentarios de nuestra comunidad de usuarios para continuar mejorando y expandiendo las capacidades de la plataforma.</p>
        </section>
    </div>

    <script>
        // Efecto de copiado para los bloques de código
        document.querySelectorAll('.code-block').forEach(block => {
            block.addEventListener('click', function() {
                const code = this.querySelector('code').textContent;
                navigator.clipboard.writeText(code).then(() => {
                    const originalContent = this.innerHTML;
                    this.innerHTML = '✅ ¡Copiado al portapapeles!';
                    setTimeout(() => {
                        this.innerHTML = originalContent;
                    }, 2000);
                });
            });
        });

        // Efecto de scroll suave
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
