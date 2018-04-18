People that make databases like to include an extra little language to manipulate it. This gives database people something to do when no data is being added to the system and provides them with a space to work in where there is no chance of messing anything other than the database's data up. Because stored procedures are callable via SQL they are accessible to any system that can talk on a socket. Through permissions, a database programmer can protect against direct changes to data and instead offer interfaces that simplify things for other developers. As languages in new projects change the db programmer can work orthogonality to this.

Here's why stored procedures are bad. 

<strong>They are actually verbose</strong>
Sure you can find simple examples where they are concise like logging something in a table but try to do anything fancy like calculate a Fibonacci and you will find you are programming slow again. 

<strong>They are a yet another different language</strong>
Say you have a coder that needs to look at the database stored procedures. Now they have to learn a new language

<strong>They are hard to debug</strong>
As they are not general purpose languages you will be hard pressed to find a good debugger for them.

<strong>They are harder to version control</strong>
Small point, but each change to the code requires a database update 


What database programmers should work with is a typed general purpose language which only supports manipulating data in their database through static type checking.
