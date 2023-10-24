# mcedit-syntax-json
This package can be used to generate mcedit (Midnight Commander) syntax file for JSON (.json) file format highlighting.

## Installation
### Manually
Manual installation can be done by copying the `json.syntax` into file to your syntax folder (a or b)

a) Global syntax foldre `/usr/share/mc/syntax/`

    $ cp ./syntax/json.syntax /usr/share/mc/syntax

You need to register new file type in your `Syntax` file, by adding following lines before `unknown` file `/usr/share/mc/syntax/Syntax` 

Insert the text:

    file ..\*\\.json$ JSON\sFile
    include json.syntax    

b) User-specific configuration, `~/.local/share/mc/mcedit/`

    $ mkdir -p ~/.local/share/mc/syntax
    $ cp ./syntax/json.syntax ~/.local/share/mc/syntax

You need to register new file type in your `Syntax` file.

Create the file `Syntax`

    $ >>~/.local/share/mc/syntax/Syntax
    $ chmod 644 ~/.local/share/mc/syntax/Syntax

Insert the text:

    file ..\*\\.json$ JSON\sFile
    include /home/<user>/.local/share/mc/syntax/json.syntax

`Syntax` file usually can be found in `/usr/share/mc/syntax/Syntax` or `$HOME/.config/mc/mcedit/Syntax`

### Using a script
To install, run the script

    $ sudo ./mc_syntax-install.sh

## Preview
![JSON_syntax_highlighter_for_mcedit](https://github.com/neosy/mcedit-syntax-json/assets/105918329/497c637a-2826-4f3e-bbe5-ce76d2765661)

# Other
If you want to get default black background color, edit `$HOME/.config/mc/ini` and change `basecolor` to

    base_color=editnormal=default,black:editwhitespace=default,red

## License
The contents of this package uses the same license as Midnight Commander, the GPLv2 or higher.
