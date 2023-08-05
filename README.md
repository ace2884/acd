1.**Define Token, Pattern and Lexeme**
 Token: A token is a single, meaningful unit of a programming language or natural language text. It can be a keyword, identifier, operator, symbol, or literal value.
 Pattern: A pattern is a template or rule that describes a set of possible sequences of characters. It's often used in text matching or searching algorithms to find occurrences that match the specified pattern.
 Lexeme: A lexeme is the lowest-level syntactic unit in a programming language. It's the actual sequence of characters that makes up a specific instance of a token, without considering its surrounding
 
2.**Context-Free Grammar** (CFG) is a formal way to describe the syntax or structure of a programming language or natural language using a set of production rules. It's called "context-free" because each rule applies independently of its surrounding context, making it suitable for modeling hierarchical structures.
  
3. **Actions performed by Shift reduce parser**
A shift-reduce parser performs two main actions during parsing:

 Shift: It shifts (moves) the input symbols from the front of the input stream to the parsing stack. This action indicates that the parser has recognized a part of the input that matches a certain production rule.

 Reduce: It reduces a sequence of symbols on the parsing stack to a non-terminal symbol according to a production rule. This indicates that a higher-level structure has been identified in the input.

These actions continue iteratively until the parsing stack contains only the start symbol, and the input stream is empty, indicating successful parsing or a syntax error.

4.**set of rules for first and flow**
**FIRST Set Rules:**
1. For each terminal symbol, FIRST(Terminal) = {Terminal}.
2. For each non-terminal symbol, if it derives ε (empty string), include ε in FIRST(Non-Terminal).
3. For each production A -> X1X2...Xn, include FIRST(X1) in FIRST(A).
4. If ε is in FIRST(Xi) for all i=1 to n, then include ε in FIRST(A).

**FOLLOW Set Rules:**
1. Follow the start symbol gets the end-of-input symbol ($).
2. For each production A -> X1X2...Xn, include FIRST(Xn) (excluding ε) in FOLLOW(Xn-1), and if ε is in FIRST(Xn), include FOLLOW(A) in FOLLOW(Xn-1).
3. If ε is in FIRST(Xn) and Xn is the last symbol in the production, include FOLLOW(A) in FOLLOW(Xn).
4. If there's a production A -> X1X2...Xn and ε is in FIRST(Xi) for all j=i+1 to n, then include FOLLOW(A) in FOLLOW(Xi).

These rules are crucial for constructing predictive parsing tables, which are used in top-down parsing methods like LL(1) parsing. They help determine the expected tokens at various points in a context-free grammar, aiding the parser in making parsing decisions.

5. **Type Checking:** Type checking is a compiler or interpreter process that verifies if the types of operands and operations in a program are compatible and consistent according to the programming language's rules. It helps prevent type-related errors during program execution.

6. **Chomsky Hierarchy:** The Chomsky hierarchy categorizes grammars into four levels based on their generative power and structure. The levels, from least to most expressive, are Type 3 (Regular), Type 2 (Context-Free), Type 1 (Context-Sensitive), and Type 0 (Unrestricted). It's a hierarchy of increasing complexity.

7. **Flow Graph:** A flow graph is a graphical representation of a program's control flow. It consists of nodes representing basic blocks of code and directed edges representing the flow of control between these blocks.

8. **Code Generation:** Code generation is the process in compilation where high-level source code is translated into lower-level code, such as assembly or machine code, that can be executed by a computer. It involves allocating registers, managing memory, and arranging instructions.

9. **Issues in Code Generation:** Some issues in code generation include register allocation, managing memory efficiently, generating optimal code for different architectures, handling complex expressions, and minimizing the overhead introduced by generated code.

10. **Flow Graph Leaders:** Leaders in a flow graph are the first statements of basic blocks. Rules to define leaders include the first statement of the program, the target of a conditional or unconditional jump, and the statement immediately following a jump.

11. **Language, Grammar, Automata, Regular Expression:**
   - Language: A set of strings or sequences over a given alphabet.
   - Grammar: A set of production rules defining the structure of a language.
   - Automata: Abstract models (like Finite Automata) used to recognize or generate languages.
   - Regular Expression: A concise way to describe patterns or sets of strings in a language.

12. **DFA (Deterministic Finite Automaton):** A finite automaton where each state transition is uniquely determined by the current input symbol. Example: A simple DFA recognizing the language of even number of 'a's.

13. **Compiler, Interpreter, Translator:**
   - Compiler: A program that translates high-level source code to machine code ahead of execution.
   - Interpreter: A program that directly executes high-level source code without creating an intermediate machine code.
   - Translator: A general term for programs that convert code from one language to another.

14. **Types of LR Parsers and Comparison:** LR parsers include LR(0), SLR(1), LALR(1), and LR(1). They differ in the size of the parsing tables and their expressive power. SLR is less powerful than LALR and LR(1), but it's easier to construct. LALR and LR(1) are more powerful but require larger parsing tables.

15. **Shift-Reduce Parsing Conflicts:** Conflicts can occur during shift-reduce parsing when the parser encounters an ambiguity in the grammar, leading to multiple possible actions. Common conflicts include Shift/Reduce conflicts and Reduce/Reduce conflicts.

16. **Attributed Grammar:** An attributed grammar associates attributes (values) with grammar symbols, which are then evaluated during parsing. It's used to carry information through the parsing process, often for semantic analysis or code generation.

17. **CFG (Context-Free Grammar) and CSG (Context-Sensitive Grammar):** 
   - CFG: Grammar with production rules not dependent on the context of the symbols.
   - CSG: Grammar where production rules may depend on the context in which symbols appear.

18. **Limitations of Static Allocation:** Static allocation of memory has limitations such as fixed memory allocation size, inefficient memory usage, inability to handle dynamic data structures effectively, and lack of flexibility in memory management.

19. **Dead Code Elimination:** It's a compiler optimization technique that identifies and removes code that can never be executed, reducing unnecessary computation and improving code efficiency.

20. **Relocatable Machine Code:** It's machine code that can be loaded and executed at any memory location, as opposed to absolute machine code that relies on a fixed memory address. It's essential for creating executable programs that can be loaded into different memory spaces.

21. **Address Descriptor:** An address descriptor holds information about the memory location or register used to store a variable or temporary value during code generation. It's crucial for efficient management of memory and registers in generated code.

22. **NFA (Nondeterministic Finite Automaton):** Like DFA but with non-unique state transitions for certain inputs. Example: An NFA recognizing strings containing "ab" or "ba".

23. **Copy Propagation:** Copy propagation is an optimization technique that replaces uses of a variable with its assigned value, effectively eliminating redundant assignments and improving code efficiency.

24. **Reachability in Code Optimization:** Reachability refers to the property of a program's code where certain instructions or code blocks can be executed during program execution. In optimization, unreachable code is often removed to enhance code efficiency.

25. **Live Variable Analysis:** Live variable analysis identifies variables whose values will be used later in the program, allowing the compiler to optimize by avoiding unnecessary computations or memory operations.

26. **Loop Optimization Techniques:** Various loop optimization techniques include loop unrolling, loop fusion, loop interchange, loop-invariant code motion, and strength reduction, all aimed at improving the performance of loops.

27. **Parser:** A parser is a compiler component that analyzes the structure of source code based on a given grammar. It verifies whether the code conforms to the grammar rules and generates a parse tree or abstract syntax tree.

28. **Semantic Analysis Purpose:** Semantic analysis checks the meaning and validity of the program's structure and expressions. It ensures that the code adheres to the language's semantics and detects semantic errors.

29. **Flow Graph Terminology:** In defining a flow graph, terminology includes nodes representing basic blocks, directed edges representing control flow, and leaders representing the first statements of basic blocks.

30. **Addressing Modes:** Various addressing modes include Immediate, Direct, Indirect, Register, Register Indirect, Indexed, and Auto-Increment/Decrement. Examples: Immediate (#42), Direct (variable), Indexed (R1+2), Register (R2).

31. **Address vs. Register Descriptor:** An address descriptor holds information about memory locations for variables, while a register descriptor contains information about register allocation for variables.

32. **Redundant Subexpression Elimination:** It's an optimization that identifies and removes calculations that yield the same result as previous computations. Example: In "a = b * c; d = b * c;", the subexpression "b * c" is redundant.

33. **Grammar Transformation:** Original Grammar: L → L ; S | S; S → id = E | id (E) E → id | num. Transformed: L → S L' | S L' ; L' → ε. S → id = E | id (E) E → id | num.

34. **Syntax Directed Definition:** It's a context-free grammar extended with semantic actions. Example: Grammar rule E → E + T {print("+")}; T {print(T.val)}.

35. **Canonical Collection of LR(1) Items:** The set of items represents states in an LR(1) parsing table. Given the context, a detailed explanation would be more appropriate.

36. **Type Conversion vs. Type Checking:** Type conversion is changing the type of a value explicitly, like converting an integer to a float. Type checking ensures that operations are valid with regard to types, like adding integers but not strings.

37. **Principle Sources of Optimization:** Optimization stems from reducing execution time, minimizing memory usage, and improving code maintainability. Patterns like constant folding, loop optimization, and strength reduction enhance code efficiency.

38. **Rules for Leaders of Basic Blocks:** Leaders are the first statements of basic blocks. Rules include the first statement of the program, targets of jumps, and statements following jumps. Algebraic transformations simplify expressions and optimize code.

39. **Flow Graph and DAG Applications:** A flow graph represents control flow, aiding in optimization. Directed Acyclic Graphs (DAGs) find application in expression evaluation and code optimization due to their ability to identify and eliminate redundant computations.

40. **DAG for Expression:** In the expression "a = b * -c + b * -c", a DAG would combine common subexpressions, resulting in fewer computations and efficient code. Constructing it graphically would involve nodes and edges representing expressions and their relationships.
List out the rules for FIRST and Follow in short
