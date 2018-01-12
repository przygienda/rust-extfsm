Version 0.6
===========

* added `extend_events` which can use any `IntoIterator` on Events 
* changed FSM DOT output to stack self->self events on top of each other to improve readability,
  however to be able  to dotfile a graph `Events` and `States` must provide `Ord` 
* allow to render a non-mutable fsm reference given the results are ephemeral every time 
* changed the return value of the transition to hold a vector which is syntactically easier 
  on the user, this is an somewhat API breaking change of course albeit if code written does 
  something like 
    
    `vec![..].drain(..)::collect()`
  
  it should be just inefficient but still conform. Ideal for performance would be 
  boxed slices but those precondition Copy traits which is very limiting. 