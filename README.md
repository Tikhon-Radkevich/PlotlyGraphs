HTML Tags You Can Use on GitHub
===============================

<details open>
  <summary>This is the summary</summary>
  <p>And here are the details:</p>
  <ol>
    <li>Cash on hand: $500.00</li>
    <li>Current invoice: $75.30</li>
    <li>Due date: 5/6/19</li>
  </ol>
</details>

## `<kbd>` and `<samp>`

Sample or quoted output from a computer program using `<samp>`: <samp>sample output</samp>.

User input with `<kbd>`: <kbd>help mycommand</kbd>.

Tip: multiple keystrokes as part of a single input like <kbd><kbd>Ctrl</kbd>+<kbd>c</kbd></kbd> should be represent with nested `<kbd>`'s. The <code>Ctrl</code> is wrapped in its own `<kbd>`, the `+` _doesn't_ get its own `<kbd>`, then the `c` gets its own `<kbd>`: `<kbd><kbd>Ctrl</kbd>+<kbd>c</kbd>`. Results in: <kbd><kbd>Ctrl</kbd>+<kbd>c</kbd>

You can also nest `<samp>`'s inside `<kbd>`'s to represent text presented by the system which is then used for some user input. With GitHub's CSS these look the same as `<kbd>`'s nested inside `<kbd>`'s. For example: the <kbd><samp>OK</samp></kbd> button (`<kbd><samp>OK</samp></kbd>`).

If clicking multiple buttons (or menu items, etc) as part of a single input, you need `<kbd>`'s nested inside `<kbd>`'s to represent the multiple parts to a single input, same as with multiple keystrokes. But then you _also_ nest `<samp>`'s inside the leaf `<kbd>`'s to represent that it's clicking on things presented by the program rather than just keystrokes. Example: <kbd><kbd><samp>File</samp></kbd>⇒<kbd><samp>New Document</samp></kbd></kbd> (`<kbd><kbd><samp>File</samp></kbd>⇒<kbd><samp>New Document</samp></kbd></kbd>`).

A `<kbd>` inside a `<samp>` represents output from a computer program, but when the program was echoing back some previous input from the user! Not styled any differently by GitHub: <samp><kbd>git add my-new-file.cpp</kbd></samp>. Another example of this from MDN is <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/samp">showing the output of a terminal session</a> as a `<samp>` inside a `<pre>`, and with the user-entered parts wrapped in `<kbd>`'s inside the `<samp>`. This ends up styled a little oddly on GitHub but it does make sense (also note the use of Unicode █ as the cursor):

<pre><samp>mike@interwebz:~$ <kbd>md5 -s "Hello world"</kbd>
MD5 ("Hello world") = 3e25960a79dbc69b674cd4ec67a72c62

mike@interwebz:~$ █</samp></pre>

## `<sub>` and `<sup>`

Subscripts<sub>sub</sub> and superscripts<sup>sup</sup> with `<sub>` and `<sup>`.

## Footnotes


