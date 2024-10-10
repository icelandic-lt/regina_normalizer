<!-- omit in toc -->
# Regina Normalizer

![Version](https://img.shields.io/badge/Version-T9-darkviolet)
![Python](https://img.shields.io/badge/python-3.8-blue?logo=python&logoColor=white)
![CI Status](https://img.shields.io/badge/CI-[unavailable]-red)
![Docker](https://img.shields.io/badge/Docker-[unavailable]-green)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow)

Regina is a tool for normalization of Icelandic text in preparation for conversion to speech. Normalization involves converting numbers,
dates, ordinals, etc. into fully spelled-out alphabetic words.

## Overview

This repository was created at Reykjavík University and is
part of the [Icelandic Language Technology Programme](https://github.com/icelandic-lt/icelandic-lt).

- **Category:** [TTS](https://github.com/icelandic-lt/icelandic-lt/blob/main/doc/tts.md)
- **Domain:** Server
- **Languages:** Python (but dependencies need Rust)
- **Language Version/Dialect:**
  - Python: 3.8+
- **Audience**: Developers, Researchers
- **License**: MIT
- **Origins:** [regina_normalizer](https://github.com/cadia-lvl/regina_normalizer)

## Status
![Not installable](https://img.shields.io/badge/Not_Installable-red)

The Regina Normalizer is not presently installable. An error
occurs during installation having to do with an incompatible Rust/Cargo
configuration required for the indirect `crossbeam-deque v0.8.5` dependency.

## System Requirements
- Operating System: Linux
- Disk Space: >1.7 GB
- Rust installed

## Description

*(Original documentation below)*

**Dependencies**

`pip install git+https://github.com/cadia-lvl/POS.git@v3.1.0`

`pip install wandb`

Run `pip install regina-normalizer`

In a python shell, run:

`import regina_normalizer.normalizer`

**Input string**

`normalizer.input_string({text_string}, {domain})`

Example:

`normalizer.input_string("Leikurinn fór 2-2 fyrir KR.", "sport")`


\>\>\> Leikurinn fór tvö tvö fyrir K R .

**Input file**

`normalizer.input_file({input_file}, {output_file}, "other")`

Example:

`normalizer.input_file("input.txt", "output.txt", "other")`

input.txt:

```
Þetta þarf að norma a.m.k. 2x. Ég verð 3ja ára í sumar.
Símanr er 888-3492, en hjá þér?
Þetta ætti að taka 2-3 klst.
```

output.txt

```
Þetta þarf að norma að minnsta kosti tvö x . Ég verð þriggja ára í sumar . Símanúmer er átta átta átta <sil> þrír fjórir níu tveir , en hjá þér ? Þetta ætti að taka tvö til þrjár klukkustundir .
```




