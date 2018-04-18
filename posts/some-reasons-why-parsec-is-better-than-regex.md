1. <strong>No need to escape things twice</strong>.

Usually in a programming language the escape character is backslash. Backslash is also used as an escape character in regular expressions. By Using a parsec, escaping for things like square bracket or even the second escaping backslash become non-existent. compare:

Regex:
```
"\[\\\\\["
```

Parsec:
```
string "[\\]"
```

Some languages like java-script build regular expression syntax into their languages but things just adds to language bloat.

2. <strong>Builder functions are type safe</strong>

Because regexps are almost always built from strings, if I want to produce a function that builds a regexp from arguments, I won't know if i have composed the parts in a valid way without testing a full expression. The function choice for instance in parsec can be written as follows

```
choice ps = foldr1 (<|>) ps
```

This can be verified to produce a working parser for any other working parsers given to it. With regex however I might forget to intersperse pipe "|" characters between options and not know that it's a bug until I've tested a list of choices greater than one. Also if there is an error that could have been picked up by a type system, then it may be harder to find the error especially if you have written a large function. A type safe library can locate a type error usually within two terms, the type of the function caller(Expected type) and the function callee(Actual type).

```
choice xs = "[" ++ ( map (\x->"("++x++")") xs) ++ "]"
```

3. <strong>Parsec uses monads</strong>
Try an implement an "S expression" validator in a single regexp. You can't do it. Now you need to get functions to compose parsers. Parsec provides functions for this which utilize monads, You can think of programming with monads as like programming with matruska dolls. Before each function is applied the mommy matruskas exchange information to help aid their babies transformation and transfer. In the case of parsec, each grammar composed has the state of the parser kept track for you by the parsec bind function. The best thing about monads is they aren't even specific to parsing, they can be used for any computations that involve the same patterns of type signatures. This means you can leverage functions which work in other libraries as well as fairly generic syntax extensions such as "do notation".
