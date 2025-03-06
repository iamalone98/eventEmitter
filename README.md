# EventEmitter

## Install

```text
go get github.com/iamalone98/eventEmitter
```

## Quick start example

```golang
import (
  "fmt"
  "github.com/iamalone98/eventEmitter"
)

func main() {
  emitter := eventEmitter.NewEventEmitter()

	emitter.On("test", func(data interface{}) {
		if v, ok := data.(int); ok {
			fmt.Println(v)
		}
	})

	emitter.Emit("test", 1)
}
```
