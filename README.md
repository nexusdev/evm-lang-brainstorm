brainstorming for new EVM language

#### model

* actor-based / "smart objects" (no `contract` keyword ever!)

* first-class async

* ABI-compatible - but used sparingly and deliberately, as system entrypoints

* first class "systems" ("applets" - control/environment group with entrypoints)

* auth in runtime

#### type-enhanced safety

* say "dependent types" one more time, motherfucker, I double dare you

#### heavily leverage global shared runtime env

* "world aware"

* factories enable superpowered address typing (e.g., if you expect "lending" and owned object to work, it better work)

* global shared runtime objects (TODO examples). Address+type info unique per chain.

* runtime knows object "safety" classes (proven to do what we think / want)

* safe "shim" objects enable provable constraints on object behavior


#### misc

* no-ether by default (provide wrapper)
* no reentry by default (for entrypoints)
* No analogy to `.call` and `.send`. Opcodes `CALL`, `CALLCODE` (kill it with fire), `DELEGATECALL` are exposed as distinct language features
* syntax sugar for hash addressed storage like solidity ref types, eg `shamap :: type1, type2, type3 => type4` instead of `mapping(type1=>mapping(type2=>mapping(type3=>type4))) shamap` 

