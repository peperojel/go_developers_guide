## Deeper Into Go

### Variable declarations
- Go is a "static type" language. We need to assign a *type* to every variable about to be declared.
    ```Go
    var card string = "Ace of Spades"

    // Optionally we can let the compiler to infer var type
    
    card := "Ace of Spades"

    // No need for := for following reassignments

    card = "Five of Diamonds"
    ```
- We need to inform the compiler the type of outputs of a `func` about to be declared.
    ```
    func newCard() string {}
    ```

### Quiz questions

<!-- Variable declarations -->
<details>
    <summary>
    Variable declarations
    </summary>

<details>
<summary>

**Q**: Is the following a valid way of initializing and assigning a value to a variable?

`var bookTitle string = "Harry Potter"`

</summary>

**A**:
    Yes

</details>

<details>
<summary>

**Q**: Is the following a valid way of initializing an assigning a value to a variable? `fruitCount := 5`

 </summary>

**A**:
    Yes

</details>

<details>
<summary>

**Q**: After running the following code, Go will assume that the variable `quizQuestionCount` is of what type?

`quizQuestionCount := 10`

 </summary>

    Integer

</details>

<details>
<summary>

**Q**: Will the following code compile?  Why or why not?

```Go
paperColor := "Green"
paperColor := "Blue"
```

 </summary>

    No, because a variable can only be initialized one time.  In this case, the ':=' operator is being used to initialize 'paperColor' two times

</details>

<details>
<summary>

**Q**: Are the two lines following ways of initializing the variable 'pi' equivalent?

```Go
pi := 3.14 

var pi float64 = 3.14 
```

 </summary>

    Yes
</details>

<details>
<summary>

**Q**: Is the following code valid?

```Go
package main
 
import "fmt"
 
deckSize := 20
 
func main() {
  fmt.Println(deckSize)
}
```



 </summary>

    It doesn't compile. But if we change it to verbose declaration (with type) it does.

</details>

<details>
<summary>

**Q**: We might be able to initialize a variable and then later assign a variable to it.  Is the following code valid?

```Go
package main
 
import "fmt"
 
func main() {
  var deckSize int
  deckSize = 52
  fmt.Println(deckSize)
}
```

 </summary>

    Yes! We can initialize and then later assign a value to a variable.
</details>

<details>
<summary>

**Q**: Is the following code valid?

```Go
package main
 
import "fmt"
 
var deckSize int
 
func main() {
  deckSize = 50
  fmt.Println(deckSize)
}
```

 </summary>

    Yes! We can initialize a variable outside of a function, we just can't assign a value to it.

</details>

<details>
<summary>

**Q**: Is the following code valid?  Why or why not?

```Go
package main
 
import "fmt"
 
func main() {
  deckSize = 52
  fmt.Println(deckSize)
}
```

 </summary>

    No, because 'deckSize' is assigned a value before it is intialized. Variables must first be initialized with the ':=' operator or the 'var variableName type' syntax.

</details>
</details>

<!-- Function declarations -->

<details>
<summary>
Function declarations
</summary>

<details>
<summary>

**Q**: If a function returns a value, do we have to annotate, or mark, the function with the type of value that is being returned?

 </summary>

    Yes, every function that returns a value must indicate what type of value it is returning.

</details>

<details>
<summary>

**Q**: The Go compiler is presenting an error message about the following function.  What should we do to fix the error?

```Go
func getSize() {
    return "30 meters"
}
```

 </summary>

 ```Go
func getSize() string {
    return "30 meters"
}
```

</details>

<details>
<summary>

**Q**: Is the following function valid?

```Go
func estimatePi() float64 {
    return 3.14
}
```

 </summary>

    Yes

</details>

<details>
<summary>

**Q**: Is the following code valid?  Why or why not?

```Go
package main
 
import "fmt"
 
func main() {
    fmt.Println(getTitle())
}
 
func getTitle() string {
    return "Harry Potter"
}
```
 </summary>

    Yes

</details>

<!-- Question start -->
<details>
<summary>

**Q:** Here's a tough one!  Imagine we have two files in the same folder with the same package name.  Will the following code successfully compile?  This might take a little experimentation on your side.  If you do try this out yourself, run your code with the command `go run main.go state.go` .

In main.go
```Go
package main
 
func main() {
    printState()
}
```

In a separate file called state.go:
```Go
package main
 
import "fmt"
 
func printState() {
    fmt.Println("California")
}
```

</summary>

**A:**
    Yes, because both files are a part of the same package. Files in the same package can freely call functions defined in other files.

</details>
<!-- End of question -->

</details>





