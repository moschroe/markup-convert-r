# MCR - Markup ConvertR

An experiment in adapting some markup languages.

You are running a WASM version of a command line binary. Press `[enter]` in top input field to execute and then hopefully help should tell you everything else. Have fun exploring

## Features

- Converting to and from different markup formats. Not every combination works, especially XML will be buggy and does not conserve the structure 1:1.
- Nested decoding of contents (b64, nested markup, PHP `serialize()` output)
- in YAML output, optionally render strings as multiline strings (if at least one `\n` occurs). Will greatly improve legibility for any plaintext embedded in markup fields
- Optionally sort keys and, on a second level, sort arrays.

  `float` values are sorted as well, any uncomparable values are treated as if equal (in Rust `f32`/`f64` only partially implement equality).