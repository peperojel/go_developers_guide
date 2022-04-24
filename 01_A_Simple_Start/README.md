### Notas
Preguntas originadas a partir del ejemplo `main.go`.

- ¿Cómo ejecutamos nuestro código?
  
    ```bash
    # Para ejecutar
    go run main.go
    # Para compilar un ejecutable
    go build main.go
    ```
- ¿Qué función cumple la declaración `package main`?
  - Un *package* en Golang es el nombre de un proyecto, que puede constar de múltiples archivos.
  - El nombre *main* es reservado para *Packages* que al compilar tendrá como salida un archivo ejecutable (`.exe` en Windows).
  - Todo otro nombre se asumirá como un *Package* orientado a ser una dependencia.

- ¿Qué función cumple la instrucción `import "fmt"`?
  - Darle acceso al *current package* a `fmt`.
  
- ¿Cómo se organiza comunmente un *sourcecode* de Go?
  - Declaración del *package*
  - Importe de dependencias (std library or external).
  - Declarar funciones. *tell Go to do things!*


### Quiz questions
<details>
<summary>Cual es el propósito de la declaración package </summary>

Agrupar código con un propósito similar.

</details>

<details>
<summary>What is the special name we use for a package to tell Go that we want it to be turned into a file that can be executed?</summary>

`main`

</details>

<details>
<summary>The one requirement of packages named "main" is that we...</summary>

Declare a `main` function that will be run when program is executed.

</details>

</details>

<details>
<summary>Why do we use "import" statements?.</summary>

To give our package access to code written in another package.
</details>





