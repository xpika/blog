If you create the following html document:
[crayon]
<html>
   <head>
      <style>
         body {
         font-size:40px;
         }
      </style>
   </head>
   <body>
      hello
      <table>
         <tr>
            <td>
               hello
            </td>
         </tr>
      </table>
   </body>
</html>
[/crayon]

It will render like this.

<a href="http://codekinder.com/wordpress/wp-content/uploads/2016/12/Screen-Shot-2016-12-15-at-7.51.35-pm.png"><img class="alignnone size-full wp-image-725" src="http://codekinder.com/wordpress/wp-content/uploads/2016/12/Screen-Shot-2016-12-15-at-7.51.35-pm.png" alt="screen-shot-2016-12-15-at-7-51-35-pm" width="113" height="101" /></a>

<code>If you add &lt;!doctype html&gt; to the top of your document like this:</code>

[crayon]
<!doctype html>
<html>
   <head>
      <style>
         body {
         font-size:40px;
         }
      </style>
   </head>
   <body>
      hello
      <table>
         <tr>
            <td>
               hello
            </td>
         </tr>
      </table>
   </body>
</html>
[/crayon]

It will render like this.

<a href="http://codekinder.com/wordpress/wp-content/uploads/2016/12/Screen-Shot-2016-12-15-at-7.56.31-pm.png"><img src="http://codekinder.com/wordpress/wp-content/uploads/2016/12/Screen-Shot-2016-12-15-at-7.56.31-pm.png" alt="screen-shot-2016-12-15-at-7-56-31-pm" width="123" height="109" class="alignnone size-full wp-image-729" /></a>

What happens is that browsers such as firefox will think that you are viewing an old website so they will try and render websites how they used to be rendered. This old way of rendering is called "Quirks mode". Adding &lt;!doctype html&gt; signifies that you are writing a modern webpage so the browser does not render using quirks mode.
