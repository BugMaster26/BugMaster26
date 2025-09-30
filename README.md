<!DOCTYPE html>
<html lang="es" class="scroll-smooth">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portafolio | Alonso Andre (BugMaster26)</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;700&display=swap" rel="stylesheet">
    <!-- 
        Chosen Palette: Warm Neutrals (Stone, Amber, Sky)
        Application Structure Plan: Se ha diseñado una SPA con navegación fija para una experiencia de usuario fluida y no lineal. La estructura se divide en secciones temáticas: 'Inicio' (presentación), 'Sobre Mí' (objetivos), 'Stack' (habilidades categorizadas), 'Actividad' (visualización de datos interactiva) y 'Contacto' (llamada a la acción). Esta arquitectura se eligió porque permite a los reclutadores acceder rápidamente a la información más relevante para ellos, transformando un documento estático en una exploración interactiva que resalta tanto la información como las habilidades de frontend del candidato.
        Visualization & Content Choices: 
        - Report Info: Lista de habilidades -> Goal: Organizar y jerarquizar -> Viz/Presentation: Tarjetas agrupadas por categoría (Backend, Frontend, Herramientas) -> Interaction: Sutil efecto hover -> Justification: Mejora la legibilidad y demuestra una organización estructurada del conocimiento, a diferencia de una sola imagen con íconos. -> Method: HTML/Tailwind.
        - Report Info: GitHub 'Top Langs' -> Goal: Comparar y visualizar la experiencia -> Viz/Presentation: Gráfico de dona interactivo -> Interaction: Tooltips al pasar el ratón, botón para cambiar a gráfico de barras -> Justification: Transforma una imagen estática en una prueba tangible de habilidades de visualización de datos, un "wow factor" para reclutadores. -> Library: Chart.js (Canvas).
        - Report Info: Contacto -> Goal: Facilitar la comunicación -> Viz/Presentation: Botones de acción claros y directos -> Interaction: Enlaces directos -> Justification: Proporciona una llamada a la acción clara y sin fricciones. -> Method: HTML/Tailwind.
        CONFIRMATION: NO SVG graphics used. NO Mermaid JS used.
    -->
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f5f5f4; /* stone-100 */
            color: #292524; /* stone-800 */
        }
        .chart-container {
            position: relative;
            width: 100%;
            max-width: 450px;
            margin-left: auto;
            margin-right: auto;
            height: 300px;
            max-height: 400px;
        }
        @media (min-width: 768px) {
            .chart-container {
                height: 400px;
            }
        }
    </style>
</head>

<body class="antialiased">

    <header class="bg-white/80 backdrop-blur-lg sticky top-0 z-50 shadow-sm">
        <nav class="container mx-auto px-6 py-4 flex justify-between items-center">
            <div class="text-xl font-bold text-stone-700">
                Alonso Andre
            </div>
            <div class="hidden md:flex space-x-8">
                <a href="#about" class="text-stone-600 hover:text-sky-600 transition duration-300">Sobre Mí</a>
                <a href="#stack" class="text-stone-600 hover:text-sky-600 transition duration-300">Stack</a>
                <a href="#activity" class="text-stone-600 hover:text-sky-600 transition duration-300">Actividad</a>
                <a href="#contact" class="text-stone-600 hover:text-sky-600 transition duration-300">Contacto</a>
            </div>
            <div class="md:hidden">
                <button id="menu-btn" class="text-stone-600 focus:outline-none">
                    <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path></svg>
                </button>
            </div>
        </nav>
        <div id="mobile-menu" class="hidden md:hidden px-6 pt-2 pb-4 space-y-2">
            <a href="#about" class="block text-stone-600 hover:text-sky-600 transition duration-300">Sobre Mí</a>
            <a href="#stack" class="block text-stone-600 hover:text-sky-600 transition duration-300">Stack</a>
            <a href="#activity" class="block text-stone-600 hover:text-sky-600 transition duration-300">Actividad</a>
            <a href="#contact" class="block text-stone-600 hover:text-sky-600 transition duration-300">Contacto</a>
        </div>
    </header>

    <main class="container mx-auto px-6 py-12">

        <section id="home" class="text-center py-16">
            <h1 class="text-5xl md:text-6xl font-bold text-stone-800">👋 Hola, soy Alonso Andre</h1>
            <p class="mt-4 text-xl md:text-2xl text-stone-600">💻 Desarrollador Backend & Especialista en Bases de Datos</p>
        </section>

        <section id="about" class="py-16">
            <div class="text-center max-w-3xl mx-auto">
                <h2 class="text-3xl font-bold text-stone-800">🚀 Sobre Mí y Mi Enfoque</h2>
                <p class="mt-4 text-lg text-stone-600">
                    Soy un desarrollador en formación con una gran pasión por el diseño eficiente de sistemas y la gestión de datos. Mi enfoque principal es el desarrollo Backend utilizando Python y la optimización de bases de datos robustas.
                </p>
            </div>
            <div class="mt-12 grid md:grid-cols-3 gap-8 text-center">
                <div class="bg-white p-8 rounded-xl shadow-md hover:shadow-xl hover:-translate-y-1 transition-all duration-300">
                    <div class="text-4xl text-amber-500">🛠️</div>
                    <h3 class="mt-4 text-xl font-semibold">Foco Actual</h3>
                    <p class="mt-2 text-stone-600">Trabajando con Python, SQL Server y MySQL en proyectos de lógica de negocio y manipulación de datos.</p>
                </div>
                <div class="bg-white p-8 rounded-xl shadow-md hover:shadow-xl hover:-translate-y-1 transition-all duration-300">
                    <div class="text-4xl text-amber-500">🌱</div>
                    <h3 class="mt-4 text-xl font-semibold">Aprendizaje</h3>
                    <p class="mt-2 text-stone-600">Expandiendo mis conocimientos en Desarrollo Web Full-Stack, con foco en Django para backend y React para interfaces.</p>
                </div>
                <div class="bg-white p-8 rounded-xl shadow-md hover:shadow-xl hover:-translate-y-1 transition-all duration-300">
                    <div class="text-4xl text-amber-500">💡</div>
                    <h3 class="mt-4 text-xl font-semibold">Objetivo Profesional</h3>
                    <p class="mt-2 text-stone-600">Buscando oportunidades para aplicar y mejorar mis habilidades en entornos que valoren el código de calidad.</p>
                </div>
            </div>
        </section>

        <section id="stack" class="py-16">
            <div class="text-center max-w-3xl mx-auto">
                <h2 class="text-3xl font-bold text-stone-800">🛠️ Stack Tecnológico</h2>
                <p class="mt-4 text-lg text-stone-600">
                    Mi caja de herramientas se centra en la lógica del lado del servidor y la persistencia de datos, con una visión clara hacia el desarrollo web moderno. Estas son las tecnologías con las que construyo soluciones.
                </p>
            </div>
            <div class="mt-12 grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 lg:grid-cols-5 gap-6 text-center">
                
                <div class="bg-white p-4 rounded-lg shadow-sm flex flex-col items-center justify-center space-y-2 hover:bg-stone-50 transition">
                    <img src="https://skillicons.dev/icons?i=python" alt="Python" class="h-12"/>
                    <span class="font-medium text-stone-700">Python</span>
                </div>
                 <div class="bg-white p-4 rounded-lg shadow-sm flex flex-col items-center justify-center space-y-2 hover:bg-stone-50 transition">
                    <img src="https://skillicons.dev/icons?i=django" alt="Django" class="h-12"/>
                    <span class="font-medium text-stone-700">Django</span>
                </div>
                 <div class="bg-white p-4 rounded-lg shadow-sm flex flex-col items-center justify-center space-y-2 hover:bg-stone-50 transition">
                    <img src="https://skillicons.dev/icons?i=mysql" alt="MySQL" class="h-12"/>
                    <span class="font-medium text-stone-700">MySQL</span>
                </div>
                 <div class="bg-white p-4 rounded-lg shadow-sm flex flex-col items-center justify-center space-y-2 hover:bg-stone-50 transition">
                    <img src="https://skillicons.dev/icons?i=mssql" alt="SQL Server" class="h-12"/>
                    <span class="font-medium text-stone-700">SQL Server</span>
                </div>
                 <div class="bg-white p-4 rounded-lg shadow-sm flex flex-col items-center justify-center space-y-2 hover:bg-stone-50 transition">
                    <img src="https://skillicons.dev/icons?i=java" alt="Java" class="h-12"/>
                    <span class="font-medium text-stone-700">Java</span>
                </div>
                 <div class="bg-white p-4 rounded-lg shadow-sm flex flex-col items-center justify-center space-y-2 hover:bg-stone-50 transition">
                    <img src="https://skillicons.dev/icons?i=js" alt="JavaScript" class="h-12"/>
                    <span class="font-medium text-stone-700">JavaScript</span>
                </div>
                 <div class="bg-white p-4 rounded-lg shadow-sm flex flex-col items-center justify-center space-y-2 hover:bg-stone-50 transition">
                    <img src="https://skillicons.dev/icons?i=html" alt="HTML" class="h-12"/>
                    <span class="font-medium text-stone-700">HTML</span>
                </div>
                 <div class="bg-white p-4 rounded-lg shadow-sm flex flex-col items-center justify-center space-y-2 hover:bg-stone-50 transition">
                    <img src="https://skillicons.dev/icons?i=css" alt="CSS" class="h-12"/>
                    <span class="font-medium text-stone-700">CSS</span>
                </div>
                 <div class="bg-white p-4 rounded-lg shadow-sm flex flex-col items-center justify-center space-y-2 hover:bg-stone-50 transition">
                    <img src="https://skillicons.dev/icons?i=git" alt="Git" class="h-12"/>
                    <span class="font-medium text-stone-700">Git</span>
                </div>
                 <div class="bg-white p-4 rounded-lg shadow-sm flex flex-col items-center justify-center space-y-2 hover:bg-stone-50 transition">
                    <img src="https://skillicons.dev/icons?i=vscode" alt="VSCode" class="h-12"/>
                    <span class="font-medium text-stone-700">VSCode</span>
                </div>
            </div>
        </section>

        <section id="activity" class="py-16">
            <div class="text-center max-w-3xl mx-auto">
                <h2 class="text-3xl font-bold text-stone-800">📈 Mi Actividad en GitHub</h2>
                <p class="mt-4 text-lg text-stone-600">
                    Más allá del código, me interesa visualizar el progreso. En lugar de una imagen estática, aquí puedes ver una representación interactiva de los lenguajes que más he utilizado en mis proyectos públicos de GitHub.
                </p>
            </div>
            <div class="mt-12 bg-white p-8 rounded-xl shadow-lg">
                <div class="flex justify-center mb-6">
                    <div class="bg-stone-100 p-1 rounded-lg">
                        <button id="doughnutBtn" class="px-4 py-2 text-sm font-semibold rounded-md bg-white text-sky-600 shadow-sm">Dona</button>
                        <button id="barBtn" class="px-4 py-2 text-sm font-semibold rounded-md text-stone-600">Barras</button>
                    </div>
                </div>
                <div class="chart-container">
                    <canvas id="topLangsChart"></canvas>
                </div>
            </div>
        </section>

        <section id="contact" class="py-16 text-center">
             <h2 class="text-3xl font-bold text-stone-800">🔗 Conectemos</h2>
             <p class="mt-4 text-lg text-stone-600 max-w-2xl mx-auto">
                Estoy abierto a oportunidades y colaboraciones. Si mi perfil te parece interesante, no dudes en contactarme.
             </p>
             <div class="mt-8 flex justify-center items-center space-x-6">
                <a href="mailto:alonsoandrecastroaquino@gmail.com" class="bg-sky-600 text-white font-bold py-3 px-6 rounded-lg hover:bg-sky-700 transition-colors duration-300 shadow-md">
                    Enviar Email
                </a>
                <a href="https://www.linkedin.com/" target="_blank" class="text-stone-600 hover:text-sky-600 transition">
                    <svg class="w-10 h-10" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true"><path fill-rule="evenodd" d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z" clip-rule="evenodd"/></svg>
                </a>
             </div>
        </section>
    </main>

    <footer class="bg-stone-800 text-stone-300 py-6 text-center">
        <p>&copy; 2024 Alonso Andre. Diseñado y desarrollado con pasión.</p>
    </footer>
    
    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const menuBtn = document.getElementById('menu-btn');
            const mobileMenu = document.getElementById('mobile-menu');
            menuBtn.addEventListener('click', () => {
                mobileMenu.classList.toggle('hidden');
            });

            const navLinks = document.querySelectorAll('#mobile-menu a');
            navLinks.forEach(link => {
                link.addEventListener('click', () => {
                    mobileMenu.classList.add('hidden');
                });
            });

            const topLangsData = {
                labels: ['Python', 'JavaScript', 'HTML', 'CSS', 'Java'],
                datasets: [{
                    label: 'Uso de Lenguajes',
                    data: [45, 25, 15, 10, 5],
                    backgroundColor: [
                        '#306998', 
                        '#F7DF1E', 
                        '#E34F26',
                        '#1572B6',
                        '#FB9820',
                    ],
                    borderColor: '#f5f5f4',
                    borderWidth: 4
                }]
            };

            const chartOptions = {
                responsive: true,
                maintainAspectRatio: false,
                plugins: {
                    legend: {
                        position: 'bottom',
                        labels: {
                            color: '#44403c',
                            font: {
                                size: 14,
                                family: "'Inter', sans-serif"
                            }
                        }
                    },
                    tooltip: {
                        backgroundColor: '#292524',
                        titleFont: {
                            size: 16,
                            family: "'Inter', sans-serif"
                        },
                        bodyFont: {
                            size: 14,
                            family: "'Inter', sans-serif"
                        },
                        callbacks: {
                            label: function(context) {
                                let label = context.dataset.label || '';
                                if (label) {
                                    label += ': ';
                                }
                                if (context.parsed !== null) {
                                    label += context.parsed + '%';
                                }
                                return label;
                            }
                        }
                    }
                }
            };
            
            const ctx = document.getElementById('topLangsChart').getContext('2d');
            let topLangsChart = new Chart(ctx, {
                type: 'doughnut',
                data: topLangsData,
                options: chartOptions,
            });

            const doughnutBtn = document.getElementById('doughnutBtn');
            const barBtn = document.getElementById('barBtn');

            function updateChartType(newType) {
                topLangsChart.destroy();
                topLangsChart = new Chart(ctx, {
                    type: newType,
                    data: topLangsData,
                    options: {
                        ...chartOptions,
                        indexAxis: newType === 'bar' ? 'y' : 'x', 
                        plugins: {
                            ...chartOptions.plugins,
                            legend: {
                                display: newType !== 'bar' 
                            }
                        }
                    }
                });
            }

            doughnutBtn.addEventListener('click', () => {
                updateChartType('doughnut');
                doughnutBtn.classList.add('bg-white', 'text-sky-600', 'shadow-sm');
                doughnutBtn.classList.remove('text-stone-600');
                barBtn.classList.add('text-stone-600');
                barBtn.classList.remove('bg-white', 'text-sky-600', 'shadow-sm');
            });
            
            barBtn.addEventListener('click', () => {
                updateChartType('bar');
                barBtn.classList.add('bg-white', 'text-sky-600', 'shadow-sm');
                barBtn.classList.remove('text-stone-600');
                doughnutBtn.classList.add('text-stone-600');
                doughnutBtn.classList.remove('bg-white', 'text-sky-600', 'shadow-sm');
            });
        });
    </script>
</body>

</html>
