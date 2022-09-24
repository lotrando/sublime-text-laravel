# Sublime text setting for fast and easy developing in Laravel 

This is a complete Sublime-Text configuration guide for Laravel developers.

<!-- MarkdownTOC -->

- [Install Package Control](#install-package-control)
- [Install SyncSettings package](#install-sync-settings)
- [Install Emmet package](#install-emmet)
- [Install A File Icon package](#install-file-icons)
- [Install Material Theme package](#install-material-theme)
- [Install PHP Companion package](#install-phpcompanion)
- [Install Terminus package](#install-terminus)

<!-- /MarkdownTOC -->

<a id="install-package-control"></a>
## Install Package Control

Use one of the following methods to install Package Control

### Command Palette

    Open the command palette: Win/Linux: ctrl+shift+p, Mac: cmd+shift+p
    Type "Install Package Control" and press enter.

### Menu

    Open the Tools menu
    Select "Install Package Control"


<a id="install-sync-settings"></a>
## Install SyncSettings package

Open the command palette: Win/Linux: ctrl+shift+p, Mac: cmd+shift+p
Type "Install Package" and press enter
Type "SyncSettings" and press enter

## After install
Open the command palette: Win/Linux: ctrl+shift+p, Mac: cmd+shift+p
Type "Sync Settings:Edit User Settings" and press enter.
Edit User Settings

Use one of the following methods to install Package Control

### Create new gist
    Create an access token https://github.com/settings/tokens/new
    Put the token in the config file (access_token property)
    Run Sync Settings: Create and Upload command

### Do you already have a gist?

    Copy gist id and put it in config file (https://gist.github.com/<username>/<gist id>) (gist_id property)
    Run Sync Settings: Download command to retrieve your backup.
---
Config documentation: https://www.mfuentesg.dev/SyncSettings/
### My SyncSettinggs.sublime-settings file
    
    {
        "access_token": "ghp_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx",
        "gist_id": "xxxxxxxxxxxxxxxxxxxxxxxxx",
        "auto_upgrade": true,
        "excluded_files": [
            "*.png"
        ]
    }
---

<a id="install-emmet"></a>
## Install Emmet package

Open the command palette: Win/Linux: ctrl+shift+p, Mac: cmd+shift+p
Type "Install Package" and press enter
Type "Emmet" and press enter

## After install

Restart Sublime and enable telemetry

<a id="install-file-icons"></a>
## Install A File Icon package

Open the command palette: Win/Linux: ctrl+shift+p, Mac: cmd+shift+p
Type "Install Package" and press enter
Type "A File Icon" and press enter

## After install

Open the command palette: Win/Linux: ctrl+shift+p, Mac: cmd+shift+p
Type "Preferences:A File Icon Settings" and press enter.
Edit User Settings

---
### My - A File Icon.sublime-settings file
    {
        "opacity": 0.7,
        "opacity_on_hover": 0.8,
        "opacity_on_select": 1.0,
    }
---

<a id="install-material-theme"></a>
## Install Material Theme package

Open the command palette: Win/Linux: ctrl+shift+p, Mac: cmd+shift+p
Type "Install Package" and press enter
Type "Material Theme" and press enter

## After install

Edit Preference.sublime-settings file

---
### My Preference.sublime-settings file
    {
      "update_check": false,
      "margin": 10,
      "tab_size": 2,
      "translate_tabs_to_spaces": true,
      "highlight_line": true,
      "caret_extra_top": 2,
      "caret_extra_bottom": 2,
      "caret_extra_width": 2,
      "line_padding_top": 2,
      "line_padding_bottom": 1,
      "auto_complete_delay": 10,
      "hide_new_tab_button": true,
      "show_sidebar_button": false,
      "ui_scale": 1.0,
      "hardware_acceleration": "opengl",
      "remember_full_screen": true,
      "remember_workspace": true,
      "remember_layout": false,
      "font_face": "jetBrains Mono Semibold",
      "font_size": 12,
      "font_options":["dlig", "ss01"],
      "theme": "Material-Theme.sublime-theme",
      "color_scheme": "Packages/Material Theme/schemes/Material-Theme.tmTheme",
      "material_theme_accent_lime": true,
      "material_theme_accent_scrollbars": true,
      "material_theme_accent_titlebar": true,
      "material_theme_compact_panel": true,
      "material_theme_compact_sidebar": true,
      "material_theme_small_statusbar": true,
      "material_theme_small_tab": true,
      "material_theme_tabs_autowidth": true,
      "material_theme_titlebar": true,
      "material_theme_tabs_separator": true,
      "ignored_packages":
      [
            "Vintage",
      ],
    }
---
### My Material-Theme.sublime-theme file

    "rules": [
        {
          "class": "sidebar_label",
          "font.face": "jetBrains Mono Semibold",
          "font.size":  12,
        },
        {
          "font.face": "jetBrains Mono Semibold",
          "class": "sidebar_heading",
          "color": [200, 200, 200, 0.5],
          "font.bold": true,
          "font.size": 12,
        },
    ],
---

<a id="install-docblockr"></a>
## Install DocBlockr package

Open the command palette: Win/Linux: ctrl+shift+p, Mac: cmd+shift+p
Type "Install Package" and press enter
Type "DocBlockr" and press enter

## After install

Change this line in Base File.sublime-settings file

---
### My Preference.sublime-settings file
    {
        "jsdocs_spacer_between_sections": "after_description",
    }
---

<a id="install-phpcompanion"></a>
## Install PHP Companion package

Open the command palette: Win/Linux: ctrl+shift+p, Mac: cmd+shift+p
Type "Install Package" and press enter
Type "PHP Companion" and press enter

## After install

Change this line in Default(windows).sublime-keymap file

---
### PHP Companion keymaps in my - Default (windows).sublime-keymap file
    {
        { "keys": ["ctrl+alt+g"], "command": "import_namespace" },
        { "keys": ["ctrl+alt+i"], "command": "find_use" },
        { "keys": ["ctrl+alt+e"], "command": "expand_fqcn" },
        { "keys": ["ctrl+alt+c"], "command": "insert_php_constructor_property" },
    }
---

<a id="install-terminus"></a>
## Install Terminus package

Install Gitbash from https://github.com/git-for-windows/git/releases/download/v2.37.3.windows.1/Git-2.37.3-64-bit.exe

Open the command palette: Win/Linux: ctrl+shift+p, Mac: cmd+shift+p
Type "Install Package" and press enter
Type "Terminus" and press enter

## After install

Changes in Default (windows).sublime-keymap file for toggling explorer panel and terminus.

---
### Terminus and panel keymaps in my - Default (windows).sublime-keymap file
    [
        ...

        { "keys": ["ctrl+1"], "command": "toggle_side_bar" },

        { "keys": ["ctrl+`"], "command": "toggle_terminus_panel"},
        { "keys": ["ctrl+alt+t"], "command": "terminus_open", "args": {"cwd": "${file_path:${folder}}"}},

        ...
    ]

Changes Terminus.sublime-setting file.

---

### Terminus changes in my - Terminus.sublime-setting file

    {
        "default_config": {
            "windows": "gitbash"
        },

        "shell_configs": [
            {
                "name": "gitbash",
                "title": "Bash",
                "cmd": "C:\\Program Files\\Git\\bin\\bash.exe",
                "env": {},
                "enable": true,
                "platforms": ["windows"]
            },
        ],
        "256color": true,
        "brighten_bold_text": true,
        "unix_term": "xterm-256color",
        "unix_lang": "us.UTF-8",
        "scrollback_history_size": 20000,
        "min_columns": 20,
        "max_columns": 420,
        "natural_keyboard": true,
        "theme": "adaptive",
        "view_settings": {
            "font_face": "JetBrains Mono Semibold",
            "font_size": 10,
        },
    }
---

<a id="install-color-highlight"></a>
## Install Color Highlight package

Open the command palette: Win/Linux: ctrl+shift+p, Mac: cmd+shift+p
Type "Install Package" and press enter
Type "Color Highlight" and press enter

## After install

Add  Highlight.sublime-settings

---
### Changes in my - Highlight.sublime-settings file
    {
      "user": {
        "gutter_icon": "circle",
        "highlight_values": false,
      }
    }
---

<a id="install-color-highlight"></a>
## Install Color Highlight package

Open the command palette: Win/Linux: ctrl+shift+p, Mac: cmd+shift+p
Type "Install Package" and press enter
Type each

Laravel Blade AutoComplete
Laravel Blade Highlighter
Laravel Blade Spacer
Tailwind CSS
Tailwind CSS Autocomplet
LSP
LSP-bash
LSP-css
LSP-html
LSP-intelephense
LSP-json
LSP-tailwindcss
LSP-vue

and press enter
