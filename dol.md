# DOL meaning representation language
## Tree view of semantics
### **Node types**
  - **Constants**: Refer to specific objects in the world. A constant can be a number, a lexical string, or an entity.
  - **Classes**: Refer to a category of entities sharing common semantic properties. For example: `location.city`, `math.number`
    - Sub-class: *math.number ⊆ math.expression*
    - Template classes: classes with one or more parameters, for example: `t.list<c, m, n>`, where `c` is a class, `m` and `n` are integers.
  - **Functions**: The major way to form larger language units from smaller ones. A function is comprised of a *name*, a list of *core arguments*, and a *return type*.
