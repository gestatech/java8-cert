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
- [Data Access Object](https://de.wikipedia.org/wiki/Data_Access_Object)
- [Liste von Entwurfsmustern](https://de.wikipedia.org/wiki/Entwurfsmuster#Liste_von_Mustern)
- [Scope of private constructor in nested class](http://stackoverflow.com/a/12542295/811708)
- [Should an abstract class have at least one abstract method?](http://stackoverflow.com/questions/2283399/should-an-abstract-class-have-at-least-one-abstract-method)
- [Information & changes to exam topics](https://www.selikoff.net/java-ocp-8-programmer-ii-study-guide/)
- [Unbound wildcard `<?>` vs `<T>`](http://stackoverflow.com/questions/18787393/java-unbound-wildcard-vs-t)
- [Static Initialization Blocks](http://stackoverflow.com/questions/2420389/static-initialization-blocks)

### TODO

- [x] Access modifier review (`public`, `default`, `protected`, `private`)
- [x] `transient` keyword (= "field should not be serialized")
- [x] Varargs
- [x] Stringbuilder
- [x] exact behaviour of `instanceof` (with `null` and usage on interfaces)
- [x] packages & imports (static imports, important `java.*` packages)
- [x] More keywords: `synchronized`, `transient`, `native`
- [ ] Autoboxing, Unboxing
- [ ] `Comparable` interface
- [ ] `static`, `abstract` and `final` keywords. Final fields vs. methods vs. classes
- [ ] `Serializable`, `writeObject()
- [ ] Review: `abstract` classes vs. interfaces
- [ ] Review: java.lang.Object & overridable methods
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

Not part of the exam:
- `volatile` keyword

### Lessons learned / pitfalls
- toString on Enums will print String, not ordinal
- "An abstract type can be an abstract class or interface."
- "In a subclass, the compiler implicitly invokes a parameterless constructor in the superclass if a superclass constructor is not explicitly invoked."
- "Top-level classes cannot be declared using the protected access modifier. Only the access modifier public is allowed for top-level classes. An inner class can be declared with the access modifier protected because an inner class is a member of the top-level class."
- "Overriding methods can specify access modifiers that are less restrictive than the original method. Also, Java allows an overriding method to return a subtype of the return type of the original method."
- Command line params start at `args[0]` and are always Strings.
- "It is permitted, but discouraged as a matter of style, to redundantly specify the public and/or abstract modifier for a method declared in an interface."
- "If you do not specify that the interface is public, then your interface is accessible only to classes defined in the same package as the interface."
- "Static methods can not be overridden in the exact sense of the word, but they can hide parent static methods" ([source](http://stackoverflow.com/a/5436790/811708))
- Enums can not have a public constructor. All Enum values ("inner subclasses") will be constructed the first time a Enum value is used.
- "The first time that we ask for any of the `enum` values (of a certain Enum) Java constructs all of the `enum` values."
- "In Java 8, the 'effectively final' concept was introduced. If the code can still compile with the keyword `final` inserted before the local variable, the variable is effectively final." (study book)
- Inner classes: "If the member or constructor is declared private, then access is permitted if and only if it occurs within the body of the top level class (§7.6) that encloses the declaration of the member or constructor." [source](http://docs.oracle.com/javase/specs/jls/se8/html/jls-6.html#jls-6.6.1)
- 'local inner class' = nested class defined within a method
- Floats (for example) as class variables (not local ones) will be initialized with `0.0`, but not inside a method!
- In a concrete class, all methods and Constructors must contain bodies.
- A class cannot include package or import statements. (class itself not, but file that contains class)
- (`abstract`) classes can be **extended**, `interfaces` can be implemented (or `extended`, if you're an `interface` yourself). In other words, valid examples are: `interface extends interface` / `class extends class` / `class implements interface`.
- "A JavaBean is a design principle for encapsulating data in an object in Java."
- A new `public StringBuilder()` has initial capacity of 16 characters.
- Parentheses for Lambda parameter: can be omitted only if one parameter (not if 0 or 2+) and there is no type given.
- "Tight coupling is the practice of developing coupled classes that are highly dependent, such that a minor change in one class may greatly impact the other class. Alternatively, loose coupling is the practice of developing coupled classes with minimum dependencies on one another."

### Random facts & tables

#### Access modifiers

| Modifier   | Class | Package | Subclass | World |
|------------|:-----:|:-------:|:--------:|:-----:|
| public     | Y     | Y       | Y        | Y     |
| protected  | Y     | Y       | Y        | N     |
| no modifier| Y     | Y       | N        | N     |
| private    | Y     | N       | N        | N     |

#### Functional Interfaces

| Functional Interface   | # Parameters | Return Type | Single Abstract Method |
|------------------------|:------------:|:-----------:|:----------------------:|
| `Supplier<T>`          | 0            | T           | get                    |
| `Consumer<T>`          | 1 (T)        | void        | accept                 |
| `BiConsumer<T, U>`     | 2 (T, U)     | void        | accept                 |
| `Predicate<T>`         | 1 (T)        | boolean     | test                   |
| `BiPredicate<T, U>`    | 2 (T, U)     | boolean     | test                   |
| `Function<T>`          | 1 (T)        | R           | apply                  |
| `BiFunction<T, U>`     | 2 (T, U)     | R           | apply                  |
| `UnaryOperator<T>`     | 1 (T)        | T           | apply                  |
| `BinaryOperator<T, U>` | 2 (T, U)     | T           | apply                  |

#### Generics naming conventions

* `E` for an element
* `K` for a map key
* `V` for a map value
* `N` for a number
* `T` for a generic data type
* `S`, `U`, `V`, and so forth for multiple generic types

#### Exception hierarchy
* java.lang.Throwable (implements java.io.Serializable)
  * java.lang.Error
  * java.lang.Exception
    * java.lang.CloneNotSupportedException
    * java.lang.InterruptedException
    * java.lang.ReflectiveOperationException
      * java.lang.ClassNotFoundException
      * java.lang.IllegalAccessException
      * java.lang.InstantiationException
      * java.lang.NoSuchFieldException
      * java.lang.NoSuchMethodException
    * **java.io.IOException**
      * java.nio.file.attribute.UserPrincipalNotFoundException
      * java.io.EOFException
      * java.io.FileNotFoundException
      * java.net.MalformedURLException
      * java.rmi.RemoteException
      * java.net.SocketException
      * javax.net.ssl.SSLException
      * java.net.UnknownHostException
      * java.io.UnsupportedEncodingException
      * ...
    * **java.sql.SQLException**
      * java.sql.SQLTransientException
      * javax.sql.rowset.serial.SerialException
      * java.sql.SQLClientInfoException
      * ...
    * **java.lang.instrument.IllegalClassFormatException**
    * **java.awt.AWTException**
    * **javax.management.BadStringOperationException**
    * **javax.security.cert.CertificateException**
    * **java.util.zip.DataFormatException**
    * **javax.naming.NamingException**
    * **java.rmi.NotBoundException**
    * **java.text.ParseException**
    * **javax.print.PrintException**
    * **java.util.TooManyListenersException**
    * **javax.management.modelmbean.XMLParseException**
    * ...
    * java.lang.RuntimeException
      * java.lang.ArithmeticException
      * java.lang.ArrayStoreException
      * java.lang.ClassCastException
      * java.lang.EnumConstantNotPresentException
      * java.lang.IllegalArgumentException
        * java.lang.IllegalThreadStateException
        * java.lang.NumberFormatException
      * java.lang.IllegalMonitorStateException
      * java.lang.IllegalStateException
      * java.lang.IndexOutOfBoundsException
        * java.lang.ArrayIndexOutOfBoundsException
        * java.lang.StringIndexOutOfBoundsException
      * java.lang.NegativeArraySizeException
      * java.lang.NullPointerException
      * java.lang.SecurityException
      * java.lang.TypeNotPresentException
      * java.lang.UnsupportedOperationException
