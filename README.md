#### gstack 
gstack provides methods to easily obtain the function name, file path, and line number of go code.
gstack answers the questions: What function am I in? What is the full path to the file? What is the line number? 

#### Install 
```bash
go get github.com/aletheia7/gstack
cd <gstack location>
go test -v
```

#### Documentation
[![](https://img.shields.io/badge/godoc-reference-blue.svg)](https://godoc.org/github.com/aletheia7/gstack) 
#### Example

```go
package main
import (
	"fmt"
	"gstack"
)

func main() {
	buried()
}

func buried() {
	lost()
}

func lost() {
	stack1 := gstack.New()			// Index: 2
	fmt.Println(stack1)
	stack2 := gstack.New_index(3)	// Index: 3
	fmt.Println(stack2)
	stack3 := gstack.New_index(4)	// Index: 4
	fmt.Println(stack3)
}
```
##### Ouput
```bash
Index: 2, Function: main.lost, File: /<path ommitted>/src/t/t.go, Line: 19
Index: 3, Function: main.buried, File: /<path ommitted>/src/t/t.go, Line: 14
Index: 4, Function: main.main, File: /<path ommitted>/src/t/t.go, Line: 9
```

#### License 

Use of this source code is governed by a BSD-2-Clause license that can be found
in the LICENSE file.

[![BSD-2-Clause License](osi_logo_100X133_90ppi_0.png)](https://opensource.org/)
