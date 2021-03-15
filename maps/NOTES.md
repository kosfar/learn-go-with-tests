* The key type is special. It can only be a comparable type because without the ability to tell if 2 keys are equal, we have no way to ensure that we are getting the correct value. Comparable types are explained in depth in the language spec.

* An interesting property of maps is that you can modify them without passing as an address to it (e.g &myMap). This may make them feel like a "reference type", but as Dave Cheney describes they are not. A map value is a pointer to a runtime.hmap structure. So when you pass a map to a function/method, you are indeed copying it, but just the pointer part, not the underlying data structure that contains the data.