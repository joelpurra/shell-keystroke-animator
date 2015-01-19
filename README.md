# [shell-keystroke-animator](https://github.com/joelpurra/shell-keystroke-animator)

<p align="center">
  <a href="https://github.com/joelpurra/shell-keystroke-animator"><img src="https://cloud.githubusercontent.com/assets/1398544/5838453/e57ac372-a187-11e4-90f6-b2b498c457b0.gif" alt="shell-keystroke-animator Terminal demo" border="0" /></a>
</p>

<p align="center">
  <a href="https://github.com/joelpurra/shell-keystroke-animator"><img src="https://cloud.githubusercontent.com/assets/1398544/5838460/f034cda8-a187-11e4-8836-489c4ba94751.gif" alt="shell-keystroke-animator TextEdit demo" border="0" /></a>
</p>

<p align="center">
  <a href="https://github.com/joelpurra/npshell/"><img src="https://cloud.githubusercontent.com/assets/1398544/5836151/b8d8e31e-a171-11e4-8412-d23765b54a25.gif" alt="npshell in action" border="0" /></a>
</p>

Simulate stroking keys, based on characters from `stdin`, while taking screenshots to create a `.gif` animation.

Create repeatable, editable, automatable example usage of:

- Terminal/shell programs.
- Code snippets.
- Proof-of-concept for hacks.
- Other text input.



## Usage

```bash
cat "my-keys.txt" | keystroke-animator [countdown [keysleep [linesleep]]]
```

- `my-keys.txt` Sequence of keys/characters to "type", one by one.
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
