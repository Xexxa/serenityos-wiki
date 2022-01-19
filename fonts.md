# Fonts in SerenityOS (draft)

| Family            |Default for    |Size    |Format|Serif |Monospace |Regular |Italic |Bold Italic |Bold |Black|Author
| ---               |:---           |:---    |:---: |:---: |:---:     |:---:   |:---:  |:---:       |:---:|:---:|:---
| Cathode           |               |10      | .font|      | ✔️       | ✔️     |       |            |     |      | [@electrikmilk](https://github.com/electrikmilk)
| CJK Biáng         |               |36      | .font| ?    | ✔️       | ✔️     |       |            |     |      | [@Xexxa](https://github.com/Xexxa)
| Csilla            |_text editor_, .txt|10/12| .font|     | ✔️       | ✔️     |       |            | ✔️  |       |
| Katica            |_system_, .html|10/12   | .font|      |          | ✔️     |       |            | ✔️  |      | 
| Liberation Serif  |               |8-36    | .ttf | ✔️   |          | ✔️     | ✔️    | ✔️          | ✔️  |      | [@mattco98](https://github.com/mattco98)
| Liza              |               |10/24/36| .font|      | ✔️       | ✔️     |       |            | ✔️  | ✔️    |
| Marieta           |               |24/36   | .font|      |          | ✔️     |       |            | ✔️  |      | [@thankyouverycool](https://github.com/thankyouverycool)
| Pabbleton         |               |14      | .font|      |          | ✔️     |       |            | ✔️  |      |
| Roman             |               |10      | .font|  ✔️   |         | ✔️     |       |            |     |      | [@electrikmilk](https://github.com/electrikmilk)
| SerenitySans      |               |8-36    | .ttf |      |          | ✔️     |       |            |     |      |
| Serifina          |               |10      | .font| ✔️   |          |        |✔️     |            |     |      |
| Source            |               |10      | .font|      | ✔️       | ✔️     |       |            |     |      | [@electrikmilk](https://github.com/electrikmilk)
| [Tiny](/fonts/Tiny.md)|           |6       | .font|      |          | ✔️     |       |            |     |      | [@Xexxa](https://github.com/Xexxa)

## Creating a font
- **Mandatory glyphs** Always include character FFFD &#xfffd; (<https://www.unicode.org/charts/PDF/UFFF0.pdf>), it's the fallback character if a glyph is missing.

- **Filename:** Give the font a filename in the following format NameStyleSize.ext (examples: KaticaRegular10.font)

- **CJK:** If the font is primarly or exclusively for CJK characters then prefix the family with CJK and space "CJK Name" 

- **Constructed/artificial scripts:** If you want to encode for example Klingon or Tengwar, then follow the assignments of UCSUR[^1] 

- **Unicode charts:** Always check the Unicode charts if you do not know a script by heart. There is often useful information about the glyphs (similar glyphs for reference or if a glyph is based on another). [How to read the symbols in Unicode Charts](https://unicode.org/charts/About.html#Key)<br>![Screenshot from Unicode charts](/images/fonts-unicode-chart.png)

## Unicode PUA usage
- If you want to add glyphs to Unicodes PUA(private use area) for use in SerenityOS, pick codepoints within the range 10CA00-10CFFF

- **Currently reserved ranges:**
  - 10CD00-10CDFF Yak emojis https://serenityos.net/~xexxa/10CD Code points: 256, Assigned characters: 47

## Practical
- System fonts are located in `Base/res/fonts/` (repo) and `/res/fonts` (running SerenityOS)

- [How to transfer files from QEMU to your host machine](https://github.com/SerenityOS/serenity/blob/master/Documentation/TransferringFiles.md)

## Commits and pull requests
- **Before making a PR / Merge conflicts:** You can copy multiple glyphs in font editor(shift click to select a range), it is recommended that you have the habbit of copying the glyphs you added/modified to a fresh pull of the font-file and look for conflicting [pull request](https://github.com/SerenityOS/serenity/pulls) before creating a PR. There has been a few cases of merge conflicts or outdated font-files has removed glyphs.

- **Commit:** Always include the codepoints for the glyphs you added or modified. Modified glyphs should also include how/why they were modified.

- **PR:** A screenshot of what you added/edited makes it easier for maintainers to review your fantastic work.


## General design guidelines

## Testing a script
A good sample text for testing a script is the Universal Declaration of Human Rights (UDHR), there is 487 translations at <https://unicode.org/udhr/> (unicode), the sample could then if needed be compared to one of the 530 translations available at <https://www.ohchr.org/EN/UDHR/Pages/SearchByLang.aspx> (pdf, html, sound).


## Links
[Unicode charts [unicode.org]](https://www.unicode.org/charts/)

[SerenityOS Discord #fonts](https://discord.com/channels/830522505605283862/927893781968191508)

[^1]: [Under-ConScript Unicode Registry](https://www.kreativekorp.com/ucsur/)
