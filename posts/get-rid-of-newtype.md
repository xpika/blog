In Haskell, data types are defined using the keyword data. I personally think it should just be type. Actually, maybe it would be better if you just defined constructors with = syntax.type could be called alias. Makes sense so far.

Then there is newtype. newtype is like data but only for one constructor. It is strict by default and eliminated after type resolution happens by the compiler. Every time i see it, I'm reminded that newtype is actually data with a subtle change. What happens if people want syntax for unboxing? Maybe there should be an evenNewerType keyword. It's descending into what I would call "keyword hell". If people want to add bang patterns, they can just add them.

The justification seems to be one of marketing. "Look how clever the compiler is at optimizing this". This should not come at the expense of making the code harder to read.
