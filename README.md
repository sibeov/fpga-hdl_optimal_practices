# 1. Introduction
Inspired by Jason Turners book [Cpp - Best Practices](https://github.com/cpp-best-practices/cppbestpractices) and the
fact that the initial author (@sibeov) miss something similar. This is an attempt to develop a forever changing,
open-source and free book discussing, evaluating and always having up-to-date best practices in accordance with the
FPGA-development industry. It is no attempt to rival similar books and is also something which started as a hobby and 
knowledge base for the initial author. This README and the project in general is currently in the EXTREMLY early stages and is still work-in-progress.

# 2. Table of Content
- [1. Introduction](#1-introduction)
- [2. Table of Content](#2-table-of-content)
- [3. Scope](#3-scope)
- [4. About](#4-about)
	- [4.1. Intention and goals](#41-intention-and-goals)
	- [4.2. FPGA- vs ASIC-development](#42-fpga--vs-asic-development)
	- [4.3. HDLs](#43-hdls)
- [5. Contributions](#5-contributions)
	- [5.1. How](#51-how)
- [6. Building the document](#6-building-the-document)
	- [6.1. Dependencies](#61-dependencies)
		- [6.1.1. Windows](#611-windows)
		- [6.1.2. Linux - Ubuntu](#612-linux---ubuntu)
	- [6.2. Build](#62-build)

# 3. Scope
See `scope.md` in `doc` directory.

# 4. About

## 4.1. Intention and goals
The hope and intention is for this book-(project) to be driven by FPGA-communities (all over the world) and the
industry.

## 4.2. FPGA- vs ASIC-development
The initial author has currently no background in ASIC-development, but there should be noe problem in having both
branches of the industry included.

## 4.3. HDLs
The book is HDL-agnostic, meaning that VHDL, (System)verilog etc shall be equally represented with source-code examples
and discussions. For the moment, only (System)verilog and VHDL will be represented in the book. But this (with
intention) and the rest of this project/book is prone to change.

# 5. Contributions
See `specifications.md` in `doc` folder for more info with regards to rules and structure of book.

## 5.1. How
1. Debugging and writing LaTex (if needed).
2. Provide source-code examples.
3. Translating source-code examples to other HDLs
   * Like SystemVerilog -> VHDL and vica versa.
4. Spell-checking and proof-writing.
5. Formalizing the rules and specifications of the book and also:
   * Reviews of rules and specifications
6. Provide suggestions to topics to include in the book.

# 6. Building the document

## 6.1. Dependencies

### 6.1.1. Windows
- MikTex
	- [Install MikTex](https://miktex.org/howto/install-miktex)
  		```shell
  		winget install miktex
  		```
- pygments
	```shell
	pip install pygments
	```

### 6.1.2. Linux - Ubuntu
- TexLive
  ```shell
  sudo apt-get install texlive-full
  ```
- pygments
  ```shell
  python3 -m pip install pygments
  ```

## 6.2. Build
Should be the same for all OSs.
```
# Clone repo
git clone <repo_url> [<local_repo_path>]
cd <local_repo_path>/tex
# Initialize continous latexbuild process
latexmk -pdf -pvc -outdir=../out -shell-escape top.tex
```