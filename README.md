# tables

football.db RSSSF (Rec.Sport.Soccer Statistics Foundation) tables (cache / playground / sandbox) mirror

tables pages converted to (plain) text  e.g.

- [rsssf.org/tables/30f.html](https://rsssf.org/tables/30f.html)       => [./tables/30f.txt](tables/30f.txt)        (=> wiki-style @  [rsssf.github.io/tables/30f](https://rsssf.github.io/tables/30f))
- [rsssf.org/tables/86full.html](https://rsssf.org/tables/86full.html) => [./tables/86full.txt](tables/86full.txt)  (=> wiki-style @  [rsssf.github.io/tables/86full](https://rsssf.github.io/tables/86full))

and many more, see the [.html tables a-z index page »](https://rsssf.github.io/tables/)



## why?

the point is to offer a common starter base that makes it easier to turn the ad-hoc semi-structured football leagues & cups, tables, match results, line-ups, penalty shoot-outs, and more into strutured data for (automatic) conversion to json, csv, sql & friends.


## how?

- the character endcoding is ALWAYS unicode (utf-8) - no more wondering
  if the encoding is windows-1250/1251/1252/1254, iso-8859-1/2, utf-16le or whatnot.
- all html entities are replaced with actual characters incl. known typos such as `&nitlde;`, `&oulm;`, `&uml;`, `&slig;`, `&aaacute;` etc.
- "smart" (single or double) quotes or unicode minus/hyphens are asciified
- all headings (h1/h2/h3/h4/h5/h6) replaced with wikitext-like headings e.g.
  -  `<h1>World Cup 1986</h1>`  => `= World Cup 1986`
  -  `<h2>Group A - ARG BUL ITA KOR</h2>`  => `== Group A - ARG BUL ITA KOR`
  -  etc.
- all named anchors (`<a name='fin'>`) replaced with plain text visible anchors (`‹§fin›`)
- all hyperlinks (`<a href='#premier'>Premier League</a>`) replaced with plain text visible links / references (`‹Premier League, see §premier›`)
- all style formatting (bold/italic/underline/strong) removed
- all `<pre>` (formatted) blocks merged into one plain text file


## what's next?

the long term vision is to get the RSSSF (Rec.Sport.Soccer Statistics Foundation) tables (pages) turned more
into a wiki (with source pages tracked via git)
that make it easier to fix typos and encourage updates.
why not use "uniform" proper wikipedia like article structures - that is, one h1 for the titled followed by h2s and the h2s divided into h3s and so on -
instead of the current ad-hoc zoo of h2 & h4 combos, or bold and underline "hand-crafted headers" or whatnot
and all without fear of losing the history (since all changes are tracked via git allowing easy restore and time travel all the way back to its origin).

for an experimental first try of an alternate (rsssf tables) online page view
(with auto-generated table of contents
and view/edit button to the git-backed .txt source and more),
start at the [.html tables a-z index page »](https://rsssf.github.io/tables/)





## scripts & tools

looking for the scripts & tools used? see [/scripts »](https://github.com/rsssf/scripts)
