# Postfix Evaluator and Validator using Pushdown Automaton (PDA)

Este proyecto implementa y **visualiza** la evaluación de expresiones en **Notación Polaca Inversa (RPN / Postfija)** usando un **Autómata de Pila (PDA)**.  
Está orientado a fines educativos: muestra cómo un PDA puede validar la estructura de una expresión y calcular su resultado si es correcta.

---

## 🎯 Objetivo del Proyecto

- Mostrar el funcionamiento interno de un **PDA evaluador** de expresiones postfijas.
- Representar de forma clara el **contenido de la pila** durante el proceso.
- **Validar** si la expresión es correcta según las reglas del autómata.
- **Calcular** el resultado si la expresión es válida.

---

## 🧠 Modelo Formal del Autómata

El autómata se define por la séptupla:

\[
M = (Q, \Sigma, \Gamma, \delta, q_0, Z_0, F)
\]

- \(Q = \{ q_0, q_1 \}\)
- \(\Sigma = \{ V, +, -, *, /, \hat{}\}\)  
  (Donde **V** representa un valor numérico/operando)
- \(\Gamma = \{ X, Z_0 \}\)
- \(q_0 = q_1\)
- \(Z_0\) es el símbolo de fondo de pila
- \(F = \varnothing\) — **Aceptación por pila vacía** (o por configuración final válida)

### Reglas principales (\(\delta\))

| Entrada | Cima de la pila | Acción |
|:------:|:----------------:|:------:|
| **V**  | `Z0`             | `XZ0`  |
| **V**  | `X`              | `XX`   |
| **+ - \* /** | `XX`     | `X`    |
| **ε**  | `XZ0`            | **acepta** |

> Intuición: cada **operando** hace `push(X)`.  
> Cada **operador binario** hace `pop(X), pop(X)` y luego `push(X)`.  
> Al terminar, se acepta si la pila queda en configuración válida (una “X” consumida correctamente sobre `Z0`).

---

## 🗂️ Estructura del Proyecto

---

## ▶️ Cómo Ejecutar el Proyecto

### Opción A) Visual Studio Code + Live Server (recomendado)
1. Clona el repositorio:
   ```bash
  git clone https://github.com/PaoloVM27/Evaluador-y-Validador-Postfijo-con-Automata-de-Pila.git
   cd Evaluador-y-Validador-Postfijo-con-Automata-de-Pila

