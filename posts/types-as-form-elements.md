When I was in kindergarden we had this toy where you placed shaped objects into something the size of soccer ball. The ball had a number of holes in it. The aim of the game was to fit the right shapeÂ to the right hole. Only the correct shaped hole would allow you to insert it's matching shape.

<a href="http://codekinder.com/wordpress/wp-content/uploads/2014/05/shape_fitter.png"><img class="alignnone size-medium wp-image-91" alt="shape_fitter" src="http://codekinder.com/wordpress/wp-content/uploads/2014/05/shape_fitter-272x300.png" width="272" height="300" /></a>

This is a concept which is similar to what learnt when assembling PC's. I discovered that many of the parts only fitted if you put them in the correct way. I learnt that these as "keyed" inputs. In comparison to some other sockets, such as old ram chips, where if you put them in the wrong way, the computer may short circuit.

The concept of a keyed port like in the puzzle mentioned earlier and computer hardware is like Â a type checker. Type checkers can stop invalid code from running at development time which is before you even run the application. Code without that kind of check may otherwise malfunction at some client's expense.

Keying inputs is something Graphical interface designers often do as well. Consider a checkbox. It has two states which you could describe as "checked" and "unchecked". This is similar to the Boolean type which also has only two values "True" and "False". Â  Consider what the interface would be like if all checkboxes were replaced with text fields. The user may think it right to enter words that are synonymous with true such as Yes, Correct or the slang term yup or the ambiguous "maybe". On a side note, I've overheard a funny way to answer Â a question with two queries. Â Instead of replying "both" you can overload the phrase "yes" to be an answer to both questions. For example:
<blockquote>"So, do you like typed or untyped languages?"

"Yes!"</blockquote>
On my smartphone the checkboxes are replaced by switches which have the same effect.

Going through other types, an enumeration is a bit like a radio boxes. When you have too many a select box becomes more appropriate. Numbers can be keyed by an up/down control however this is often left out for convenience reasons. Â Text like a persons name is pretty much too variable to be keyed in any way and is better off collected in its literal form.I find it hard to imagine a checkbox asking if your last name is "Smith", it's at least unfair to anyone without that surname.

Sometimes selecting one option will allow for more options to be selected. This is similar to a composite type such as a Maybe. Consider a form element which asks you if you want to leave your email and only allows you to fill in an email field if you select yes. This could be thought of as

<code>Maybe Email</code>

Sometimes the presence of one option can counter another. For example, choosing a cd drive may negate the various options associated with a Disc drive and visa versa.

<code>Either HardDrive DiscDrive</code>


The concept seems to be a sound one, but having to insert Constructors like Just and Nothing and Left and Right can be a bit of a pain.
