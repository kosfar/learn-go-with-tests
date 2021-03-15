* In Go if a symbol (so variables, types, functions et al) starts with a lowercase symbol then it is private outside the package it's defined in.

* In Go, when you call a function or a method the arguments are copied.

* These pointers to structs even have their own name: struct pointers and they are [automatically dereferenced](https://golang.org/ref/spec#Method_values).

* In Go, if you want to indicate an error it is idiomatic for your function to return an err for the caller to check and act on.

* nil is synonymous with null from other programming languages. Errors can be nil because the return type of Withdraw will be error, which is an interface. If you see a function that takes arguments or returns values that are interfaces, they can be nillable.
Like null if you try to access a value that is nil it will throw a runtime panic. This is bad! You should make sure that you check for nils.

* Whilst the Go compiler helps you a lot, sometimes there are things you can still miss and error handling can sometimes be tricky. There is one scenario we have not tested. To find it, run the following in a terminal to install errcheck, one of many linters available for Go. go get -u github.com/kisielk/errcheck

* When a function returns a pointer to something, you need to make sure you check if it's nil or you might raise a runtime exception, the compiler won't help you here. Useful for when you want to describe a value that could be missing

* [Don’t just check errors, handle them gracefully](https://dave.cheney.net/2016/04/27/dont-just-check-errors-handle-them-gracefully)
