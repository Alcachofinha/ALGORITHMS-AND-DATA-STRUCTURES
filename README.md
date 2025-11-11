# Postfix Evaluator and Validator using Pushdown Automaton (PDA)

Este proyecto implementa y visualiza la evaluación de expresiones en **Notación Polaca Inversa (RPN / Postfija)** utilizando un **Autómata de Pila (PDA)**. Demuestra cómo un PDA puede validar la estructura de una expresión y calcular su resultado si es correcta. Incluye interfaz web con **HTML/CSS/JS** y un núcleo de evaluación en **WebAssembly (WASM)** generado desde **C++**.

---

## 🎯 Objetivo del Proyecto

- Mostrar el funcionamiento interno de un **PDA** evaluador de expresiones postfijas.
- Representar claramente la **pila** durante el proceso.
- **Validar** si la expresión es correcta bajo las reglas del autómata.
- **Calcular** el resultado si la expresión es válida.

---

## 🧠 Modelo Formal del Autómata

El autómata se define por la séptupla:

\[
M = (Q, \Sigma, \Gamma, \delta, q_0, Z_0, F)
\]

- \(Q = \{ q_0, q_1 \}\)
- \(\Sigma = \{ V, +, -, *, /, \hat{}\}\) donde **V** es un operando numérico
- \(\Gamma = \{ X, Z_0 \}\)
- \(q_0 = q_1\)
- \(Z_0\) es el símbolo de fondo de pila
- \(F = \varnothing\) — aceptación por **pila vacía** o configuración final válida

### Reglas principales (\(\delta\))

| Entrada | Cima de la pila | Acción |
|:------:|:----------------:|:------:|
| V      | Z0               | XZ0    |
| V      | X                | XX     |
| + - * /| XX               | X      |
| ε      | XZ0              | acepta |

Intuición: cada **operando** hace `push(X)`. Cada **operador binario** hace `pop(X), pop(X)` y luego `push(X)`. Al terminar, se acepta si la pila queda en configuración válida sobre `Z0`.

---

## 🗂️ Estructura del Proyecto

