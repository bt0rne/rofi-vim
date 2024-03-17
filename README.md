# rofi-vim

## A Vim cheat sheet for _Rofi_ or _dmenu_

I wanted to create a quick searchable Vim cheat sheet, and I decided to use a
text file as the cheat sheet and then pipe that to a _Rofi_ dmenu.

## Example

If you have _Rofi_ installed you can try it out like this:

```bash
curl -s https://raw.githubusercontent.com/rdvm/rofi-vim/master/vimcheat | rofi -dmenu -p "Vim action" -i -theme-str 'window {width: 98%;}' -theme-str 'window {location: north;}'
```

Or if you have _dmenu_ installed:

```bash
curl -s https://raw.githubusercontent.com/rdvm/rofi-vim/master/vimcheat | dmenu -i -l 30
```

## Instuctions

The `rofi-vim` file in this repository is the script I use on my system to
launch the cheat sheet. You can place the script somewhere in the `$PATH` on
your system to be able to call it from anywhere or by using a key-binding.

The script will download the cheat sheet file from this repo and cache it
locally so it only needs to be downloaded once. When you run `rofi-vim` it will
automatically fetch a fresh copy if the current cached copy is more than 30 days
old.

### Using with _Rofi_ and _dmenu_

There is an optional `--dvim` argument if you want to use _dmenu_ instead of
_Rofi_, and if no argument is supplied it will use _Rofi_ by default.
