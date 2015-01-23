<p align="center">
  <a href="https://github.com/joelpurra/shell-keystroke-animator">
    <img src="https://cloud.githubusercontent.com/assets/1398544/5870690/b476196a-a2d2-11e4-885b-1532bea27749.gif" alt="shell-keystroke-animator in action" border="0" />
  </a>
</p>


# [shell-keystroke-animator](https://github.com/joelpurra/shell-keystroke-animator)

Simulate stroking keyboard keys into another application/window while taking screenshots to create a `.gif` animation.

Create repeatable, editable, automatable example usage of:

- Terminal/shell programs.
- Code snippets.
- Proof-of-concept for hacks.
- Other text input.



## Installation

### On Mac with Homebrew

```bash
brew tap joelpurra/joelpurra
brew install shell-keystroke-animator
```

### On other systems

Clone or download, then either use `shell-keystroke-animator/src/keystroke-animator` directly where you put it, or symlink `keystroke-animator`.



## Examples

<p align="center">
  <a href="https://cloud.githubusercontent.com/assets/1398544/5851864/9f8eb82e-a20d-11e4-9c05-a33de1558be3.gif">
    <img src="https://cloud.githubusercontent.com/assets/1398544/5851864/9f8eb82e-a20d-11e4-9c05-a33de1558be3.gif" alt="shell-keystroke-animator Google search demo" width="50%" border="0" />
  </a>
</p>

<p align="center">
  <a href="https://github.com/joelpurra/shell-keystroke-animator">
    <img src="https://cloud.githubusercontent.com/assets/1398544/5851982/9e88415a-a20f-11e4-8976-9a3fedeb54a0.gif" alt="shell-keystroke-animator Terminal demo" border="0" />
  </a>
</p>

<p align="center">
  <a href="https://github.com/joelpurra/jqnpm">
    <img src="https://cloud.githubusercontent.com/assets/1398544/5852881/aaefa09c-a21d-11e4-9e7b-7c2c5574e0b6.gif" alt="jqnpm in action" border="0" />
  </a>
</p>

<p align="center">
  <a href="https://github.com/joelpurra/shell-keystroke-animator">
    <img src="https://cloud.githubusercontent.com/assets/1398544/5851871/cc05ff3e-a20d-11e4-9a60-cdea5c6cf346.gif" alt="shell-keystroke-animator TextEdit demo, with a shadow" border="0" />
  </a>
</p>

<p align="center">
  <a href="https://github.com/joelpurra/shell-keystroke-animator">
    <img src="https://cloud.githubusercontent.com/assets/1398544/5851868/c1023710-a20d-11e4-9a0e-fd4bd54d3b9b.gif" alt="shell-keystroke-animator TextEdit demo, without a shadow" border="0" />
  </a>
</p>

<p align="center">
  <a href="https://github.com/joelpurra/npshell">
    <img src="https://cloud.githubusercontent.com/assets/1398544/5836151/b8d8e31e-a171-11e4-8412-d23765b54a25.gif" alt="npshell in action" border="0" />
  </a>
</p>


## Usage

Quickly focus another application/window, where you want your keystrokes to go and animation be created from, as soon as you've started `keystroke-animator`.

Running the software creates a series of `.png` images, and an `output.gif` in the same folder you started it from (`$PWD`).


```bash
cat "my-keys.txt" | keystroke-animator [--no-shadow] [countdown [keysleep [linesleep [endsleep]]]]
```


- `my-keys.txt` Sequence of keys/characters to read from `stdin` and then "type", one by one.
- `--no-shadow` Turn off application window shadows (optional). Useful if the background of the window isn't white.
- `countdown` Pre-script countdown, in integer seconds (optional).
- `keysleep` Time to sleep between keys, in seconds (optional).
- `linesleep` Time to sleep between lines, in seconds (optional).
- `endsleep` Time to sleep at the end of the animation, in seconds (optional).



## Limitations

- Doesn't work great with Terminal commands which take longer than `linesleep` to execute fully.
- The software isn't designed to handle special characters. Only linebreaks (`\n`) are treated differently, and is sent as the <kbd>&crarr;</kbd> (return) key.
- Tested on Mac OS X 10.10 Yosemite - please add support for any other platforms you like!

## Kudos

- [`ttygif`](https://github.com/icholy/ttygif) and [`ttyrec`](https://github.com/mjording/ttyrec)For inspiration. Shame I couldn't get those programs to work properly.
- [houbysoft's](http://houbysoft.com) [AskDifferent answer](http://apple.stackexchange.com/a/63899) to the question [Can a Mac be programmed to simulate pressing a key at a certain rate via software?](http://apple.stackexchange.com/questions/63897/can-a-mac-be-programmed-to-simulate-pressing-a-key-at-a-certain-rate-via-softwar)



---

## License
Copyright (c) 2015 Joel Purra <http://joelpurra.com/>
All rights reserved.

When using **shell-keystroke-animator**, comply to the MIT license. Please see the LICENSE file for details.
