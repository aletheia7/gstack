### gstack 
gstack is a go (golang) package. From the godocs of gstack

Package gstack provides methods to easily obtain the function name, file path, and line number of go code.

gstack answers the questions: What function am I in? What is the full path to the file? What is the line number? 

#### Install 
```bash
go get github.com/aletheia7/gstack
cd <gstack location>
go test -v
```

#### Example

```golang
stack1 := New() // Index: 2
fmt.Println(stack1)
stack2 := New_index(3) // Index: 3
fmt.Println(stack2)

// Index: 2, Function: gstack_test.Example, File: /<ommitted path
// ...>/go/src/gstack/gstack_test.go, Line: 27
// Index: 3, Function: testing.runExample, File: /<ommitted path
// ...>/go/src/pkg/testing/example.go, Line: 98
```
