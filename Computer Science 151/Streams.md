---
tags:
  - cs151
---
## Regular Expressions (Regex)

```java
String regex = "put regex here"
// Strings have a built in matches method
System.out.println("string".matches(regex))
```
### Regex Symbols
## Some Facts
* Streams are similar to collections
* They don't store their own data
	* the data comes from elsewhere
	* from a collection, a file, a database, the internet
* streams were designed to work well with lambda expressions
* streams are immutable
* stream processing is lazy

## Lazy Processing
* works backwards, only computes what is necessary
* will stop processing after limit is reached (`xxx.limit(num)`)
* 