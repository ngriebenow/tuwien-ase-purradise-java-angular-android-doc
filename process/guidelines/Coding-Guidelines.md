
| Issue |  #24 |
| ----- | --- |
| author       | Thomas Stoiber @11777755 |
| released by  | Nicolas Griebenow @01617265 |
| release date | 2020-11-01 |

# Coding Guidelines
The code guidelines are inspired by the Google's coding standards for source code in the Java™ Programming Language.      
https://google.github.io/styleguide/javaguide.html

[[_TOC_]]

## General
### File encoding
Files are encoded in UTF-8

### Classes
#### Exactly one top-level class declaration
Each top-level class resides in a source file of its own.
#### Ordering of class contents
The content of a class should be implemented in a logical order. Generally it should be in the form:
 * constant members
 * final members
 * non-final members
 * constructor
 * methods
 * inner classes
Overloaded methods should not be split - there are no other methods in between those two.

### Formatting
#### One statement per line
Each statement is followed by a line break.
#### Block Indentation
The block indentation (e.g. at an if) is **4 spaces**.
#### Lines
##### Line Length
A line is at maximum **120 characters** long.
Exceptions:
* package statement
* import statements
* URLs in Strings or javadoc
##### Line-Wrapping
When a line is going to be wrapped, it is at these points:
 * before an operator like (`+`, `-`) as well as `.`, `::` operators
 * before a generic statement (`<T extends Foo & Bar>`)
 * after a assignment operator
 * After an opening parenthesis `(`. The parenthesis stays in the line.
 * After a comma in a parameter list or method call
 * After a lambda arrow only if the body contains exactly one statement

When a statement is wrapped, it is continued with 4 spaced indentation.

**Note:** The primary goal of line wrapping is to have clear code, _not necessarily_ code that fits in the smallest number of lines.

#### Braces
##### Braces are used where optional
Braces are **always** used with `if`, `else`, `for`, `do` and `while` statements, even when the body is empty or contains only a single statement.
##### K & R style
Braces follow the Kernighan and Ritchie style ("Egyptian brackets") for nonempty blocks and block-like constructs:
*   No line break before the opening brace.
*   Line break after the opening brace.
*   Line break before the closing brace.
*   Line break after the closing brace, _only if_ that brace terminates a statement or terminates the body of a method, constructor, or _named_ class. For example, there is _no_ line break after the brace if it is followed by `else` or a comma.
Examples:

```
return () -> {
    while (condition()) {
        method();
    }
};

return new MyClass() {
    @Override public void method() {
        if (condition()) {
            try {
                something();
            } catch (ProblemException e) {
                recover();
            }
        } else if (otherCondition()) {
            somethingElse();
        } else {
            lastThing();
        }
    }
};
```
#### Whitespaces
##### Vertical
Blank lines are required to be between two methods, constructors, ... (except between two member variables of the same type - e.g. final static, final, non-final).

Blank lines are always allowed to be used to improve readability.

##### Horizontal
###### Statements
There must be a space between the statement and the parenthesis in statements like `if`, `for`, ... and between the brace and the statement in statements like `else`, `catch`, ... .
###### Operators
There must be a space between the value and the operator.
```
int a = 1 + 2; // OK
int a=1+2; // Not OK
``` 
##### Parameters
There must be a whitespace after a `,` in a parameter list (method definition and method call).

### Naming
We always use English names.
#### Packages
Package names are all lowercase, with consecutive words simply concatenated together (no underscores). For example, com.example.deepspace
#### Classes
Class names are written in UpperCamelCase.
Class names are typically nouns (`Map`) or noun phrases (`ImmutableList`).
Interface names can also be adjective phrases (`Readable`).
#### Methods
Method names are written in lowerCamelCase.

Method names are typically verbs or verb phrases. For example, sendMessage or stop.

Underscores may appear in JUnit test method names.

#### Constants
Constant names use CONSTANT_CASE.
#### Variables, Parameters
Variables and parameters use lowerCamelCase.

### Programming Practices

#### Caught exceptions: not ignored

Except as noted below, it is very rarely correct to do nothing in response to a caught exception. (Typical responses are to log it, or if it is considered "impossible", rethrow it as an `AssertionError`.)

When it truly is appropriate to take no action whatsoever in a catch block, the reason this is justified is explained in a comment.
```
try {
    int i = Integer.parseInt(response);
    return handleNumericResponse(i);
} catch (NumberFormatException ok) {
    // it's not numeric; that's fine, just continue
}
return handleTextResponse(response);
```

**Exception:** In tests, a caught exception may be ignored without comment _if_ its name is or begins with `expected`. The following is a very common idiom for ensuring that the code under test _does_ throw an exception of the expected type, so a comment is unnecessary here.
```
try {
    emptyStack.pop();
    fail();
} catch (NoSuchElementException expected) {
}
```

#### Static members: qualified using class

When a reference to a static class member must be qualified, it is qualified with that class's name, not with a reference or expression of that class's type.
```
Foo aFoo = ...;
Foo.aStaticMethod(); // good
aFoo.aStaticMethod(); // bad
somethingThatYieldsAFoo().aStaticMethod(); // very bad
```

#### Declarations and Initalizations
##### Arrays
Arrays are declared in Java-Style, not in C-Style
```
int[] a; // OK
int b[]; // Not OK
```
##### Long Values
Long-Values are defined with a capital L, not with a small l.
´´´
long a = 1L; // OK
long b = 1l; // Not OK
´´´

### Documentation
We are using Javadoc in Java and JSDoc in Typescript to document our code.
#### Formatting
The _basic_ formatting of Javadoc blocks is as seen in this example:
```
/**
 * Multiple lines of Javadoc text are written here,
 * wrapped normally...
 */
public int method(String p1) { ... }
```
... or in this single-line example:
```
/** An especially short bit of Javadoc. */
```
#### Summary Fragment
The summary fragment consists of noun and verb phrases instead of full sentences. (`Returns the customer ID` instead of `This method returns ...`)

#### Block Tags
When block-tags are used, they are not allowed to be empty.

There are no Block-Tags in a single-line javadoc (`/** Returns the customer ID **/` instead of `/** @return the customer ID **/`).

#### Usage
Every public and protected method should have a documentation.
Classes can have a javadoc, but don't have to.

**Exception:** Documentation is optional for "simple, obvious" methods like `getFoo()`, in cases where there really and truly is nothing else worthwhile to say but `"Returns the foo"`.

**Exception:** The documentation is not always present on a method that overrides a supertype method.

## Java
### Imports
#### Wildcard Imports
Wildcard imports are not used. All imports must be fully qualified.
#### Import Ordering
Imports are ordered as follows:
1.  All static imports in a single block.
2.  All non-static imports in a single block.
Between the static and the non-static imports is an empty line. Imports are ordered by name.
```
import static test.TestClass.testMethod;

import java.util.Map;
import test.TestClass;
import test.TestClass.NestedClass;
```

### Programming Practices
#### `@Override`: always used
A method is marked with the `@Override` annotation whenever it is legal. This includes a class method overriding a superclass method, a class method implementing an interface method, and an interface method respecifying a superinterface method.

## Typescript

### Auto-Lint
You can use ESLint to automatically fix your linting issues. Use the following command:  
`npm run-script lint:fix`

### Typedefinitions
In Typescript, we use typedefinitions as precise as possible and. Every every parameter of a function and every non-constant variable must have a typedefinition.

There is a space before and after the typedefinition operator.
```
var a \: number;

function foo(a : string, b : any) {
    ...
}
```

### Punctuation
#### Statments must have semicolons
Every Statement must end with a semicolon. E.g.:
```
// Not Ok
function foo() {
    const a = 15;
    return a
}
// Ok
function foo() {
    const a = 15;
    return a;
}
```
#### Strings use double-quotes
Strings use double-quotes instead of single-quotes.
```
const a = "This is OK";
const b = 'This is not OK';
```

### No trailing comma in arrays
In array-definitions, there is no trailing comma.
```
a = [1, 3, 5,] // Not OK
a = [1, 3, 5] // OK
```

## Android
The guidelines for Android are inspired from: https://medium.com/mindorks/android-resource-naming-convention-42e4e8026614

### Layout
Java classes of layout components are called ´<Name><Type>´, where `<Name>` is the Name of the component in UpperCamelCase and `<Type>` is the type of the component. (e.g. `MainActivity`).

The xml layout files are named `<Type>_<Name>`, where `<Type>` is the type of the component and `<Name>` is the name of the component, in lower case separated by underscores (e.g. `activity_main`).
