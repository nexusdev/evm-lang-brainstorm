brainstorming for new EVM language


* actor-based / "smart objects" (no `contract` keyword ever!)

* runtime knows object "safety" classes (proven to do what we think / want)

* global shared runtime objects (TODO examples). Address+type info unique per chain.

* safe "shim" objects enable provable constraints on object behavior

* first-class async

* ABI-compatible - but used sparingly and deliberately, as system entrypoints

* first class "systems" ("applets" - control/environment group with entrypoints)

* "world aware"

* auth in runtime

* no-ether by default (provide wrapper)
* no reentry by default (for entrypoints)

* No analogy to `.call` and `.send`. Opcodes `CALL`, `CALLCODE` (kill it with fire), `DELEGATECALL` are exposed as distinct language features

* syntax sugar for hash addressed storage like solidity ref types, eg `shamap :: type1, type2, type3 => type4` instead of `mapping(type1=>mapping(type2=>mapping(type3=>type4))) shamap` 

* factories enable superpowered address typing (e.g., if you expect "lending" and owned object to work, it better work)
