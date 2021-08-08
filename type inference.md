# Type Inference

Kotlin has a concept of _type inference_ for compile-time type information, meaning some type information in the code may be omitted, to be inferred by the compiler. There are two kinds of type inference supported by Kotlin.

-   [Local type inference](https://kotlinlang.org/spec/type-inference.html#local-type-inference), for inferring types of expressions locally, in statement/expression scope;
-   [Function signature type inference](https://kotlinlang.org/spec/type-inference.html#function-signature-type-inference), for inferring types of function return values and/or parameters.

Type inference is a [type constraint](https://kotlinlang.org/spec/kotlin-type-constraints.html#kotlin-type-constraints) problem, and is usually solved by a type constraint solver. For this reason, type inference is applicable in situations when the type context contains enough information for the type constraint solver to create an [optimal constraint system solution](https://kotlinlang.org/spec/kotlin-type-constraints.html#finding-optimal-constraint-system-solution) w.r.t. type inference problem.

> Note: for the purposes of type inference, an optimal solution is the one which does not contain any free type variables with no explicit constraints on them.

Kotlin also supports flow-sensitive types in the form of [smart casts](https://kotlinlang.org/spec/type-inference.html#smart-casts), which have direct effect on type inference. Therefore, we will discuss them first, before talking about type inference itself... _(see source for more information)_

### Source
[Type inference - Kotlin language specification](https://kotlinlang.org/spec/type-inference.html)