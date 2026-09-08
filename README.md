# Maxon Homebrew tap

```bash
brew install maxon-lang/tap/maxon
```

Installs the [Maxon](https://maxon.dev) compiler — a systems language whose compiler is written in
itself. `maxon` lands on your PATH immediately; no shell restart, and no Gatekeeper warning, because
Homebrew clears the quarantine attribute a downloaded archive would carry.

Verify it:

```bash
maxon --version
```

## What gets installed

The compiler reads its standard library from source and finds it by walking up from its own
executable, so the whole tree is installed into the formula's `libexec` and `bin/maxon` is a symlink
into it. That is deliberate: installing the binary alone would leave it with no standard library.

## Contents

`Formula/maxon.rb` is **generated** — by `installer/homebrew/generate.sh` in
[maxon-lang/maxon](https://github.com/maxon-lang/maxon), from the SHA256 of the published release
archive. Edit it there, not here.
