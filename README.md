Extended Final State Machine in Rust 
====================================

[![crates.io](http://meritbadge.herokuapp.com/coap)](https://crates.io/crates/coap)
[![Travis Build Status](https://travis-ci.org/przygienda/rust-extfsm.svg?branch=master)](https://travis-ci.org/przygienda/rust-extfsm)
[![Coverage Status](https://coveralls.io/repos/przygienda/rust-extfsm/badge.svg?branch=master&service=github)](https://coveralls.io/github/przygienda/rust-extfsm?branch=master)

   * internal event queue allows a machine to post events 
     against itself on transition completion 
   * supports optional transition per state entry/exit  
   * events can carry dynamic arguments accessible when 
     transition is executed
   * machine generates its own .dot graphs easily converted into .pdf or .svg
   * slog debugging support 
   * machine's extended state can be examined when not processing events

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
