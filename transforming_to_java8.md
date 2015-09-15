## Transforming code to Java 8

#### SpringOne2GX 2015: Tuesday 2:45PM

* Effectively final.
* The variable inside the lamba is mutable. 
  ` .forEach(i -> (System.out::Println))` // i is mutable here.
* Intermediate functions are implcitly lazy. 
* Streams are lazy.
* Until the Terminal functions is called the intermidiate function is not called.
* Interfaces can have default method.
* Improved performance due to lazy invocation. 

##### Execute around method pattern
##### Cascade method pattern

