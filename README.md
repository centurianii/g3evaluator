g3Evaluator
===========

A graphical client testing tool for batch processing javascript commands.<br />
It uses <code>eval()</code> and emulates <code>console.log()</code> in all clients even in IE browsers.

Capabilities:
=============
<ol>
<li>Dynamically add library files.<br />
It is viable even if we use the <code>file:///</code> protocol.</li>
<li>Dynamically create panels.<br />
Each panel consists of tabs and each tab contains a block of javascript commands that test our code. Consider panels as jasmine's test suites and tabs as nesting suites that contain a bunch of specs. It is apparent that each panel tests some specific code/library/file.</li>
<li>Dynamically add/edit/delete panels and tabs</li>
<li>Emulate <code>console.log()</code> in all browsers.</li>
<li>Edit title.</li>
<li>Load body html code except the <code>&lt;script></code> tags so that, we can edit our source file and replace the barebone original tags.</li>
<li>Uses advanced object stringify capabilities of <code>g3.debug</code> object. For this reason a new method was addded to <code>g3.debug</code>: <code>g3.debug.toHtml()</code>.</li>
<li>Excibit's late instantiation (instantiation on demand) of singleton objects with the following command: <code>g3.Evaluator.getInstance();</code>.</li>
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
  :  |- <g3MyClass.js>
  :  :
  |-tests
  |  |-jasmine-standalone-2.0.0
  |  |  |-lib
  |  |  |-spec
  :  :  :
  |  |-g3
  |  :  |- <g3MyClass-SpecRunner.html>
  |  :  |- <g3MyClass-Spec.js>
  |  :  |- <g3MyClass-SpecHelper.js>
  |  :  |- g3Evaluator.css
  |  :  |- g3Evaluator.js
  |  :  |- g3Evaluator.html (rename this file to test-g3MyClass.html)
  |  :  |- <test-g3MyClass.html>
  :  :  :
</pre>

There are two <code>g3</code> folders: the one contains the actual code and the other under <code>tests</code> contains the test files.

Todo
====
Use of web storage to save user edit.

Have fun!
