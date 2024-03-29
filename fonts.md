# Fonts in SerenityOS (draft)

_The information in this table is available(and up-to-date) at <https://fonts.serenityos.net/>._

| Family            |Default for    |Size    |Format|Serif |Monospace |Regular |Italic |Bold Italic |Bold |Black|Author
| ---               |:---           |:---    |:---: |:---: |:---:     |:---:   |:---:  |:---:       |:---:|:---:|:---
| Ataraxia          |               |10      | .font|      | ✔️       | ✔️     |       |            | ✔️   |      | [@djwisdom](https://github.com/djwisdom)
| Cathode           |               |10      | .font|      | ✔️       | ✔️     |       |            |     |      | [@electrikmilk](https://github.com/electrikmilk)
| CJK Biáng         |               |36      | .font| ?    | ✔️       | ✔️     |       |            |     |      | [@Xexxa](https://github.com/Xexxa)
| Csilla            |_text editor_, .txt|10/12| .font|     | ✔️       | ✔️     |       |            | ✔️  |       |
| Katica            |_system_, .html|10/12   | .font|      |          | ✔️     |       |           | ✔️  |      | 
| Liberation Serif  |               |8-36    | .ttf | ✔️   |          | ✔️     | ✔️    | ✔️          | ✔️  |      | [@mattco98](https://github.com/mattco98)
| Liza              |               |10/24/36| .font|      | ✔️       | ✔️     |       |            | ✔️  | ✔️    |
| Lucidity          |               |12      | .font|      |         | ✔️     |       |            | ✔️  |      | [@djwisdom](https://github.com/djwisdom)
| Marieta           |               |24/36   | .font|      |          | ✔️     |       |            | ✔️  |      | [@thankyouverycool](https://github.com/thankyouverycool)
| Pabbleton         |               |14      | .font|      |          | ✔️     |       |            | ✔️  |      |
| Roman             |               |10      | .font|  ✔️   |         | ✔️     |       |            |     |      | [@electrikmilk](https://github.com/electrikmilk)
| Satori            |               |10      | .font|      |          | ✔️     |       |           | ✔️    |      | [@djwisdom](https://github.com/djwisdom)
| Satori Mono       |               |10      | .font|      | ✔️        | ✔️     |       |           | ✔️    |      | [@djwisdom](https://github.com/djwisdom)
| SerenitySans      |               |8-36    | .ttf |      |          | ✔️     |       |            |     |      | [@sunverwerth](https://github.com/sunverwerth)
| Serifina          |               |10      | .font| ✔️   |          |        |✔️     |            |     |      | [@thankyouverycool](https://github.com/thankyouverycool)
| Source            |               |10      | .font|      | ✔️       | ✔️     |       |            |     |      | [@electrikmilk](https://github.com/electrikmilk)
| [Tiny](/fonts/Tiny.md)|           |6       | .font|      |          | ✔️     |       |            |     |      | [@Xexxa](https://github.com/Xexxa)

## Creating a font
- Read our quick intro to using **FontEditor** at (<https://wiki.serenityos.net/FontEditor/UsingFontEditor.html>)
- **Mandatory glyphs** Always include character FFFD &#xfffd; (<https://www.unicode.org/charts/PDF/UFFF0.pdf>), it's the fallback character if a glyph is missing.

- **Filename:** Give the font a filename in the following format NameStylePresentationSize.ext (examples: KaticaRegular10.font)

- **Metadata:** metadata.family contains the fonts "name", for example "Katica". metadata.name contains the font "name" and style, for example "Katica Regular".

- **CJK:** If the font is primarly or exclusively for CJK characters then prefix metadata.family and metadata.name with CJK and space. "CJK Name" & "CJK Name Style"

- **Constructed/artificial scripts:** If you want to encode for example Klingon or Tengwar, then follow the assignments of UCSUR[^1] 

- **Unicode charts:** Always check the [Unicode charts](https://www.unicode.org/charts/) if you do not know a script by heart. There is often useful information about the glyphs (similar glyphs for reference or if a glyph is based on another). [How to read the symbols in Unicode Charts](https://unicode.org/charts/About.html#Key)<br>![Screenshot from Unicode charts](/images/fonts-unicode-chart.png)

## Unicode PUA usage
- If you want to add glyphs to Unicodes PUA(private use area) for use in SerenityOS, pick codepoints within the range 10CA00-10CFFF.

- **Currently reserved ranges:**
  - 10CD00-10CDFF Yak emojis [https://serenityos.net/~xexxa/10CD](https://serenityos.net/~xexxa/10CD) Code points: 256, Assigned characters: 47.

## Practical
- System fonts are located in `Base/res/fonts/` (repo) and `/res/fonts` (running SerenityOS)

- [How to transfer files from QEMU to your host machine](https://github.com/SerenityOS/serenity/blob/master/Documentation/TransferringFiles.md)

## Commits and pull requests
- **Before making a PR / Merge conflicts:** You can copy multiple glyphs in font editor(shift click to select a range), it is recommended that you have the habit of copying the glyphs you added/modified to a fresh pull of the font-file and look for conflicting [pull request](https://github.com/SerenityOS/serenity/pulls) before creating a PR. There has been a few cases of merge conflicts and outdated font-files removing glyphs.

- **Commit:** Always include the codepoints for the glyphs you added or modified. Modified glyphs should also include how/why they were modified.

- **PR:** A screenshot of what you added/edited makes it easier for maintainers to review your fantastic work.

## Working with CJK (Chinese, Japanese and Korean)

- **Katica:** currently glyphs with multiple variants in Katica uses simplefied Chinese, if that is not available it uses suitable Chinese with a <code>G*</code>-code[^2].

- **CJK Biáng:** currently glyphs with multiple variants in CJK Biáng uses traditional Chinese.

## General design guidelines

## Testing a script
A good sample text for testing (especially rarer) scripts is the Universal Declaration of Human Rights (UDHR), there are 487 translations at <https://unicode.org/udhr/> (unicode), the sample could then if needed be compared to one of the 530 translations available at <https://www.ohchr.org/EN/UDHR/Pages/SearchByLang.aspx> (pdf, html, sound).

## Emojis
- Emojis are located in `Base/res/emoji/` (repo) and `/res/emoji` (running SerenityOS)

- ~~New emoji should be added to [emoji.txt](https://github.com/SerenityOS/serenity/blob/master/Base/home/anon/Documents/emoji.txt)~~. New emojis are no longer required to be added to emoji.txt. This is automatically handled by a script during CI run.

- Emoji has the filename `U+{hex code}.png`, eg. `U+1F332.png`, emoji with multiple codepoints is separated with underscore, eg. `U+1F1EE_U+1F1F8.png`

- Emoji presentation selectors(**U+FE0F**) has to be excluded from the filename of emoji with multiple codepoints [#14917](https://github.com/SerenityOS/serenity/pull/14917) Polar Bear 🐻‍❄️ with the codepoints `U+1F43B U+200D U+2744 U+FE0F` gets the filename `U+1F43B_U+200D_U+2744.png`

- The size of emoji is 7 px width and always **10 px height**. Some kind of agreement was reached in #fonts to allow the width to be 7px, 8px, 9px, 10px when needed for complex emoji but the goal is to keep it 7x10 if possible.

- Emoji shall be optimized to remove unneccesarry meta-data, `optipng -strip all` is recommended. ~~(This does on occation render the emoji unvieweble in SerenityOS so it might be a good idea to check before making a PR!)~~ (Fixed in https://github.com/SerenityOS/serenity/pull/14910)

- Emojis are system-wide, no matter what font is used.

- There are currently issues with glyphs in the .font taking precedent over emojis and with Emoji picker(not all emojis showing).

- The commit message when adding emoji should contain the glyph, name and codepoint. You can automatically generate these with `Meta/generate-emoji-txt.sh Build/i686/UCD/emoji-test.txt /folder/to/the/emoji/you/have/made /the/file/you/want/the/list/of/emoji/in/the/right/format/commit.txt`

- Flag emoji: The visible part should, unlike the other emoji, be 10x7 if possible with transparant padding on the y-axis. Some flags is more suitable as 9x7, 10x6, etc. Some flexability is allowed.

![image](https://user-images.githubusercontent.com/93391300/194284891-1c18fb07-0f2a-46b5-9e06-2b1d775caea2.png)

*A 10x7 flag in a 10x10 canvas*


## Trivia
Katicabogárfélék is Hungarian for ladybug.

## Links
[Unicode charts [unicode.org]](https://www.unicode.org/charts/)

[SerenityOS Discord #fonts](https://discord.com/channels/830522505605283862/927893781968191508)

[Using our font in Browser](browser-for-developers.md#libweb-and-fonts)

## References
[^1]: [Under-ConScript Unicode Registry](https://www.kreativekorp.com/ucsur/)
[^2]: [Wikipedia: CJK Unified Ideographs](https://en.wikipedia.org/wiki/CJK_Unified_Ideographs)
