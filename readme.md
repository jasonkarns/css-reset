CSS Reset
=========

Essentially [Eric Meyer's reset](http://meyerweb.com/eric/tools/css/reset/), I've made a few tweaks that make his reset more palatable to my tastes. I've also [blogged](http://jasonkarns.com/blog/2010/02/15/css-reset/) about this project.

Changes
-------

### :focus { outline:none; }
The only rule of Meyer's reset that I consider actually harmful to the end user experience, the original rule disabled the browser default dotted outline on focused items.
Removing the default outline makes keyboard navigation almost impossible. Meyer even notes in the comments that developers should remember to override the rule with custom styles for focused items. But who actually does that?
Patrick Lauke found a method for alleviating the most annoying parts of the focus outline: [http://24ways.org/2009/dont-lose-your-focus](http://24ways.org/2009/dont-lose-your-focus)

### font-size: 100%;
While this rule doesn't affect the end user all that much, the rule's selector matches almost every element. Additionally, the font-size property is inherited. This means the property is both inherited *and* directly applied to nearly every element in your HTML.
For ardent Firebug users, this renders the style pane almost 99% noise as the same rule is inherited and then overridden at every level of the DOM tree. No thanks.

Questionable
------------

I haven't yet removed these items from the reset but I seriously question their utility. Among the following rules, think back to how often they would have actually been helpful on your projects. Not that often?

1. `border:0;` &ndash; on anything besides `img`, `abbr`, `acronym`?
2. `outline:0;` &ndash; what has outline by default?
3. `vertical-align: baseline;` &ndash; isn't that already the default?
4. `background: transparent;` &ndash; isn't that already the default?
5. `blockquote, q {quotes:none;}` &ndash; `blockquote` doesn't get quotation marks by default, and who actually uses `q`? If you ask me, quotation marks are just like punctuation&mdash;they should be part of the content, not the markup.
6. `ins` and `del` &ndash; I think the default style is fine. If not, it would get overridden by my main design anyway.

Feedback
--------
I'd love any feedback on this. Add your comments on the [wiki](http://wiki.github.com/jasonkarns/css-reset/) or my [blog post](://jasonkarns.com/blog/2010/02/15/css-reset/) on this subject.