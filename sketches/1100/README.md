## Scenario
Same as 1000

## Structure
Watch out for the Lispy DSL.
 - (context) function defines the entry point of a package
 - (symbol) declares a symbol
 - (with) declares a list of symbols that will be resolved but kept internally
 - (has) declares a list of symbols that will make up that symbol. it must contain a list of lists with the head being the name of the subsymbol and the tail being a reference to a symbol or an atom
 - (something) when something is one of the following resolves to a reference to their symbol
   - name of a file within the package
   - name of a variable previously declared with (with)
 - (inherit) probably a language construct, but serves to reference a newly created symbol that joins a base and a "middle-man" descriptor between the two
 