## JIT Compiler

#### SpringOne2GX 2015: Thursday 08:30AM

* javac is a static complier. Kind of like old school paper map.
* JIT compiler is the runtime compiler. It gets all the information at runtime.
* bytecode -> interpreter -> Profiler -> JIT compiler -> machine code
* -XX:+PrintInterpreter
* -XX:+PrintCompilaton
* On stack replcaement
* javap -c *.class
* -XX:PrintInlining
* hot( called too many times) method too big
* INstall hotspot to view PrintAssembly.
* JIT Watch
* `@CompilerControl`
* Dead code identification.
* Escape Analysis
* Safepoint checks.

* Profiler: What method should be optimized
** Null checks
** Call sites
** Execution count
* JIT compiler
** Client C1
** Server C2
** Tiered compilation.

##### Paretor Principle
80% of the time only 20% of the code is being executed.

##### Java Microbenchmark Harness (JMH)
* Micro benchmarking framework
* Setup similar to JUnit.
* `@Benchmark` annotation


