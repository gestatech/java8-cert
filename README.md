# java8-cert
Some code for practicing for the Java 8 OCP / Java SE 8 Programmer (1Z0-809).

150min (2.5h), 85 questions, 65% to pass.

### Hot topics

- Lambdas
- Streams
- File IO
- NIO
- Generics
- Collection API
- File IO (Writer, Reader, ...)
- NIO 2: Path, Files, String, Stringwriter
- Exceptions
- HashMap
- Abstrakte Klassen
- Annotations
- Date/Time API
- Concurrency Updates
- Reflection


### Resources

- Java OCP study book
- [Learning the Java Language: Table of Contents](https://docs.oracle.com/javase/tutorial/java/TOC.html)
- [java-certificate.com](http://www.java-certificate.com)
- [Java 8 Streams Tutorial](http://winterbe.com/posts/2014/07/31/java8-stream-tutorial-examples/)
- [Java Streams Cheat Sheet](http://files.zeroturnaround.com/pdf/zt_java8_streams_cheat_sheet.pdf)
- [Java Docs on `Optional`](https://docs.oracle.com/javase/8/docs/api/java/util/Optional.html)
- [Why does Java have `transient` fields?](http://stackoverflow.com/questions/910374/why-does-java-have-transient-fields)
- [Java Docs on Varargs](http://docs.oracle.com/javase/8/docs/technotes/guides/language/varargs.html)
- [Use @Override annotation when implementing abstract methods?](http://stackoverflow.com/questions/1005898/java-should-i-add-an-override-annotation-when-implementing-abstract-methods)
- [Methods in interface with or without a public/abstract access modifier?](http://stackoverflow.com/questions/161633/should-methods-in-a-java-interface-be-declared-with-or-without-a-public-access-m)
- [Defining an Interface](https://docs.oracle.com/javase/tutorial/java/IandI/interfaceDef.html)
- [Java Docs on StringBuilder](https://docs.oracle.com/javase/tutorial/java/data/buffers.html)
- [Formatting Print Output](https://docs.oracle.com/javase/tutorial/java/data/numberformat.html)
- [The 'Immutable Interface' Pattern](https://en.wikipedia.org/wiki/Immutable_interface)
- [Java packages overview](https://docs.oracle.com/javase/8/docs/api/)
- [Java Class Library (JCL) - main features](https://en.wikipedia.org/wiki/Java_Class_Library#Main_features)

### TODO

- [x] Access modifier review (`public`, `default`, `protected`, `private`)
- [x] `transient` keyword
- [x] Varargs
- [x] Stringbuilder
- [x] exact behaviour of `instanceof` (with `null` and usage on interfaces)
- [x] packages & imports (static imports, important `java.*` packages)
- [ ] Autoboxing, Unboxing
- [ ] `Comparable` interface
- [ ] `static` and `final` keywords. Final fields vs. methods vs. classes
- [ ] `Serializable`, `writeObject()
- [ ] Review: `abstract` classes vs. interfaces
- [ ] Review: java.lang.Object & overridable methods
- [ ] More keywords: `volatile`, `static`, `abstract`, `final`, `synchronized`, `transient`, `native`
- [ ] Review: Inheritance & interfaces
- [ ] Java 8: Interfaces with default method implementation
- [ ] Collection API: set vs. map), lower/upper/wildcard bound
- [ ] Design Patterns?
- [ ] Review Exceptions, exception hierarchy tree
- [ ] Annotations on Java Types
- [ ] Repeating annotations
- [ ] Reflection: access to parameter names at runtime
- [ ] Review: Singleton classes
- [ ] Review: Inner classes
- [ ] Review: Generics, generic classes/interfaces, usage
- [ ] Generics: Wildcards

### Lessons learned / pitfalls
- toString on Enums will print String, not ordinal
- "An abstract type can be an abstract class or interface."
- "In a subclass, the compiler implicitly invokes a parameterless constructor in the superclass if a superclass constructor is not explicitly invoked."
- "Top-level classes cannot be declared using the protected access modifier. Only the access modifier public is allowed for top-level classes. An inner class can be declared with the access modifier protected because an inner class is a member of the top-level class."
- "Overriding methods can specify access modifiers that are less restrictive than the original method. Also, Java allows an overriding method to return a subtype of the return type of the original method."
- Command line params start at `args[0]` and are always Strings.
- "It is permitted, but discouraged as a matter of style, to redundantly specify the public and/or abstract modifier for a method declared in an interface."
- "If you do not specify that the interface is public, then your interface is accessible only to classes defined in the same package as the interface."

