# mcedit-syntax-json
This package can be used to generate mcedit (Midnight Commander) syntax file for JSON (.json) file format highlighting.

## Adding into mcedit
You can generate new json.syntax with different color scheme

Copy the json.syntax into your syntax folder `/usr/share/mc/syntax/`, or if you are using user-specific configuration, than `$HOME/.local/share/mc/mcedit/`.

You need to register new file type in your `Syntax` file, by adding following lines before `unknown` file type

    file ..\*\\.(tf|tfvars)$ Terraform
    include tf.syntax

`Syntax` file usually can be found in `/usr/share/mc/syntax/Syntax` or `$HOME/.config/mc/mcedit/Syntax`

## Preview
![JSON_syntax_highlighter_for_mcedit](https://github.com/neosy/mcedit-syntax-json/assets/105918329/497c637a-2826-4f3e-bbe5-ce76d2765661)

# Other
If you want to get default black background color, edit `$HOME/.config/mc/ini` and change `basecolor` to

    base_color=editnormal=default,black:editwhitespace=default,red
