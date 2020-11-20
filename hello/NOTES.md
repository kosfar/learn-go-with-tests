Notes on [Hello, World](https://quii.gitbook.io/learn-go-with-tests/go-fundamentals/hello-world)


* Another quality of life feature of Go is the documentation. You can launch the docs locally by running `godoc -http :8000`. If you go to http://localhost:8000/pkg you will see all the packages installed on your system.

* Constants should improve performance of your application as it saves you creating the `"Hello, "` string instance every time Hello is called.

* Refactoring is not just for the production code! It is important that your tests are clear specifications of what the code needs to do.

* In Go public functions start with a capital letter and private ones start with a lowercase.
