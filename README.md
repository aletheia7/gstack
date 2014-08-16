#### gstack 
gstack is a go (golang) package. From the godocs of gstack:

>Package gstack provides methods to easily obtain the function name, file path, and line number of go code.

>gstack answers the questions: What function am I in? What is the full path to the file? What is the line number? 

#### Keywords
gostack is used as a stack trace (stacktrace), backtrace (back trace), and callstack (call stack) debug tool.

#### Install 
```bash
go get github.com/aletheia7/gstack
cd <gstack location>
go test -v
```

#### Documentation
```bash
godoc gstack
```
#### Example

```go
package main

import (
	"fmt"
	"gstack"
)

func main() {

	stack1 := gstack.New() 			// Index: 2
	fmt.Println(stack1)

	stack2 := gstack.New_index(3)	// Index: 3
	fmt.Println(stack2)

	// Index: 2, Function: gstack_test.Example, File: /<ommitted path ...>/go/src/gstack/gstack_test.go, Line: 27
	// Index: 3, Function: testing.runExample, File: /<ommitted path  ...>/go/src/pkg/testing/example.go, Line: 98
}
```

![LGPL](lgplv3-147x51.png)
