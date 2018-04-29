Extended Finite State Machine in Rust 
=====================================

[![crates.io](http://meritbadge.herokuapp.com/coap)](https://crates.io/crates/extfsm)
[![Travis Build Status](https://travis-ci.org/przygienda/rust-extfsm.svg?branch=master)](https://travis-ci.org/przygienda/rust-extfsm)
[![Coverage Status](https://coveralls.io/repos/przygienda/rust-extfsm/badge.svg?branch=master&service=github)](https://coveralls.io/github/przygienda/rust-extfsm?branch=master)

Introduction
============

Library to support programming of Extended Finite State Machines (FSM) in Rust. 
The machine is not necessarily built for fastest zero-copy speed but greatest 
flexibility and maintanability. Non zero-copy design has been chosen since after 
event processing it stores state and passes control back out which would make 
management of lifetimes very onerous on the user otherwise. 

FSMs are from long engineering experience the cleanest way to implement 
asynchronous protocols between components.

Features
========

   * internal event queue allows a machine to post events 
     against itself on transition completion 
   * supports optional transition per state entry/exit  
   * events can carry dynamic arguments accessible when 
     transition is executed
   * machine generates its own .dot graphs easily converted into .pdf or .svg supporting 
     colored edges and summarizing edges for same start and end state transitions
   * slog debugging support 
   * machine's extended state can be examined when not processing events
   * machine transitions can be traversed read-only
   * flyweight pattern to run many instances of same FSM with different extended state

License
=======

   Copyright (c) 2017, Juniper Networks, Inc.
   All rights reserved.

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   This code is not an official Juniper product.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.
