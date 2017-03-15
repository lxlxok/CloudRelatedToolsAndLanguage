## Go language

#### Function Related

> Parameter pass by value

* Strings 
* String
* Number
* Boolean   

> Parameter of function pass by pointer

* map  
* slice

> Variable change

Variable will be change if it is pass by pointer

```
type Circle struct {
    radius int
}

func (c *Circle) Change() {
    c.radius = 5  
}

func (c Circle) NotChange() {
    c.radius = 5
}

func main() {
    c := Circle{3}  
    c.NotChange()   // c keep the same radium
    c.Change()      // c change its radium

    cp := &Circle{3}
    c.NotChange() // c keep the same radium
    c.Change() // c change its radium  
}
```

#### Variable Related

> How to change a variable

In the same package, variable can be change directly by name.

```
package method

var GlobleStatus = 0
```

If the package is imported, only exported variable can be change  `method.GlobleStatus`

> The uniqueness of variable

There is only one singleton of `method.GlobleStatus` variable, no matter how many time the package have been imported by different package.



