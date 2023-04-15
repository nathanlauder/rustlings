## Data types

- usize is a type dependent on architecture (arch) of the system it is operating on.  The system size (x64, x32) will force the size of the type

##  References and Borrowing

Rust allows for a variable to be borrowed.  In a borrowed state, a variable is immutable.  However, a ***single*** mutable reference `&mut var` can be made to the variable to modify the reference.  This is only doable if the original variable declaration is mutable

```rust
let mut s = String::from("Hello");

let ref = &mut s;
// will fail
let ref2  = &mut s;
```

## Vec

When iterating over a &vec, the iterator is a refernce to whatever element is being currently iterated over.  If the iterated value needs to change, you must dereference (*i) the value to reassume ownership.