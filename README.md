# timelapse

A simple go function to measure app execution times and return in a human being format.

## Install

Require a running go environmnent with go modules.

1. Create a app folder
2. At command line run:
3. `go mod init yourAppFolderName`
4. create a main go file:
5. `touch  main.go`
6. Get the package:
7. `go get github.com/alansantosmg/timelapse`
8. Import the package and use in your app. See example below:

## Example

```go
package main

import (
	"fmt"
	"time"

// import timelapse package 
	t "github.com/alansantosmg/timelapse"
)

func main() {

    // sets a variable start type time at the beggining of your app
    start := time.Now()
    
    // past time - only for example purpose
	time.Sleep(5 * time.Second)

    // sets a variable end after the last execution code line 
	end := time.Now()

    // Pass start and end  to elapsedTime function and print the return
	fmt.Println(t.ElapsedTime(start, end))
}

```
