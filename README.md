# pmed-tex-preamble
LaTeX Preamble with macros, operators, and symbols for writing about Precision Medicion/Precision Health. The intended benefits of this file are to:
1. Make notation easy to change - To change the symbol for something one line in the preamble needs to be changed. Avoids find and replace  
2. Enhance document readability - Compare a) \val(\pol) vs. b) \mathcal{V}(\pi) . To understand (a) you have to remember the shorthand, while to understand (b) you have to remember the meaning of each symbol. 
3. Reduce typos - writing what you mean instead of the associated symbols can prevent inconsistencies like forgetting to wrap a character in \mathbb{} or \mathrm{}

# Suggested Usage
## Using the preamble in a project

If you are using the preamble in a paper do not clone this repository. Instead, download the preamble file directly to your project directory. 

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
