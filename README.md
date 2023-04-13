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

You can use `<sup>` to create linked footnotes.<sup id="backToMyFootnote"><a href="#myFootnote">1</a></sup>

## `<ins>` and `<del>`

Inserted text with `<ins>`: <ins>inserted</ins> and deleted text with `<del>`: <del>deleted</del>. These can both have the `cite` attribute.

## `<var>`

Variables with `<var>`: <var>myVariable</var>.

## `<q>`

Inline quotes with `<q>` get curly quotation marks around them: <q>inline quote</q>. You can also use the `cite` attribute on them. You can use `cite` on a `<blockquote>` too, if you enter the `<blockquote>` manually.

## Definition lists (`<dl>`, `<dt>` and `<dd>`)

<dl>
  <dt>Publisher</dt>
  <dd>CNN and others</dd>
  <dt>Community admin</dt>
  <dd>Admins of Climate Feedback, Public Editors, etc</dd>
  <dt>Hypothesis admin</dt>
  <dt>Hypothesis developer</dt>
</dl>

## `<ruby>`, `<rt>` and `<rp>`

`<ruby>`, `<rt>` and `<rp>` can be used for [showing pronunciation of East Asian characters](http://html5doctor.com/ruby-rt-rp-element/). Example:

<ruby>
  漢 <rp>(</rp><rt>Kan</rt><rp>)</rp>
  字 <rp>(</rp><rt>ji</rt><rp>)</rp>
</ruby>

## `<div>`
  
`<div>` is also allowed, along with the `itemscope` and `itemtype` attributes for [defining microdata](http://html5doctor.com/microdata/):

<div itemscope itemtype ="http://schema.org/Movie">
  <h6 itemprop="name">Avatar</h6>
  <span>Director: <span itemprop="director">James Cameron</span> (born August 16, 1954)</span>
  <span itemprop="genre">Science fiction</span>
  <a href="https://youtu.be/0AY1XIkX7bY" itemprop="trailer">Trailer</a>
</div>

## HTML Entities

An `&` gets changed into `&amp;` and `<` and `>` get changed into `&lt;` and `&gt;`.
You can also enter HTML entities like `&copy;` and `&pound;` directly:
&copy;, &pound;, &sect;, &para;, &larr;, &rarr;, &hearts;.

## Unicode Characters

You can paste unicode characters directly and they'll be rendered. Here's a few: ⌘ ⌥ ❄ ★ ☂ 🍔 🤷 📚 🎒 ✋ 👓 🐅.

## Emoji

## References

* [GitHub's HTML sanitization code](https://github.com/jch/html-pipeline/blob/master/lib/html/pipeline/sanitization_filter.rb#L44-L106)
* A [GitHub issue](https://github.com/github/markup/issues/245) about this

## Footnotes

<ol>
  <li id="myFootnote">
    <p>
      Since you need an <code>id</code> attribute on both the footnote and on the footnote reference (to enable the footnote to contain a link <em>back</em> to the reference) I think they both need to be done in raw HTML. I don't think there's any Markdown syntax for this. See the <a href="https://gist.githubusercontent.com/seanh/13a93686bf4c2cb16e658b3cf96807f2/raw/04f35dd73445897827592a155c193976bfb756b8/Testing.markdown">source code of this file</a> for how it's done.
      <a href="#backToMyFootnote" title="Jump back to footnote 1 in the text.">↩︎</a>    
    </p>
  </li>
</ol>
