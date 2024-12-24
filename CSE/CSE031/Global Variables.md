
Variable declaration does allocate memory, structure allocation does not.

Data which is declared outside of all scopes(typically before the start of main) will allocate memory statically with a global scope, not having to be passed from place to place.
