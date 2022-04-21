# User guide
## Keyboard shortcuts

| Shortcut | Action |
| ---: | --- |
| `✲ Ctrl` + `⎇ Alt` + `Space` | Open emoji picker |
| `⌘ Super` + `Space` | Open assistant |
| `F2` | Rename file |
| `⌘ Super` + `↓ Down` | Minimize window |
| `⌘ Super` + `↑ Up` | Maximize window |
| `⌘ Super` + `← Left` | Tile window left |
| `⌘ Super` + `→ Right` | Tile window right |
| `⌘ Super` + `↹ Tab` | Cycle between windows |
| `⇧ Shift` + `⎇ Alt` | Hold shift and press alt to toggle keymaps |
| `✲ Ctrl` + `⇧ Shift` + `A` | Command Palette (inside software) |

## Settings
### Settings window has several sub-categories on which to choose from.
![](images/settings.png)

## Browser 
### Browser settings - Personalize browser settings through his window.
![](images/browser_settings_browser_tab.png)
![](images/browser_settings_content_filtering_tab.png)

## Clock
### Clock settings - Choose time format and timezone.
![](images/clock_settings_clock_tab.png)
![](images/clock_settings_time_zone_tab.png)

## Display
### Display settings - change background, themes, fonts, monitor size and number of virtual workspaces.
![](images/display_settings_background_tab.png)
![](images/display_settings_themes_tab.png)
![](images/display_settings_fonts_tab.png)
![](images/display_settings_monitor_tab.png)
![](images/display_settings_workspaces_tab.png)

## Keyboard
### Keyboard settings - update keyboard properties and keymap.
![](images/keyboard_settings_keyboard_tab.png)
![](images/keyboard_settings_add_a_keymap_dropdown_list.png)

## Mail
### Mail settings - provide important values in order for the mail program to work.
![](images/mail_settings_mail_tab.png)

## Mouse
### Mouse settings - modify mouse properties and personalize cursor theme.
![](images/mouse_settings_mouse_tab.png)
![](images/mouse_settings_cursor_theme_tab.png)

## Terminal
### Terminal settings - update terminal behavior, layout and font style.
![](images/terminal_settings_terminal_tab.png)
![](images/terminal_settings_view_tab.png)


## Insert Unicode

_How to insert Unicode that's not covered in one of the keyboard character mapping file._

__Option 1: Copy character from Font Editor__

Select the character you want in Font Editor and press `✲ Ctrl` + `⇧ Shift` + `C` to copy the character.

__Option 2: Copy character in terminal__
1. Open Terminal
2. `copy "\u000000a5"`
3. Character ` ✲ ` is now in clipboard, `Ctrl` + `V` to paste it somewhere

__Option 3: Create character in terminal using js__
1. Open Terminal
2. Type `js`
3. Use console.log to generate character from hex, if you want the ¥ yen sign character type `console.log("\u00A5");`
4. Copy the character `✲ Ctrl` + `⇧ Shift` + `C`

![](images/user-guide__terminal-js-copy-character.png)
