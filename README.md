# Evaluador y Validador Postfijo con Autómata de Pila

Herramienta académica para **validar** y **evaluar** expresiones en **notación postfija (RPN)** utilizando los conceptos de **Autómata de Pila (PDA)**. Incluye verificación léxica/sintáctica básica, reporte de errores y ejemplos de uso.

> Proyecto creado para fines didácticos en cursos de Autómatas/Lenguajes Formales y Estructuras de Datos.

---

## ✨ Características

- ✅ **Valida** que una cadena postfija sea correctamente formada (operadores/operandos y balance de pila).
- ➕ **Evalúa** la expresión postfija y devuelve el resultado numérico.
- 🧠 **Modelo PDA** documentado: estados, alfabeto de entrada, alfabeto de pila y transiciones.
- 🧪 **Casos de prueba** incluidos para expresiones válidas e inválidas.
- 📝 **Mensajes de error** claros (símbolo desconocido, falta de operandos, pila no vacía al final, etc.).

---

## 📦 Requisitos

<!-- Ajusta según tu implementación -->
- <!-- TODO: Cambia si no es Java --> **Java 17+** (o superior)
- **Maven/Gradle** (opcional si usas build)
- Sistema operativo: Windows, macOS o Linux

> Si tu proyecto está en otro lenguaje, edita esta sección (por ejemplo: Python 3.11, g++/CMake, etc.).

---

## 🚀 Instalación y ejecución

### Opción A — Compilar y ejecutar (Java)

```bash
# Clonar el repositorio
git clone https://github.com/PaoloVM27/Evaluador-y-Validador-Postfijo-con-Automata-de-Pila.git
cd Evaluador-y-Validador-Postfijo-con-Automata-de-Pila

# Compilar (Maven)
mvn -q package

# Ejecutar (reemplaza MainClass por tu clase principal)
java -cp target/*.jar MainClass
