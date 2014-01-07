g3Evaluator
===========

A graphical client testing tool for batch processing javascript commands.<br />
It uses <code>eval()</code> and emulates <code>console.log()</code> in all clients even in IE browsers.

Capabilities:
=============
<ol>
<li>Dynamically create panels.<br />
Each panel consists of tabs and each tab contains a block of javascript commands that test our code.</li>
<li>Dynamically add/edit/delete panels and tabs</li>
<li>Emulate <code>console.log()</code> in all browsers.</li>
<li>Edit title.</li>
<li>Load body html code except the <code>&lt;script></code> tags so that, we can edit our source file and replace the barebone original tags.</li>
</ol>

Depends
=======
On <code>g3.debug</code>.

Testing
=======
The <code>g3.Evaluator</code> is used to test functioning behaviour along with jasmine v.2.0.

<h3>How our code is constructed?</h3>
<pre>
my source files (g3), necessary libraries (jquery) and my tests folder (tests):
client
  :
  |-jquery
  :  :
  |-g3
  :  |-g3MyClass.js
  :  :
  |-tests
  |  |-jasmine-standalone-2.0.0
  |  |  |-lib
  |  |  |-spec
  :  :  :
  |  |-g3
  |  :  |-g3MyClass-SpecRunner.html
  |  :  |-g3MyClass-Spec.js
  |  :  |-g3MyClass-SpecHelper.js
  |  :  |-test-g3MyClass.js (rename this file to this one!)
  :  :  :
</pre>

There are two <code>g3</code> folders: the one contains the actual code and the other under <code>tests</code> contains the test files.

Todo
====
Use of web storage to save user edit.

Have fun!
