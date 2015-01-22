# [shell-keystroke-animator](https://github.com/joelpurra/shell-keystroke-animator)

Simulate stroking keys, based on characters from `stdin`, while taking screenshots of the application window to create a `.gif` animation.

Create repeatable, editable, automatable example usage of:

- Terminal/shell programs.
- Code snippets.
- Proof-of-concept for hacks.
- Other text input.



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
  <a href="https://github.com/joelpurra/npshell/">
    <img src="https://cloud.githubusercontent.com/assets/1398544/5836151/b8d8e31e-a171-11e4-8412-d23765b54a25.gif" alt="npshell in action" border="0" />
  </a>
</p>



## Usage

Running the software creates a series of `.png` images, and an `output.gif`.

```bash
cat "my-keys.txt" | keystroke-animator [--no-shadow] [countdown [keysleep [linesleep]]]
```

- `my-keys.txt` Sequence of keys/characters to read from `stdin` and then "type", one by one.
- `--no-shadow` Turn off application window shadows (optional). Useful if the background of the window isn't white.
- `countdown` Pre-script countdown, in integer seconds (optional).
- `keysleep` Time to sleep between keys, in seconds (optional).
- `linesleep` Time to sleep between lines, in seconds (optional).



## Limitations

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
