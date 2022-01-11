# Fonts in SerenityOS

| Family            |Default for    |Size    |Format|Serif |Monospace |Regular |Italic |Bold Italic |Bold |Black|Author
| ---               |:---           |:---    |:---: |:---: |:---:     |:---:   |:---:  |:---:       |:---:|:---:|:---
| Cathode           |               |10      | .font|      | ✔️       | ✔️     |       |            |     |      | [@electrikmilk](https://github.com/electrikmilk)
| CJK Biáng         |               |36      | .font| ?    | ✔️       | ✔️     |       |            |     |      | [@Xexxa](https://github.com/Xexxa)
| Csilla            |.txt           |10/12   | .font|      | ✔️       | ✔️     |       |            | ✔️  |       |
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
- Always include character FFFD &#xfffd; (https://www.unicode.org/charts/PDF/UFFF0.pdf), it's the fallback character if a glyph is missing.
- Give the font a filename in the following format NameStyleSize.ext (examples: KaticaRegular10.font)
- If the font is primarly or exclusively for CJK characters then prefix the family with CJK and space "CJK Name" 

## General design guidelines


## Links
[Unicode charts [unicode.org]](https://www.unicode.org/charts/)

[SerenityOS Discord #fonts](https://discord.com/channels/830522505605283862/927893781968191508)
