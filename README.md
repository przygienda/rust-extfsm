Extended FSM in Rust 
====================

[![crates.io](http://meritbadge.herokuapp.com/coap)](https://crates.io/crates/coap)
[![Travis Build Status](https://travis-ci.org/przygienda/rust-extfsm.svg?branch=master)](https://travis-ci.org/przygienda/rust-extfsm)

   * internal event queue allows machine to post events 
     on transition completion 
   * state entry/exit transition support 
   * events can carry arguments accessible on transition
   * generates its own .dot graphs 
   * slog debugging support 
   * extended state can be examined when not executing

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
