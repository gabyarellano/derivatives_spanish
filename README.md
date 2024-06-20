# <span style="color:rgb(213,80,0)">Cálculo: Derivadas</span>

[![Ver en File Exchange](https://www.mathworks.com/matlabcentral/images/matlab-file-exchange.svg)](https://www.mathworks.com/matlabcentral/fileexchange/99249-calculus-derivatives) o [![Abrir en MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=MathWorks-Teaching-Resources/Calculus-Derivatives&project=Derivatives.prj)

![Versiones de MATLAB Probadas](https://img.shields.io/endpoint?url=https%3A%2F%2Fraw.githubusercontent.com%2FMathWorks-Teaching-Resources%2FCalculus-Derivatives%2Frelease%2FImages%2FTestedWith.json)

**Módulo Curricular**

_Creado con R2021a. Compatible con R2021a y versiones posteriores._

# Información

Este módulo curricular contiene [scripts interactivos de MATLAB®](https://www.mathworks.com/products/matlab/live-editor.html) que enseñan conceptos fundamentales y terminología básica relacionada con el cálculo de derivadas. Se enfoca en la aproximación numérica y la representación gráfica como herramientas para entender los conceptos de cálculo.

## Antecedentes

Puedes usar estos scripts interactivos como demostraciones en clases, actividades de clase o asignaciones interactivas fuera de clase. El módulo de derivadas se divide en cinco scripts y una aplicación de práctica. El primero cubre la [definición límite de la derivada](#H_727F8117) e incluye varios ejemplos motivadores para el estudio de derivadas. El segundo cubre [derivadas de potencias y la linealidad de las derivadas](#H_77AFFCCB) trabajando desde la definición límite de la derivada, incluyendo una aplicación al movimiento parabólico. El tercero cubre [derivadas de exponenciales, logaritmos naturales, senos y cosenos](#H_9F419170) así como la discusión sobre derivadas de orden superior. Las aplicaciones incluyen crecimiento poblacional y comportamiento oscilatorio. El cuarto script presenta visualizaciones de [la regla del producto y la regla de la cadena para derivadas](#H_DBF5C0DF) así como problemas de práctica generados aleatoriamente. Las aplicaciones incluyen tasas relacionadas y la regla del cociente para derivadas. El quinto script presenta [aproximación de funciones diferenciables](#H_98D870A0) por polinomios, incluyendo líneas tangentes, y conduciendo a polinomios de Taylor. La [aplicación Calculus Flashcards](#H_A8913F44) permite a los usuarios seleccionar los tipos de reglas de derivada (o integral) que deseen practicar, generar problemas aleatorios y rastrear su progreso dentro de una sesión.


Las instrucciones dentro de los scripts interactivos te guiarán a través de los ejercicios y actividades. Todos los ejercicios interactivos ofrecen retroalimentación mientras que las preguntas de reflexión son más abiertas y no incluyen soluciones en este módulo. Comienza con cada script interactivo ejecutándolo una sección a la vez. Para detener la ejecución del script o una sección a mitad de camino (por ejemplo, cuando una animación está en progreso), usa el botón <img src="Images/EndIcon.png" width="19" alt="EndIcon.png"> **Detener** en la sección **EJECUTAR** de la pestaña **Live Editor** en la barra de herramientas de MATLAB.

## Contáctanos

Las soluciones están disponibles a petición del instructor. Contacta al equipo de recursos didácticos de MathWorks si deseas solicitar soluciones, proporcionar comentarios o si tienes alguna pregunta.

<a name="H_30BC7141"></a>

## Prerrequisitos

Matemáticamente, este módulo asume un conocimiento de funciones que es estándar en los materiales de curso de precálculo con respecto a potencias, exponenciales, valores absolutos, logaritmos, senos, cosenos, funciones racionales y asíntotas. Además, este módulo asume fluidez básica con límites al discutir la definición límite de la derivada.

Se requiere una fluidez mínima con MATLAB para usar este módulo; principalmente es matemáticas tipo calculadora estándar como usar \texttt{*} para multiplicación y <samp>/</samp> para división. Para comandos que van más allá de interactuar con una calculadora, el conocimiento necesario está incluido en el módulo. Si quieres mejorar tu conocimiento de MATLAB, [MATLAB Onramp](https://matlabacademy.mathworks.com/details/matlab-onramp/gettingstarted) es un tutorial introductorio gratuito de dos horas que enseña los aspectos esenciales de MATLAB.

<a name="H_330E72C3"></a>
## Cómo empezar
### Accediendo al Módulo
### **En MATLAB Online:**

Usa el enlace [<img src="Images/OpenInMO.png" width="136" alt="OpenInMO.png">](https://matlab.mathworks.com/open/github/v1?repo=MathWorks-Teaching-Resources/Calculus-Derivatives&project=Derivatives.prj) para descargar el módulo. Se te pedirá iniciar sesión o crear una cuenta de MathWorks. El proyecto se cargará, y verás una aplicación con varias opciones de navegación para comenzar.

### **En Escritorio:**

Descarga o clona este repositorio. Abre MATLAB, navega a la carpeta que contiene estos scripts y haz doble clic en [Derivatives.prj](https://matlab.mathworks.com/open/github/v1?repo=MathWorks-Teaching-Resources/Calculus-Derivatives&project=Derivatives.prj). Esto agregará los archivos apropiados a tu ruta de MATLAB y abrirá una aplicación que te preguntará por dónde te gustaría comenzar.

Asegúrate de tener todos los productos ([listados a continuación](#H_E850B4FF)) instalados. Si necesitas incluir un producto, agrégalo usando el Explorador de Complementos. Para instalar un complemento, ve a la pestaña **Inicio** y selecciona <img src="Images/AddOnsIcon.png" width="16" alt="AddOnsIcon.png"> **Complementos** > **Obtener Complementos**.

<a name="H_E850B4FF"></a>
## Productos

MATLAB® y Symbolic Math Toolbox™ se utilizan a lo largo. Herramientas del Curve Fitting Toolbox™ se utilizan en <samp>TranscendentalsRules.mlx</samp>.

<a name="H_E8C62B23"></a>
# Scripts
<a name="H_727F8117"></a>
## [La Definición de la Derivada](https://matlab.mathworks.com/open/github/v1?repo=MathWorks-Teaching-Resources/Calculus-Derivatives&project=Derivatives.prj&file=Definition.mlx)
| **<samp>Definition.mlx</samp>** | **En este script, los estudiantes...**  |
| :-- | :-- |
| <img src="https://github.com/MathWorks-Teaching-Resources/Calculus-Derivatives/blob/release/Images/SecantTangent2.gif" width="171" alt="Líneas secantes"> |-  explicarán la definición límite de la derivada y su relación con las líneas secantes. <br>-  identificarán el signo de la derivada en un punto como positivo, negativo o cero basado en el gráfico de una función. <br>-  identificarán puntos donde la derivada de una función continua no existe y explicarán por qué con referencia a la definición de la derivada. <br>-  reconocerán $f^{\prime } (x)$ , $\frac{\textrm{d}f}{\textrm{d}x}$ , y $\frac{\textrm{d}}{\textrm{d}x}\left\lbrack f(x)\right\rbrack$ como notación equivalente para la derivada de $f$ con respecto a $x$ .  |

<a name="H_77AFFCCB"></a>
## [Derivadas de Polinomios](https://matlab.mathworks.com/open/github/v1?repo=MathWorks-Teaching-Resources/Calculus-Derivatives&project=Derivatives.prj&file=PowerRules.mlx)
| **<samp>PowerRules.mlx</samp>** | **En este script, los estudiantes...**  |
| :-- | :-- |
| <img src="Images/image_4.png" width="171" alt="image_4.png"> |-  explicarán por qué la definición límite de la derivada resulta en la regla de potencia para derivadas. <br>-  calcularán las derivadas de combinaciones lineales de potencias a mano. <br>-  aplicarán derivadas para resolver preguntas prácticas.  |

<a name="H_9F419170"></a>
## [Derivadas de Funciones Trascendentales](https://matlab.mathworks.com/open/github/v1?repo=MathWorks-Teaching-Resources/Calculus-Derivatives&project=Derivatives.prj&file=TranscendentalsRules.mlx)
| **<samp>TranscendentalsRules.mlx</samp>** | **En este script, los estudiantes...**  |
| :-- | :-- |
| <img src="https://github.com/MathWorks-Teaching-Resources/Calculus-Derivatives/blob/release/Images/DerivativeOfSine.png" width="171" alt="Derivada numérica del seno"> |-  determinarán la relación funcional de las derivadas de senos, cosenos, exponenciales y logaritmos naturales. <br>-  explicarán el patrón en las derivadas de $\sin (ax)$ , $\cos (ax)$ , y $\exp (ax)$ para valores constantes de $a$ y que la derivada de $\ln (ax)$ no sigue el patrón simple. <br>-  aplicarán las unidades correctas a derivadas de cualquier orden. <br>-  explorarán ecuaciones diferenciales simples de primer y segundo orden que describen un sistema físico y las usarán para crear modelos matemáticos del sistema.  |

<a name="H_DBF5C0DF"></a>
## [Regla de la Cadena y Regla del Producto](https://matlab.mathworks.com/open/github/v1?repo=MathWorks-Teaching-Resources/Calculus-Derivatives&project=Derivatives.prj&file=TranscendentalsRules.mlx)
| **<samp>CombinationRules.mlx</samp>** | **En este script, los estudiantes...**  |
| :-- | :-- |
| <img src="https://github.com/MathWorks-Teaching-Resources/Calculus-Derivatives/blob/release/Images/productRuleIcon.png" width="171" alt="regla del producto"> |-  explicarán por qué la regla de la cadena es $\frac{\textrm{d}}{\textrm{d}x}\left\lbrack f(g(x))\right\rbrack =f^{\prime } (g(x)) \cdot g^{\prime } (x)$ . <br>-  aplicarán la regla de la cadena para calcular derivadas. <br>-  explicarán por qué la regla del producto es $\frac{\textrm{d}}{\textrm{d}x}\left\lbrack f(x)\cdot g(x)\right\rbrack =f(x)\cdot \frac{\textrm{d}g}{\textrm{d}x}+\frac{\textrm{d}f}{\textrm{d}x}\cdot g(x)$ . <br>-  aplicarán la regla del producto para calcular derivadas. <br>-  practicarán el reconocimiento y la aplicación fluida de las reglas para calcular derivadas.  |

<a name="H_98D870A0"></a>
## [Polinomios de Taylor](https://matlab.mathworks.com/open/github/v1?repo=MathWorks-Teaching-Resources/Calculus-Derivatives&project=Derivatives.prj&file=TaylorPolynomials.mlx)
| **<samp>TaylorPolynomials.mlx</samp>** | **En este script, los estudiantes...**  |
| :-- | :-- |
| <img src="Images/taylorpolyexample.gif" width="171" alt="animación de aproximación de polinomio de Taylor"> |-  calcularán líneas tangentes. <br>-  calcularán aproximaciones cuadráticas. <br>-  calcularán aproximaciones polinomiales de orden superior.  |

<a name="H_A8913F44"></a>
# App: [Tarjetas Educativas de Cálculo](https://matlab.mathworks.com/open/github/v1?repo=MathWorks-Teaching-Resources/Calculus-Derivatives&project=Derivatives.prj&file=CalculusFlashcards)

Practica el reconocimiento y la resolución de problemas computacionales estándar en cálculo.

<p style="text-align:left"><img src="Images/image_8.png" width="371" alt="image_8.png"></p>
<a name="H_F61733D7"></a>
# Licencia

La licencia para este módulo está disponible en el archivo [LICENSE.md](https://github.com/MathWorks-Teaching-Resources/Calculus-Derivatives/blob/release/LICENSE.md).

# Módulos de Material Didáctico Relacionados
| **Módulo de Material Didáctico** | **Contenido de Muestra** | **Disponible en:**  |
| :-- | :-- | :-- |
| [**Cálculo: Integrales**](https://www.mathworks.com/matlabcentral/fileexchange/105740-calculus-integrals) | <img src="Images/image_9.png" width="171" alt="image_9.png"> | [<img src="Images/OpenInFX.png" width="91" alt="OpenInFX.png">](https://www.mathworks.com/matlabcentral/fileexchange/105740-calculus-integrals)<br>[<img src="Images/OpenInMO.png" width="136" alt="OpenInMO.png">](https://matlab.mathworks.com/open/github/v1?repo=MathWorks-Teaching-Resources/Calculus-Integrals&project=Integrals.prj)<br> [GitHub](https://github.com/MathWorks-Teaching-Resources/Calculus-Integrals)   |
| [**Análisis de Fourier**](https://www.mathworks.com/matlabcentral/fileexchange/106725-fourier-analysis) | <img src="Images/image_12.png" width="171" alt="image_12.png"> | [<img src="Images/OpenInFX.png" width="91" alt="OpenInFX.png">](https://www.mathworks.com/matlabcentral/fileexchange/106725-fourier-analysis)<br>[<img src="Images/OpenInMO.png" width="136" alt="OpenInMO.png">](https://matlab.mathworks.com/open/github/v1?repo=MathWorks-Teaching-Resources/Fourier-Analysis&project=FourierAnalysis.prj)<br>[GitHub](https://github.com/MathWorks-Teaching-Resources/Fourier-Analysis)  |
| <br>[**Métodos Numéricos con Aplicaciones**](https://www.mathworks.com/matlabcentral/fileexchange/111490-numerical-methods-with-applications) | <img src="Images/image_15.png" width="171" alt="image_15.png"> | <br>[<img src="Images/OpenInFX.png" width="91" alt="OpenInFX.png">](https://www.mathworks.com/matlabcentral/fileexchange/111490-numerical-methods-with-applications)<br>[<img src="Images/OpenInMO.png" width="136" alt="OpenInMO.png">](https://matlab.mathworks.com/open/github/v1?repo=MathWorks-Teaching-Resources/Numerical-Methods-with-Applications&project=NumericalMethods.prj)  <br>[GitHub](https://github.com/MathWorks-Teaching-Resources/Numerical-Methods-with-Applications)   |


O siéntase libre de explorar nuestro otro [contenido modular de material didáctico](https://www.mathworks.com/matlabcentral/fileexchange/?q=tag%3A%22courseware+module%22&sort=downloads_desc_30d).

# Recursos para Educadores
-  [Página para Educadores](https://www.mathworks.com/academia/educators.html) 
<a name="H_0FA5DA18"></a>
# Contribuir 

¿Buscas más? ¿Encontraste un problema? ¿Tienes una sugerencia? Por favor, contacta al [equipo de recursos didácticos de MathWorks](mailto:%20onlineteaching@mathworks.com). Si deseas contribuir directamente a este proyecto, puedes encontrar información sobre cómo hacerlo en la página [CONTRIBUTING.md](https://github.com/MathWorks-Teaching-Resources/Calculus-Derivatives/blob/release/CONTRIBUTING.md) en GitHub.


 *©* Derechos de autor 2023 The MathWorks™, Inc