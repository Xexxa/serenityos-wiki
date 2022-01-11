# Fonts in SerenityOS

| Family            |Size    |Format|Serif |Monospace |Regular |Italic |Bold Italic |Bold |Black
| ---               |:---    |:---: |:---: |:---:     |:---:   |:---:  |:---:       |:---:|:---:
| Csilla            |10/12   | .font|      | ✔️       | ✔️     |       |            | ✔️  | 
| Katica            |10/12   | .font|      |          | ✔️     |       |            | ✔️  | 
| Liberation Serif  |8-36    | .ttf | ✔️   |          | ✔️     | ✔️    | ✔️          | ✔️  |
| Liza              |10/24/36| .font|      | ✔️       | ✔️     |       |            | ✔️  | ✔️
| Marieta           |24/36   | .font|      |          | ✔️     |       |            | ✔️  | 
| Pabbleton         |14      | .font|      |          | ✔️     |       |            | ✔️  | 
| SerenitySans      |8-36    | .ttf |      |          | ✔️     |       |            |     |
| Serifina          |10      | .font| ✔️   |          |        |✔️     |            |     |
| Tiny              |6       | .font|      |          | ✔️     |       |            |     |

## Creating a font
- Always include character FFFD &#xfffd; (https://www.unicode.org/charts/PDF/UFFF0.pdf), it's the fallback character if a glyph is missing.
- Give the font a filename in the following format NameStyleSize.ext (examples: KaticaRegular10.font)
- If the font is primarly or exclusively for CJK characters then prefix the family with CJK and space "CJK Name" 

## General design guidelines


## Links
[Unicode charts [unicode.org]](https://www.unicode.org/charts/)
[SerenityOS Discord #fonts](https://discord.com/channels/830522505605283862/927893781968191508)
