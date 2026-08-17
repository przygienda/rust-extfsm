Version 0.14
============

* updated dependencies to current releases:
  * `dot` `0.1` -> `0.2` (this is visible in the public API since `extfsm` implements
    `dot::GraphWalk` and `dot::Labeller` for its graph types)
  * `uuid` `0.8` -> `1`
  * `itertools` `0.10` -> `0.15` (deprecated `group_by` replaced by `chunk_by`)
  * `slog-atomic` `2` -> `3` (dev dependency)
* builds warning free: all `clippy` and `rustdoc` warnings addressed
* introduced `SharedTransitionTable`/`SharedEntryExitTransitionTable` internal type
  aliases to simplify the FSM type signatures

Version 0.7
===========
* breaks API from 0.6 making the addition of transition more of a 'stacked' API where 
  properties of transitions can be added as needed. This will prevent further breakage 
  in the future when arguments are added. 
* summarize graph edges much better 
* allow for colored edges which are kept in groups

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