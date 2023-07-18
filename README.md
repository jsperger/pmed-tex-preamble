# pmed-tex-preamble
LaTeX Preamble with macros, operators, and symbols for writing about Precision Medicion/Precision Health. The intended benefits of this file are to:
1. Make notation easy to change - To change the symbol for something one line in the preamble needs to be changed. Avoids find and replace  
2. Enhance document readability - Compare a) `\val(\pol)` vs. b) `\mathcal{V}(\pi)` . To understand (a) you have to remember the shorthand, while to understand (b) you have to remember the meaning of each symbol. 
3. Reduce typos - writing what you mean instead of the associated symbols can prevent inconsistencies like forgetting to wrap a character in `\mathbb{}` or `\mathrm{}`

# Suggested Usage
## Using the preamble in a project

If you are using the preamble in a paper do not clone this repository. Instead, 
1. Download the preamble file (`pmed-tex-preamble.tex`) directly to your project directory.
2. Then insert `\input{pmed-tex-preamble.tex}` somewhere before the `\begin{document}` command.
3. Modify the commands to suit your needs by changing the output to what you desire or adding your own shorthand.
4. You can compile the two overview tex files to view the current symbols (`overview-output.tex`) or the current symbols with the commands to produce them (`overview-commands-plus-output.tex`). These will automatically update based on changes to the output of the current commands. These will not automatically include additional functions that you add.

## Contributing to the project

Git clone is appropriate here. 

### Notes on Contributing

Define downstream quantities using the commands defined up stream. 

Good: 

\DeclareMathOperator{\val}{{\mathcal{V} }} % value function

\DeclareMathOperator{\valhat}{{\widehat{\val}}} % estimated value function

Bad:

\DeclareMathOperator{\val}{{\mathcal{V}}} % value function

\DeclareMathOperator{\valhat}{{\widehat{\mathcal{V} }}} % estimated value function

Commands for operators and symbols should use all lower case letters

Commands changing the font for a character should use lower case letters for the portion of the command representing the style and a character matching the desired output  i.e. an upper-case letter if the output will be an upper-case letter. 

Good:\mbbR for \mathbb{R} 

Bad: \mbbr for \mathbb{R}
