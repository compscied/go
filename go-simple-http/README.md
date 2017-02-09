# Purpose of this is to illustrate how to write a simple web server in Go

# Install Go, set path etc.
- https://golang.org/doc/install

# Create a file
- gows.go

# Edit the file
~~~~~
package main

import (
	"io"
	"net/http"
)

func hello(w http.ResponseWriter, r *http.Request) {
	io.WriteString(w, "Go world go!")
}

func main() {
	http.HandleFunc("/", hello)
	http.ListenAndServe(":8080", nil)
}
~~~~~

# Run
- go run gows.go

# In a browser navigate to
- localhost:8080

