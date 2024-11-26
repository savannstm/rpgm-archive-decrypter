# rpgm-archive-decrypter

RPGM Archive Decrypter is a [RPG Maker Decrypter](https://github.com/uuksu/rpgmakerdecrypter) rewrite in Rust (**_BLAZINGLY FAST_** :fire:).
It can be used to extract encrypted archives of RPG Maker XP/VX/VXAce game engines.
It is faster and lighter than RPG Maker Decrypter, and also has **NO** requirements to run, except a working PC.

_And also features much more cleaner code!_

## Installation

Get required binaries in Releases section.
One with `.exe` extension is for Windows, without it - is for Linux.

## Usage

Call `rpgmad -h` for help.

```text
A tool to extract encrypted .rgss RPG Maker archives.

Usage: rpgmad.exe [OPTIONS]

Options:
  -i, --input-file <input-path>
          Path to the RGSSAD file. [default: ./]
  -o, --output-dir <output-path>
          Path to put output files. [default: ./]
  -f, --force
          Forcefully overwrite existing Data, Graphics and other files.
  -h, --help
          Prints the help message.
```

For example, to extract archive to same same directory where it exists:
`rpgmad C:/RPGMakerGame/Archive.rgssad`.

You can recongnize archives by their extensions: `rgssad`, `rgss2a`, `rgss3a`.

## GUI

Full-featured GUI will maybe come out someday. Not sure in a relevancy.

## Development

### Building

Requirements: `rustup` with installed Rust toolchain, linker (`gcc`, `llvm` or `msvc`).

Clone the repository and compile with `cargo b -r`.

### Tests

I'm not really skilled in tests, but the validity of output files is tested the following ways:

-   Of images, using image viewers.
-   Of rx/rvdata files, using [rvpacker-txt-rs](https://github.com/savannstm/rvpacker-txt-rs).

As long as these tests succesful, there shouldn't be any bugs.

## License

Project is licensed under WTFPL.
