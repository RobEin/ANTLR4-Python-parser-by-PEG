# ANTLR4 parser for Python 3.13.1 &nbsp; [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

### About files:
 - PythonParser.g4
   - is the ANTLR4 parser grammar that based on the official [Python PEG grammar](https://docs.python.org/3.13/reference/grammar.html)

 - PythonLexerBase class
    - handles the Python indentations
    - creates encoding token
    - tokenizes fstring literals
    - and manage many other things

- Example files: [Python 3.13.1 Standard Lib](https://github.com/python/cpython/tree/3.13/Lib)

### Recent changes:
- parser grammar update for Python 3.13.1
- added ENCODING token
- complete rewrite of fstring tokenizer in lexer grammar and PythonLexerBase class
  - now correctly tokenizes the followings in fstring:
      - escape sequences
      - walrus operator
      - dictionary comprehension
      - set comprehension
- soft keywords changes:
  - no embedded code (semantic predicates) in parser grammar for soft keywords
  - no need for PythonParserBase class
  - no need for transformGrammar.py
  - BREAKING CHANGES:
    - dedicated tokens for soft keywords (instead of NAME token):
      - NAME_OR_TYPE
      - NAME_OR_MATCH
      - NAME_OR_CASE
      - NAME_OR_WILDCARD


<br/><br/> 
### Related links:
[ANTLR 4](https://www.antlr.org/)

[ANTLR4-tools](https://github.com/antlr/antlr4/blob/master/doc/getting-started.md#getting-started-the-easy-way-using-antlr4-tools)

[ANTLR 4 Documentation](https://github.com/antlr/antlr4/tree/master/doc)

[ANTLR 4 Runtime API](https://www.antlr.org/api/Java/)

[Python 3.12 Lexical Analysis](https://docs.python.org/3.12/reference/lexical_analysis.html)

[cpython](https://github.com/python/cpython)

[ANTLR4 parser for Python 2.7.18](https://github.com/RobEin/ANTLR4-parser-for-Python-2.7.18)

[ANTLR4 parser for Python 3.8](https://github.com/RobEin/ANTLR4-parser-for-Python-3.8.12)
