# colscript

## 👥 Autores
### Valencia | Ángel | Rincón


## � ¿Qué es `COLSCRIPT`?

`COLSCRIPT` es un lenguaje de programación de sintaxis declarativa inspirado en el español. Su diseño prioriza la legibilidad natural, permitiendo que las instrucciones se lean de forma cercana al lenguaje cotidiano sin perder la estructura formal de un lenguaje de programación.

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
