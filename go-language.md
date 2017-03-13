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
```



