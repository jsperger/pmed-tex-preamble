# pmed-tex-preamble
LaTeX Preamble with macros, operators, and symbols for writing about Precision Medicion/Precision Health using semantic commands. Write what you mean, not the markup


Syntactic: A policy $\pi$
\newcommand{\pol}{\pi} %policy
Semantic: A policy $\pol$


Syntactic: The estimated policy $\widehat{\pi}$
\newcommand{\polhat}{\widehat{\pol}} % notice the use of our previously defined command \pol 
Semantic: The estimated policy $\polhat$

$\widehat{\mathcal{V}}(\widehat{\pi})$

$\valhat{\polhat}

Even better might be 

Syntactic: \textit{Clostridium}
\newrobustcmd*{\est}[1]{\widehat{#1}}%
Semantic: \est{val} (\est{\pol})

The intended benefits of this file are to:
1. Make notation easy to change - To change the symbol for something one line in the preamble needs to be changed. Avoids find and replace which is liable to break in unforeseen ways. 

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
