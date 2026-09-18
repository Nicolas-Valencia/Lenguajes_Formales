# colscript

## 👥 Autores
### Valencia | Ángel | Rincón


## � ¿Qué es `scriptcol`?

`scriptcol` es un lenguaje de programación de sintaxis declarativa inspirado en el español. Su diseño prioriza la legibilidad natural, permitiendo que las instrucciones se lean de forma cercana al lenguaje cotidiano sin perder la estructura formal de un lenguaje de programación.

---

## 🔑 Palabras clave

| Palabra      | Significado                              |
|--------------|------------------------------------------|
| `tenga`      | Declaración de variable                  |
| `si`         | Condicional `if`                         |
| `sino`       | Rama `else`                              |
| `o_entonces` | Rama `else if` / `otherwise`             |
| `mientracas` | Bucle `while`                            |
| `cantelas`   | Imprimir en pantalla                     |
| `sisas`      | Verdadero (`true`)                       |
| `nonas`      | Falso (`false`)                          |

---

## 🔣 Operadores

### 🧠 Lógicos

| Operador      | Significado |
|---------------|-------------|
| `y`           | AND         |
| `y_aparte`    | AND         |
| `o_de_pronto` | OR          |

### ⚖️ Comparación

| Operador | Significado           |
|----------|-----------------------|
| `==`     | Igual a               |
| `>=`     | Mayor o igual que     |
| `<`      | Menor que             |

### 💾 Asignación

| Operador | Significado           |
|----------|-----------------------|
| `=`      | Asignación de valor   |

---

## � Las 15 reglas

### 1️⃣

si (edad >= 18){
    cantelas("ya es legal");
}

---

### 2️⃣

mientracas(ciudad == "Cali"){
    violencia = sisas
}

---

### 3️⃣

tenga ventilador = nonas
si calor >= 30 {
    ventilador = sisas
}

---

### 4️⃣

si (calor >= 30 y aparte cobija == sisas){
    cantelas("vaya bañese mas bien")
}

---

### 5️⃣

si (edad >= 18 y_aparte tiene_cedula == sisas){
    cantelas("puede entrar")
} o_entonces{
    si (edad >= 18 o_de_pronto tiene_permiso == sisas){
        cantelas("puede entrar")
    }
}

---

### 6️⃣

tenga tiene_permiso = nonas;
tenga edad = 19;

si (edad >= 18 o_de_pronto tiene_permiso == sisas) {
    cantelas("Puede pasar");
}

---

### 7️⃣

tenga edad = 17;
tenga tiene_permiso = sisas;
tenga acompañado = nonas;

si ((edad >= 18 y tiene_permiso == sisas) o_de_pronto acompañado == sisas) {
    cantelas("Puede pasar");
} sino {
    cantelas("No puede pasar");
}

---

### 8️⃣

tenga contador = 0;

mientracas (contador < 5) {
    cantelas(contador);
    contador = contador + 1;
}

---

### 9️⃣

tenga calor = 32;
tenga ventilador = nonas;

si (calor >= 30) {
    ventilador = sisas;
    cantelas("Hace calor, prenda el ventilador");
} sino {
    cantelas("Está haciendo fresquito");
}

---

### 🔟

tenga ciudad = "Cali";

mientracas (ciudad == "Cali") {
    cantelas("Hace calorcito");
    ciudad = "Armenia";
}

---

### 1️⃣1️⃣

si (nota >= 3 y asistencia >= 80) {
    cantelas("Pasó");
}

---

### 1️⃣2️⃣

si (tiene_plata == sisas o_de_pronto tiene_tarjeta == sisas) {
    cantelas("Puede comprar");
}

---

### 1️⃣3️⃣

si (tiene_hambre == sisas o_de_pronto tiene_sueno == sisas) {
    cantelas("Vaya coma o duerma");
}

---

### 1️⃣4️⃣

si (es_lunes == sisas y_aparte es_festivo == sisas) {
    cantelas("No hay clase");
}

---

### 1️⃣5️⃣

si (usuario_correcto == sisas y clave_correcta == sisas) {
    cantelas("Bienvenido");
}

---

## 📊 Tabla de variables y tipos

Catálogo completo de las variables definidas en los ejemplos de las 15 reglas, con su equivalente en Java y un ejemplo de valor.

| Variable             | Tipo Java | Ejemplo de valor   |
|----------------------|-----------|--------------------|
| `edad`               | `int`     | `19`               |
| `calor`              | `double`  | `32.5`             |
| `temperatura`        | `double`  | `28.5`             |
| `ciudad`             | `String`  | `"Cali"`           |
| `nombre`             | `String`  | `"Diego"`          |
| `contraseña`         | `String`  | `"1234"`           |
| `tiene_cedula`       | `boolean` | `SISAS`            |
| `tiene_permiso`      | `boolean` | `NONAS`            |
| `acompañado`         | `boolean` | `SISAS`            |
| `usuario_activo`     | `boolean` | `SISAS`            |
| `ventilador`         | `boolean` | `NONAS`            |
| `aire_acondicionado` | `boolean` | `SISAS`            |
| `saldo`              | `double`  | `75000.0`          |
| `contador`           | `int`     | `0`                |
| `cantidad`           | `int`     | `5`                |
| `nota`               | `double`  | `4.2`              |
| `asistencia`         | `int`     | `90`               |


------------------------------------------------------------------

Fundamentación Teórica y Diseño de Colscript:

El diseño y la implementación del lenguaje de programación Colscript se sustentan en los principios formales de la Ciencia de la Computación, específicamente en la teoría de lenguajes formales, autómatas y la fase de análisis sintáctico y léxico de los compiladores. Las bases técnicas para definir su estructura se derivan principalmente de dos obras cumbres de la literatura informática:
1. "Introduction to Automata Theory, Languages, and Computation" (John E. Hopcroft, Rajeev Motwani, Jeffrey D. Ullman) [Introduction to Automata Theory, Languages, and Computation en Wikipedia].
2. "Compilers: Principles, Techniques, and Tools" (Alfred V. Aho, Monica S. Lam, Ravi Sethi, Jeffrey D. Ullman) — conocido globalmente como el Libro del Dragón.

1. Origen del Alfabeto, Palabras Clave y Tokens
En el Capítulo 1 ("Automata: The Methods and the Madness") de Hopcroft et al., se establece que un lenguaje formal se construye a partir de un alfabeto, que es un conjunto finito de símbolos. En Colscript, este alfabeto abstracto se materializa mediante el análisis léxico descrito en el Capítulo 3 ("Lexical Analysis") del libro de Aho et al.
La teoría de compiladores define que el texto fuente debe ser fragmentado en unidades lógicas llamadas tokens (identificadores, operadores, constantes) y palabras clave (keywords). 

2. Definición de la Sintaxis y Operadores
La estructura de las sentencias de Colscript (como las estructuras condicionales y los bucles) se fundamenta en las Gramáticas Libres de Contexto (GLC), detalladas de forma exhaustiva en el Capítulo 5 ("Context-Free Grammars and Languages") de Hopcroft, Motwani y Ullman. La sintaxis de un lenguaje define cómo se agrupan los tokens para formar instrucciones válidas.
En nuestro lenguaje, expresiones lógicas como si (calor >= 30 y_aparte cobija == sisas) siguen estrictamente las reglas de derivación gramatical. La precedencia de los operadores lógicos (y, y_aparte, o_de_pronto) y de comparación (==, >=, <) se hereda de los modelos jerárquicos de análisis sintáctico expuestos en el Capítulo 4 ("Syntax Analysis") del libro de Aho y Ullman, garantizando que el árbol de análisis sintáctico (parse tree) evalúe las operaciones matemáticas y booleanas sin ninguna ambigüedad.

3. Validación Matemática de las 15 Reglas Gramaticales
Las 15 reglas provistas en la especificación de Colscript representan las producciones formales de nuestra gramática. Según el Capítulo 4 de Hopcroft et al., las propiedades de los lenguajes libres de contexto permiten demostrar matemáticamente si una cadena pertenece o no a un lenguaje.
Cada una de nuestras 15 reglas de ejemplo es un reflejo de una producción válida de la gramática formal de Colscript. Por ejemplo, la regla que define la estructura del mientracas (bucle) o la combinación secuencial de declaraciones (tenga) seguida de condicionales anidados, requiere un análisis de reconocimiento sintáctico predictivo (como un analizador LL o LR). La teoría formal nos asegura que cuando el compilador o intérprete de Colscript analiza estas 15 estructuras, la máquina abstracta sabrá con precisión milimétrica cuándo el código es semánticamente correcto o cuándo debe arrojar un error de sintaxis debido a una violación de las reglas de producción del lenguaje.

---

## 📐 Gramática BNF

```
<sentencia> ::= <declaracion> | <declaracion_condicional> | <asignacion> | <condicional> | <ciclo> | <impresion>

<declaracion> ::= "tenga" <identificador> "=" <valor> ";"

<declaracion_condicional> ::= "tenga" <identificador> "=" <valor> "si" <expresion> <bloque>

<asignacion> ::= <identificador> "=" <expresion> [ ";" ]

<condicional> ::= "si" "(" <expresion> ")" <bloque> [ <alternativa> ]

<alternativa> ::= "sino" <bloque> | "o_entonces" "si" "(" <expresion> ")" <bloque> | "o_entonces" <bloque>

<bloque> ::= "{" <sentencias> "}"

<ciclo> ::= "mientracas" "(" <expresion> ")" <bloque>

<impresion> ::= "cantelas" "(" <expresion> ")" ";"

<expresion> ::= <expresion_or>

<expresion_or> ::= <expresion_and> | <expresion_and> "o_de_pronto" <expresion_or>

<expresion_and> ::= <comparacion> | <comparacion> "y" <expresion_and> | <comparacion> "y_aparte" <expresion_and>

<comparacion> ::= <operando> <operador_comparacion> <operando> | "(" <expresion> ")" | <operando>

<operando> ::= <valor> | <valor> "+" <operando>

<operador_comparacion> ::= "==" | ">=" | "<"

<valor> ::= <numero> | <texto> | "sisas" | "nonas" | <identificador>

<numero> ::= <entero> | <entero> "." <entero>

<identificador> ::= <letra> { <letra> | <digito> | "_" }

<entero> ::= <digito> { <digito> }

<digito> ::= "0" | "1" | "2" | "3" | "4" | "5" | "6" | "7" | "8" | "9"

<letra> ::= "a" | "b" | "c" | "d" | "e" | "f" | "g" | "h" | "i" | "j" | "k" | "l" | "m" | "n" | "o" | "p" | "q" | "r" | "s" | "t" | "u" | "v" | "w" | "x" | "y" | "z"

<texto> ::= '"' { <caracter> } '"'

<caracter> ::= <letra> | <mayuscula> | <digito> | " " | "," | "." | "!" | "?" | "á" | "é" | "í" | "ó" | "ú" | "ñ"

<mayuscula> ::= "A" | "B" | "C" | "D" | "E" | "F" | "G" | "H" | "I" | "J" | "K" | "L" | "M" | "N" | "O" | "P" | "Q" | "R" | "S" | "T" | "U" | "V" | "W" | "X" | "Y" | "Z"
```