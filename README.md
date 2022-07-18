Hi!
===
I'm @kampde

Brief mention of What The Hell is modal editing
===============================================
* Differentiation between actually writing on the document or moving the cursor
  around / executing actions on the text.
* See http://www.viemu.com/a_vi_vim_graphical_cheat_sheet_tutorial.html
* Also, there are multiple plugins for multiple editors to bring vi movements
  to them, so even if you don't use Vim you can benefit from this!

Vim Movements
=============
What movements can you do with regular movement keys?

* left, down, up, right (`hjkl`)
* line start (`0`), content start (for indented lines, `_`), line end (`$`)
* go to first line (`gg`), go to line 83 (`83gg`), go to last line (`G`)
* differentiation between word and WORD (ie foo-bar are 2 words but only 1 WORD)
  * words are sequences of letters, numbers and underscores. A dot, dash, slash
    or any other character marks the end of a word.
  * WORDS are sequences of non-whitespace characters.
* go to next word (`w`) / WORD (`W`)
* beginning of current/previous word (`b`) / WORD (`B`)
* end of current/next word (`e`) / WORD (`E`)
* go to next paragraph (`}`), beginning of current/previous paragraph (`{`)
* also multiplied. So you can say three words forward (`3w`) or 8 lines up (`8k`).
* next character "u" in this line (`fu`, "find u", works with any character)
* before next character "u" in this line (`tu`, "til u", works with any
  character)

Movements with visual mode (ie selecting text)
==============================================
* Just enter "Visual" mode (`v`) or "Visual Line" (`V`) or "Visual Block" (`^V`)
  and move the cursor around with the movements we just saw.
  * If you execute a command (like `d`elete) when you have something selected,
    the command acts on your selection.

* Many actions (like `c`hanging, `y`anking, `d`eleting) accept a movement:
  * delete 3 words (`d3w`)
  * change current paragraph (`c}`)
  * Uppercase current word (`gUw`)

Extra movements when selecting/issuing a command
================================================
You can act on blocks as well. Like the whole word/WORD independently on the
cursor position, act on the content on parentheses or braces or html tags

* change text inside (Inside) parentheses (`ci)`)
  * look, `i` here does not enter insertion mode, because the action `c`
    expects a _movement_.
  * similar for deleting shit inside curly braces (`di}`) or yanking the
    text inside braces (`yi]`)
  * lowercasing text between angle brackets (`gui>`). Uppercasing is possible
    too (`gUi>`)
  * selecting text inside html tags (`vit`)
  * deleting current word (`diw`) or WORD (`diW`)
* Selecting all (All) and not just Inside
  * instead of using `i` as part of the movement you use `a`
  * `ca)`
  * `da}`
  * ...

Nice Stack Overflow documentation
=================================
Google for "[stackoverflow you don't grok vi](https://stackoverflow.com/a/1220118/592540)"
