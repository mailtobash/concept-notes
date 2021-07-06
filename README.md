# Newline characters
![Typewriter works](https://cdn.dribbble.com/users/1000955/screenshots/2993972/ezgif.com-gif-maker.gif)

## Operating system
Windows - `\r\n`  
MAC - `\r`     
Linux- `\n`

## Impacts on a developer ##
- Code - autocrlf
    - `git config --global core.autocrlf` ==> input for MAC
    - `git config --global core.autocrlf` ==> auto for Windows

- Processing files 
```System.setProperty("line.separator","\r\n"); // Java
f = open('/tmp/'+filename, 'w', newline='\n') # Python
```

- VI - `:se list` you will see `^M` character. That means this file is from a DOS/Windows origin.
- Editors - smart, they look after it. Dont use old editor.

### Pointers:
1. Set up your crlf in git config
2. Consider line endings when reading files
3. Think of consumer/audience when writing them - especially for data we pass to people.
4. Give files in a format that does not have these limitations (CSV)
