### Define an interface

    type Car interface {
       Drive() string
    }

### Implement an interface

There is no implements or inherits or similar keyword. The relationship
of types to another interface is implicit. So to implement the interface
define above we declare a struct with the same method along with an
implementation.

    type Porsche struct {
    }

    func (p Porsche) Drive() string {
       return "100mph";
    }

See also:

### Empty Interface

Using the type

    interface{}

you can specify an empty interface that is implemented by all types. So
if you want to build a function taking a type-less parameter use the
empty interface

    func debug(x interface{}) {
       // do something
    }
