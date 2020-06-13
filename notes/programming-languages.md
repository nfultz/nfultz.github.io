The traditional abstraction barriers between compiler, build system and package manager are increasingly ill-suited for IDEs, parallel build systems, and modern source code organization. Recent compilers like go and rustc are equipped with a fully-fledged build systems; semantic build systems like Bazel and Gradle also expect to manage the packaging of software. Does this mean we should jettison these abstraction barriers? It seems worthwhile to look for new interfaces which can accommodate these use-cases. --- [The convergence of compilers, build systems and package managers : Inside 736-131](http://blog.ezyang.com/2015/12/the-convergence-of-compilers-build-systems-and-package-managers/)

[The End of Dynamic Languages](http://elbenshira.com/blog/the-end-of-dynamic-languages/)

Wake is a brand new programming language aimed at solving modern problems, such as code testability, expressive typesafety, and language interoperability. --- [Wake Programming Language](http://www.wakelang.com/)

There are some pretty strong statements about types floating around out there. The claims range from the oft-repeated phrase that when you get the types to line up, everything just works, to not relying on type safety is unethical (if you have an SLA)1, I think programmers who doubt that type systems help are basically the tech equivalent of an anti-vaxxer2, and It boils down to cost vs benefit, actual studies, and mathematical axioms, not aesthetics or feelings. There are probably plenty of strong claims about dynamic languages that I’d disagree with if I heard them, but I’m not in the right communities to hear the more outlandish claims about dynamically typed languages. Either way, it’s rare to see people cite actual evidence. --- [Static vs. dynamic languages: a literature review](http://danluu.com/empirical-pl/)

META II was a "compiler-compiler," which is to say that when one suspects that a production compiler might be a rather large project to write in assembly—and especially if one were in an era in which COTS (commercial off-the-shelf), let alone libre and open source, compilers were still science fiction—then it makes sense to aim for an intermediate target: something small enough to be hand-coded in assembly, yet powerful enough for writing what one had been aiming for in the first place. --- [META II: Digital Vellum in the Digital Scriptorium - ACM Queue](https://queue.acm.org/detail.cfm?id=2724586)

A few days ago, Elben Shira caught the attention of the programming blogosphere with his post entitled The End of Dynamic Languages. The key point from this post is in the following statement:



    This is my bet: the age of dynamic languages is over. There will be no new successful ones.



Like him, I’ve noticed that despite the fact that there have been an enormous number of new programming languages coming out recently, the overwhelming majority of them are statically typed. Elben and others make the argument that this is because static languages are better equipped to deal with larger projects, they have better tooling, and programmers prefer them. --- [Have Static Languages Won? | Pointers Gone Wild](http://pointersgonewild.com/2015/11/25/have-static-languages-won/)

[Zero-Overhead Metaprogramming: Reflection and Metaobject Protocols Fast and without Compromises](http://stefan-marr.de/papers/pldi-marr-et-al-zero-overhead-metaprogramming/)

[Tutorial part 4: Adding JIT-compilation to a toy interpreter — libgccjit v5.1.0 ( ) documentation](https://gcc.gnu.org/onlinedocs/gcc-5.1.0/jit/intro/tutorial04.html)

[RECC, The Robert Elder Compiler (and emulator and microkernel) Collection](http://recc.robertelder.org/)

