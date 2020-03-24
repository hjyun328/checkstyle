# Checkstyle

[Checkstyle](https://checkstyle.sourceforge.io/)에서 제공되는 모듈 내용을 정리한다.
- [Google Checkstyle](https://github.com/checkstyle/checkstyle/blob/master/src/main/resources/google_checks.xml)
- [Spymemcached Checkstyle](https://github.com/couchbase/spymemcached/blob/master/etc/checkstyle.xml)


## [Annotations](https://checkstyle.sourceforge.io/config_annotation.html)

### [MissingOverride](https://checkstyle.sourceforge.io/config_annotation.html#MissingOverride) (spymemcached)

@inheritDoc이 부여된 메소드가 override 됐는지를 검사한다.

```xml
<module name="MissingOverride"/>
```

VIOLATION
```java
/*
 * {@inheritDoc}
 */
public void foo() {
}
```

OK
```java
/*
 * {@inheritDoc}
 */
@Override
public void foo() {
}
```




## [Block Checks](https://checkstyle.sourceforge.io/config_blocks.html)

### [AvoidNestedBlocks](https://checkstyle.sourceforge.io/config_blocks.html#AvoidNestedBlocks) (spymemcached)

nested block이 존재하는지 검사한다.

```xml
<module name="AvoidNestedBlocks"/>
```

VIOLATION
```java
int foo = 0;
{
    foo = 3;
}
```

OK
```java
int foo = 0;
foo = 3;
```

### [EmptyBlock](https://checkstyle.sourceforge.io/config_blocks.html#EmptyBlock) (google, spymemcached)

empty block이 존재하는지 검사한다.

```xml
<module name="EmptyBlock">
    <property name="option" value="TEXT"/>
    <property name="tokens"
                value="LITERAL_TRY, LITERAL_FINALLY, LITERAL_IF, LITERAL_ELSE, LITERAL_SWITCH"/>
</module>
```

VIOLATION
```java
if (foo == bar) {
} else {
    System.out.println("not equal");
}
```

OK
```java
if (foo != bar) {
    System.out.println("not equal");
}
```


### [LeftCurly](https://checkstyle.sourceforge.io/config_blocks.html#LeftCurly) (google, spymemcached)

LeftCurly('{')의 줄바꿈을 검사한다.

```xml
<module name="LeftCurly">
    <property name="tokens"
              value="ANNOTATION_DEF, CLASS_DEF, CTOR_DEF, ENUM_CONSTANT_DEF, ENUM_DEF,
                     INTERFACE_DEF, LAMBDA, LITERAL_CASE, LITERAL_CATCH, LITERAL_DEFAULT,
                     LITERAL_DO, LITERAL_ELSE, LITERAL_FINALLY, LITERAL_FOR, LITERAL_IF,
                     LITERAL_SWITCH, LITERAL_SYNCHRONIZED, LITERAL_TRY, LITERAL_WHILE, METHOD_DEF,
                     OBJBLOCK, STATIC_INIT"/>
</module>
```

VIOLATION
```java
if (foo == bar)
{
    System.out.println("equal");
}
else
{
    System.out.println("not equal");
}
```

OK
```java
if (foo == bar) {
    System.out.println("equal");
} else {
    System.out.println("not equal");
}
```

### [NeedBraces](https://checkstyle.sourceforge.io/config_blocks.html#NeedBraces) (google, spymemcached)

brace('{', '}')가 존재하는지 검사한다.

```xml
<module name="NeedBraces">
    <property name="tokens"
              value="LITERAL_DO, LITERAL_ELSE, LITERAL_FOR, LITERAL_IF, LITERAL_WHILE"/>
</module>
```

VIOLATION
```java
if (foo == bar)
    System.out.println("equal");
else
    System.out.println("not equal");
```

OK
```java
if (foo == bar) {
    System.out.println("equal");
} else {
    System.out.println("not equal");
}
```

### [RightCurly](https://checkstyle.sourceforge.io/config_blocks.html#RightCurly) (google, spymemcached)

RightCurly('}')의 줄바꿈을 검사한다.

```xml
<module name="RightCurly">
    <property name="id" value="RightCurlySame"/>
    <property name="tokens"
              value="LITERAL_TRY, LITERAL_CATCH, LITERAL_FINALLY, LITERAL_IF, LITERAL_ELSE,
                     LITERAL_DO"/>
</module>
```

VIOLATION
```java
if (foo == bar) {
    System.out.println("equal"); }
else {
    System.out.println("not equal"); }
```

OK
```java
if (foo == bar) {
    System.out.println("equal");
} else {
    System.out.println("not equal");
}
```

## [Class Design](https://checkstyle.sourceforge.io/config_design.html)

### [FinalClass](https://checkstyle.sourceforge.io/config_design.html#FinalClass) (spymemcached)

private 생성자를 가진 클래스의 modifier가 final인지를 검사한다.

```xml
<module name="FinalClass"/>
```

VIOLATION
```java
class Foo {
    private Foo() {
    }
}
```

OK
```java
final class Foo {
    private Foo() {
    }
}
```

### [HideUtilityClassConstructor](https://checkstyle.sourceforge.io/config_design.html#HideUtilityClassConstructor) (spymemcached)

static 메소드만 가지는 util 클래스의 생성자가 private인지를 검사한다.

```xml
<module name="HideUtilityClassConstructor"/>
```

VIOLATION
```java
class Util {
    public static void add(int a, int b) { }
    public static void div(int a, int b) { }
}
```

OK
```java
class Util {
    private Util() {
    }
    public static void add(int a, int b) { }
    public static void div(int a, int b) { }
}
```

## [InterfaceIsType](https://checkstyle.sourceforge.io/config_design.html#InterfaceIsType) (spymemcached)

interface가 type으로 쓰이는지를 검사한다.

```xml
<module name="InterfaceIsType"/>
```

VIOLATION
```java
interface Foo {
    int BAR = 100;
}
```

OK
```java
class Foo {
    private Foo() {
    }
    public static final int BAR = 100;
}
```

## [VisibilityModifier](https://checkstyle.sourceforge.io/config_design.html#VisibilityModifier) (spymemcached)

클래스 멤버의 modifier가 private, protected 인지를 검사한다.

```xml
<module name="VisibilityModifier">
    <property name="protectedAllowed" value="true" />
</module>
```

VIOLATION
```java
int foo;
int bar;
public final int baz;
public int qux;
```

OK
```java
private int foo;
protected int bar;
private final int int baz
protected int qux
```


## [Coding](https://checkstyle.sourceforge.io/config_coding.html)

### [DefaultComesLast](https://checkstyle.sourceforge.io/config_coding.html#DefaultComesLast) (spymemcached)

switch에서 default 뒤에 case가 존재하는지 검사한다.

```xml
<module name="DefaultComesLast" />
```

VIOLATION
```java
switch (foo) {
    case 1:
        break;
    default:
    case 2:
        break;
}
```

OK
```java
switch (foo) {
    case 1:
        break;
    case 2:
    default:
        break;
}
```

### [EmptyStatement](https://checkstyle.sourceforge.io/config_coding.html#EmptyStatement) (spymemcached)


```xml
<module name="EmptyStatement"/>
```

VIOLATION
```java
if (foo == bar);
    System.out.println("baz");  // always print baz
```

OK
```java
if (foo == bar) {
    System.out.println("baz");
}
```

### [EqualsHashCode](https://checkstyle.sourceforge.io/config_coding.html#EqualsHashCode) (spymemcached)

equals 메소드를 override하면 hashcode 메소드도 override 했는지 검사한다.

```xml
<module name="EqualsHashCode"/>
```

VIOLATION
```java
class Foo {
    @Override
    public boolean equals(Object obj) {
        return ...
    }
}
```

OK
```java
class Foo {
    @Override
    public boolean equals(Object obj) {
        return ...
    }

    @Override
    public int hashCode() {
        return ...
    }
}
```

### [MissingSwitchDefault](https://checkstyle.sourceforge.io/config_coding.html#MissingSwitchDefault) (google, spymemcached)

switch에서 default가 존재하는지 검사한다.

```xml
<module name="MissingSwitchDefault"/>
```

VIOLATION
```java
switch (i) {
    case 1:
        break;
    case 2:
        break;
}
```

OK
```java
switch (i) {
    case 1:
        break;
    case 2:
        break;
    default:
        break;
}
```

### [SimplifyBooleanExpression](https://checkstyle.sourceforge.io/config_coding.html#SimplifyBooleanExpression) (spymemcached)

```xml
<module name="SimplifyBooleanExpression"/>
```

VIOLATION
```java
if (foo == false) { }
```

OK
```java
if (!foo) { }
```

### [SimplifyBooleanReturn](https://checkstyle.sourceforge.io/config_coding.html#SimplifyBooleanReturn) (spymemcached)

```xml
<module name="SimplifyBooleanReturn"/>
```

VIOLATION
```java
if (foo()) {
    return true;
} else {
    return false;
}
```

OK
```java
return foo();
```

### [StringLiteralEquality](https://checkstyle.sourceforge.io/config_coding.html#StringLiteralEquality) (spymemcached)

```xml
<module name="StringLiteralEquality"/>
```

VIOLATION
```java
if (foo == "bar") {
}
```

OK
```java
if (foo.equals("bar")) {
}
```

### [SuperClone](https://checkstyle.sourceforge.io/config_coding.html#SuperClone) (spymemcached)

부모의 clone() 호출을 검사한다.

```xml
<module name="SuperClone"/>
```

VIOLATION
```java
@Override
public Object clone throws CloneNotSupportedException {
    return ...
}
```

OK
```java
@Override
public Object clone throws CloneNotSUpportedException {
    super.clone();
    return ...
}
```


## [Imports](https://checkstyle.sourceforge.io/config_imports.html)

### [AvoidStarImport](https://checkstyle.sourceforge.io/config_imports.html#AvoidStarImport) (google, spymemcached)

star('*') import가 존재하는지 검사한다.

```xml
<module name="AvoidStarImport"/>
```

VIOLATION
```java
import foo.bar.*;
```

OK
```java
import foo.bar.Baz;
```

### [IllegalImport](https://checkstyle.sourceforge.io/config_imports.html#IllegalImport) (spymemcached)

sun 패키지의 import가 존재하는지 검사한다.

```xml
<module name="IllegalImport"/>
```

VIOLATION
```java
import sun.management.counter.StringCounter;
```

### [ImportOrder](https://checkstyle.sourceforge.io/config_imports.html#UnusedImports) (spymemcached)

import 순서를 검사한다.

```xml
<module name="ImportOrder">
    <property name="ordered" value="true"/>
    <property name="separated" value="true"/>
</module>
```

VIOLATION
```java
import java.util.Map;
import java.util.List;
import java.util.ArrayList;
```

OK
```java
import java.util.ArrayList;
import java.util.List;
import java.util.Map;
```

### [RedundantImport](https://checkstyle.sourceforge.io/config_imports.html#RedundantImport) (spymemcached)

java.lang, 중복, 현재 패키지의 import를 검사한다.

```xml
<module name="RedundantImport"/>
```

VIOLATION
```java
package foo;

import java.lang.String;   // java.lang
import java.lang.String;   // duplicate
import foo.Bar;            // same package
```

### [UnusedImports](https://checkstyle.sourceforge.io/config_imports.html#UnusedImports) (spymemcached)

사용되지 않는 import를 검사한다.

```xml
<module name="UnusedImports"/>
```

VIOLATION
```java
import java.util.ArrayList;

public class Foo {
    public static void main() {
        System.out.println("foo");
    }
}
```

OK
```java
public class Foo {
    public static void main() {
        System.out.println("foo");
    }
}
```

## [Javadoc Comments](https://checkstyle.sourceforge.io/config_javadoc.html)

### [JavadocStyle](https://checkstyle.sourceforge.io/config_javadoc.html#JavadocStyle) (spymemcached)

적절하지 않거나 존재하지 않는 HTML 태그 사용 및 첫 문장에 마침표를 사용했는지 검사한다.

```xml
<module name="JavadocStyle"/>
```

### [JavadocType](https://checkstyle.sourceforge.io/config_javadoc.html#JavadocType) (spymemcached)

public annotation/enum/class/interface에 JavaDoc이 존재하는지 검사한다.

```xml
<module name="JavadocType">
    <property name="scope" value="public"/>
    <property name="allowMissingParamTags" value="true"/>
</module>
```

VIOLATION
```java
class Foo { }
```

OK
```java
/**
 * This is Foo class.
 */
class Foo { }
```


## [Miscellaneous](https://checkstyle.sourceforge.io/config_misc.html)

### [ArrayTypeStyle](https://checkstyle.sourceforge.io/config_misc.html#ArrayTypeStyle) (google, spymemcached)
배열 타입 스타일을 검사한다.

```xml
<module name="ArrayTypeStyle"/>
```

VIOLATION
```java
String foo[];
```

OK
```java
String[] foo;
```

### [Indentation](https://checkstyle.sourceforge.io/config_misc.html#Indentation) (google, spymemcached)

```xml
<module name="Indentation">
    <property name="basicOffset" value="2"/>
    <property name="braceAdjustment" value="0"/>
    <property name="caseIndent" value="2"/>
    <property name="throwsIndent" value="4"/>
    <property name="lineWrappingIndentation" value="4"/>
    <property name="arrayInitIndent" value="2"/>
</module>
```

VIOLATION
```java
/* <property name="basicOffset" value="2"/> */
class Foo {
    void bar() {
    }
}

/* <property name="braceAdjustment" value="0"/> */
void bar() {
    }

/* <property name="caseIndent" value="2"/> */
switch (foo) {
    case 0:
        break;
    case 1:
        break;
    default:
        break;
}

/* <property name="throwsIndent" value="4"/> */
public static void main(String[] args) throws
  IOException {
}

/* <property name="lineWrappingIndentation" value="4"/> */
if ((foo == bar)
  && (baz == qux)) {
    System.out.println("equal");
}

/* <property name="arrayInitIndent" value="2"/> */
int[] foo = {
    5,
    6
};
```

OK
```java
/* <property name="basicOffset" value="2"/> */
class Foo {
  void bar() {
  }
}

/* <property name="braceAdjustment" value="0"/> */
void bar() {
}

/* <property name="caseIndent" value="2"/> */
switch (foo) {
  case 0:
    break;
  case 1:
    break;
  default:
    break;
}

/* <property name="throwsIndent" value="4"/> */
public static void main(String[] args) throws
    IOException {
}

/* <property name="lineWrappingIndentation" value="4"/> */
if ((foo == bar)
    && (baz == qux)) {
    System.out.println("equal");
}

/* <property name="arrayInitIndent" value="2"/> */
int[] foo = {
  5,
  6
};
```

### [NewlineAtEndOfFile](https://checkstyle.sourceforge.io/config_misc.html#NewlineAtEndOfFile) (spymemcached)

파일의 맨 끝에 newline('\n')이 존재하는지 검사한다.

```xml
<module name="NewlineAtEndOfFile"/>
```

VIOLATION
```java
1 class Foo {
2
3 }
```

OK
```java
1 class Foo {
2 
3 }
4
```

### [UpperEll](https://checkstyle.sourceforge.io/config_misc.html#UpperEll) (google, spymemcached)

long을 'l'이 아닌 'L'로 표현하는지를 검사한다.

```xml
<module name="UpperEll"/>
```

VIOLATION
```java
long value = 100l // 1001?
```

OK
```java
long value = 100L
```

## [Modifier](https://checkstyle.sourceforge.io/config_modifier.html)

### [ModifierOrder](https://checkstyle.sourceforge.io/config_modifier.html#ModifierOrder) (google, spymemcached)

modifier 순서를 검사한다.

1. public
2. protected
3. private
4. abstract
5. default
6. static
7. final
8. transient
9. volatile
10. synchronized
11. native
12. strictfp

```xml
<module name="ModifierOrder"/>
```

VIOLATION
```java
abstract public void foo();
```

OK
```java
public abstract void foo();
```

### [RedundantModifier](https://checkstyle.sourceforge.io/config_modifier.html#RedundantModifier) (spymemcached)

불필요한 modifier를 검사한다.

```xml
<module name="RedundantModifier"/>
```

VIOLATION
```java
public interface Foo {
    public void bar();
}
```

OK
```java
public interface Foo {
    void bar();
}
```

## [Naming Conventions](https://checkstyle.sourceforge.io/config_naming.html)

### [ClassTypeParameterName](https://checkstyle.sourceforge.io/config_naming.html#ClassTypeParameterName) (google, spymemcached)

클래스 제네릭 타입을 검사한다. `"(^[A-Z][0-9]?)$|([A-Z][a-zA-Z0-9]*[T]$)"` 패턴과 일치해야한다.

```xml
<module name="ClassTypeParameterName">
    <property name="format" value="(^[A-Z][0-9]?)$|([A-Z][a-zA-Z0-9]*[T]$)"/>
    <message key="name.invalidPattern"
             value="Class type name ''{0}'' must match pattern ''{1}''."/>
</module>
```

VIOLATION
```java
class MyClass<t> { }
```

OK
```java
class MyClass<T> { }
```

### [ConstantName](https://checkstyle.sourceforge.io/config_naming.html#ConstantName) (spymemcached)

static final 변수 이름을 검사한다. `"^[A-Z][A-Z0-9]*(_[A-Z0-9]+)*$"` 패턴과 일치해야 한다.

```xml
<module name="ConstantName"/>
```

VIOLATION
```java
public static final int foo = 100;
```

OK
```java
public static final int FOO = 100;
```

### [LocalFinalVariableName](https://checkstyle.sourceforge.io/config_naming.html#LocalFinalVariableName) (spymemcached)

지역 final 변수 이름을 검사한다. `"^[a-z][a-zA-Z0-9]*$"` 패턴과 일치해야한다.

```xml
<module name="LocalFinalVariableName"/>
```

VIOLATION
```java
public void foo() {
    final int BAR = 100;
    final int Bar = 100;
}
```

OK
```java
public void foo() {
    final int bar = 100;
}
```

### [LocalVariableName](https://checkstyle.sourceforge.io/config_naming.html#LocalVariableName) (google, spymemcached)

지역 변수 이름을 검사한다. `"^[a-z]([a-z0-9][a-zA-Z0-9]*)?$"` 패턴과 일치해야한다.

```xml
<module name="LocalVariableName">
    <property name="format" value="^[a-z]([a-z0-9][a-zA-Z0-9]*)?$"/>
    <message key="name.invalidPattern"
             value="Local variable name ''{0}'' must match pattern ''{1}''."/>
</module>
```

VIOLATION
```java
int foo_1;
int Foo1;
int FOO1;
```

OK
```java
int fooBar1;
```

### [MemberName](https://checkstyle.sourceforge.io/config_naming.html#MemberName) (google, spymemcached)

클래스 멤버 이름을 검사한다. `"^[a-z][a-z0-9][a-zA-Z0-9]*$"` 패턴과 일치해야한다.

```xml
<module name="MemberName">
    <property name="format" value="^[a-z][a-z0-9][a-zA-Z0-9]*$"/>
    <message key="name.invalidPattern"
             value="Member name ''{0}'' must match pattern ''{1}''."/>
</module>
```

VIOLATION
```java
public int FOO1;
protected int FOO2;
final int FOO3;
private int FOO4;
```

OK
```java
public int foo1;
protected int foo2;
final int foo3 = 3;
private int foo4;

/* static은 무시한다. */
static int FOO5 = 0;
static int foo6 = 0;
```

### [MethodName](https://checkstyle.sourceforge.io/config_naming.html#MethodName) (google, spymemcached)

메소드 이름을 검사한다. `"^[a-z][a-z0-9][a-zA-Z0-9_]*$"` 패턴과 일치해야한다.

```xml
<module name="MethodName">
    <property name="format" value="^[a-z][a-z0-9][a-zA-Z0-9_]*$"/>
    <message key="name.invalidPattern"
             value="Method name ''{0}'' must match pattern ''{1}''."/>
</module>
```

VIOLATION
```java
void Foo() { }
```

OK
```java
void foo() { }
```

### [MethodTypeParameterName](https://checkstyle.sourceforge.io/config_naming.html#MethodTypeParameterName) (google, spymemcached)

메소드 제네릭 타입 이름을 검사한다. `"(^[A-Z][0-9]?)$|([A-Z][a-zA-Z0-9]*[T]$)"` 패턴과 일치해야한다.

```xml
<module name="MethodTypeParameterName">
    <property name="format" value="(^[A-Z][0-9]?)$|([A-Z][a-zA-Z0-9]*[T]$)"/>
    <message key="name.invalidPattern"
             value="Method type name ''{0}'' must match pattern ''{1}''."/>
</module>
```

VIOLATION
```java
public <t> void foo() { }
```

OK
```java
public <T> void foo() { }
```

### [PackageName](https://checkstyle.sourceforge.io/config_naming.html#PackageName) (google, spymemcached)

패키지 이름을 검사한다. `"^[a-z]+(\.[a-z][a-z0-9]*)*$"` 패턴과 일치해야한다.

```xml
<module name="PackageName">
    <property name="format" value="^[a-z]+(\.[a-z][a-z0-9]*)*$"/>
    <message key="name.invalidPattern"
             value="Package name ''{0}'' must match pattern ''{1}''."/>
</module>
```

VIOLATION
```java
package FOO;
package foo.BAR.baz.qux;
package foo.fooBAR.bar;
package foo._bar.baz_;
```

OK
```java
package foo;
package foo.bar.baz;
package foo.bar1.baz;
```

### [ParameterName](https://checkstyle.sourceforge.io/config_naming.html#ParameterName) (google, spymemcached)

파라미터 이름을 검사한다. `"^[a-z]([a-z0-9][a-zA-Z0-9]*)?$"` 패턴과 일치해야한다.

```xml
<module name="ParameterName">
    <property name="format" value="^[a-z]([a-z0-9][a-zA-Z0-9]*)?$"/>
    <message key="name.invalidPattern"
             value="Parameter name ''{0}'' must match pattern ''{1}''."/>
</module>
```

VIOLATION
```java
void foo(int bar_2) { }

void foo(int Bar3) { }
```

OK
```java
void foo(int bar1) { }
```

### [StaticVariableName](https://checkstyle.sourceforge.io/config_naming.html#StaticVariableName) (spymemcached)

static 변수 이름을 검사한다. `"^[a-z][a-zA-Z0-9]*$"` 패턴과 일치해야한다.

```xml
<module name="StaticVariableName"/>
```

VIOLATION
```java
static int Foo = 300;
static int FOO = 300;
```

OK
```java
static int foo = 300;
```

### [TypeName](https://checkstyle.sourceforge.io/config_naming.html#TypeName) (google, spymemcached)

타입(class, interface, enum, annotation) 이름을 검사한다. `"^[A-Z][a-zA-Z0-9]*$"` 패턴과 일치해야한다.

```xml
<module name="TypeName">
    <property name="format" value="^[A-Z][a-zA-Z0-9]*$"/>
    <property name="tokens" value="CLASS_DEF, INTERFACE_DEF, ENUM_DEF, ANNOTATION_DEF"/>
    <message key="name.invalidPattern"
             value="Type name ''{0}'' must match pattern ''{1}''."/>
</module>
```

VIOLATION
```java
class myClass { }
```

OK
```java
class MyClass { }
```


## [Regexp](https://checkstyle.sourceforge.io/config_regexp.html)

### [Regexp](https://checkstyle.sourceforge.io/config_regexp.html#Regexp) (spymemcached)

라인 뒤에 공백(' ') 혹은 탭('\t') 문자가 존재하는지 검사한다.

```xml
<module name="Regexp">
    <property name="format" value="[ \t]+$"/>
    <property name="illegalPattern" value="true"/>
    <property name="message" value="Trailing whitespace"/>
</module>
```


## [Size Violations](https://checkstyle.sourceforge.io/config_sizes.html)

### [FileLength](https://checkstyle.sourceforge.io/config_sizes.html#FileLength) (spymemcached)

한 파일이 2500 라인을 초과했는지 검사한다.

```xml
<module name="FileLength">
    <property name="max" value="2500"/>
</module>
```

### [LineLength](https://checkstyle.sourceforge.io/config_sizes.html#LineLength) (google, spymemcached)

한 라인에 100 캐릭터를 초과했는지 검사한다.

```xml
<module name="LineLength">
    <property name="fileExtensions" value="java"/>
    <property name="max" value="100"/>
    <property name="ignorePattern" value="^package.*|^import.*|a href|href|http://|https://|ftp://"/>
</module>
```

VIOLATION
```java
String foo = "foooooooooooooooooooooooooooooooooooooooooooooooooooooooooo...";
```

OK
```java
String foo = "fooooooooooooooooo" +
             "oooooooooooooooooo" +
             "ooooooooooooooo...";
```

### [MethodLength](https://checkstyle.sourceforge.io/config_sizes.html#MethodLength) (spymemcached)

메소드가 150 라인을 초과했는지 검사한다.

```xml
<module name="MethodLength"/>
```

### [ParameterNumber](https://checkstyle.sourceforge.io/config_sizes.html#ParameterNumber) (spymemcached)

파라미터 개수가 10개를 초과했는지 검사한다.

```xml
<module name="ParameterNumber">
    <property name="max" value="10"/>
</module>
```

VIOLATION
```java
void foo(int a, int b, int c, int d, int e, int f, int g, int h, int i, int j) {
}
```


## [Whitespace](https://checkstyle.sourceforge.io/config_whitespace.html)

### [EmptyForIteratorPad](https://checkstyle.sourceforge.io/config_whitespace.html#EmptyForIteratorPad) (spymemcached)

for loop의 공백을 검사한다.

```xml
<module name="EmptyForIteratorPad"/>
```

VIOLATION
```java
int foo = 0;
for ( ; foo < 100; ) {
    foo++;
}
```

OK
```java
int foo = 0;
for (; foo < 100;) {
    foo++;
}
```

### [FileTabCharacter](https://checkstyle.sourceforge.io/config_whitespace.html#FileTabCharacter) (google, spymemcached)

탭('\t') 문자가 존재하는지 검사한다.

```xml
<module name="FileTabCharacter">
    <property name="eachLine" value="true"/>
</module>
```

### [GenericWhiteSpace](https://checkstyle.sourceforge.io/config_whitespace.html#GenericWhitespace) (google, spymemcached)

제네릭의 공백 규칙을 검사한다.

```xml
<module name="GenericWhitespace">
    <message key="ws.followed"
                value="GenericWhitespace ''{0}'' is followed by whitespace."/>
    <message key="ws.preceded"
                value="GenericWhitespace ''{0}'' is preceded with whitespace."/>
    <message key="ws.illegalFollow"
                value="GenericWhitespace ''{0}'' should followed by whitespace."/>
    <message key="ws.notPreceded"
                value="GenericWhitespace ''{0}'' is not preceded with whitespace."/>
</module>
```

VIOLATION
```java
List <String> foo;
List<String>bar;
List< String> baz;
List<String > qux;

public< X, Y >X quux(X x, Y y) {
    return ...;
}
```

OK
```java
List<String> foo;

public <X, Y> X bar(X x, Y y) {
    return ...;
}
```

### [MethodParamPad](https://checkstyle.sourceforge.io/config_whitespace.html#MethodParamPad) (google, spymemcached)

메소드와 파라미터 사이의 공백을 검사한다.

```xml
<module name="MethodParamPad">
    <property name="tokens"
                value="CTOR_DEF, LITERAL_NEW, METHOD_CALL, METHOD_DEF,
                        SUPER_CTOR_CALL, ENUM_CONSTANT_DEF"/>
</module>
```

VIOLATION
```java
public void foo (int bar) {
    Baz baz = new Baz ();
    baz.qux (1);
}
```

OK
```java
public void foo(int bar) {
    Baz baz = new Baz();
    baz.qux(1);
}
```

### [NoWhitespaceAfter](https://checkstyle.sourceforge.io/config_whitespace.html#NoWhitespaceAfter) (spymemcached)

토큰 뒤의 공백을 검사한다.

```xml
<module name="NoWhitespaceAfter"/>
```

VIOLATION
```java
if (! foo) {
    ++ bar;
}
```

OK
```java
if (!foo) {
    ++bar;
}
```

### [NoWhitespaceBefore](https://checkstyle.sourceforge.io/config_whitespace.html#NoWhitespaceBefore) (google, spymemcached)

토큰 앞의 공백을 검사한다.

```xml
<module name="NoWhitespaceBefore">
    <property name="tokens"
              value="COMMA, SEMI, POST_INC, POST_DEC, DOT, ELLIPSIS, METHOD_REF"/>
    <property name="allowLineBreaks" value="true"/>
</module>
```

VIOLATION
```java
int foo = 0 ;
foo ++;
this .bar(1, 2, 3);
this.bar(1 , 2 , 3);
```

OK
```java
int foo = 0;
foo++;
this.bar(1, 2, 3);
```

### [OperatorWrap](https://checkstyle.sourceforge.io/config_whitespace.html#OperatorWrap) (google, spymemcached)

연산자의 줄바꿈을 검사한다.

```xml
<module name="OperatorWrap">
    <property name="option" value="NL"/>
    <property name="tokens"
              value="BAND, BOR, BSR, BXOR, DIV, EQUAL, GE, GT, LAND, LE, LITERAL_INSTANCEOF, LOR,
                     LT, MINUS, MOD, NOT_EQUAL, PLUS, QUESTION, SL, SR, STAR, METHOD_REF "/>
</module>
```

VIOLATION
```java
String foo = "A" +
    "B";

if ((bar == baz) &&
    (qux == quux)) {
    System.out.println("equal");
}
```

OK
```java
String foo = "A"
    + "B";

if ((bar == baz)
    && (qux == quux)) {
    System.out.println("equal");
}
```
        
### [ParenPad](https://checkstyle.sourceforge.io/config_whitespace.html#ParenPad) (google, spymemcached)

괄호 사이의 공백을 검사한다.

```xml
<module name="ParenPad">
    <property name="tokens"
                value="ANNOTATION, ANNOTATION_FIELD_DEF, CTOR_CALL, CTOR_DEF, DOT,          
                       ENUM_CONSTANT_DEF,
                       EXPR, LITERAL_CATCH, LITERAL_DO, LITERAL_FOR, LITERAL_IF, LITERAL_NEW,
                       LITERAL_SWITCH, LITERAL_SYNCHRONIZED, LITERAL_WHILE, METHOD_CALL,
                       METHOD_DEF, QUESTION, RESOURCE_SPECIFICATION, SUPER_CTOR_CALL, LAMBDA"/>
</module>
```

VIOLATION
```java
new String( "foo" );
this.bar( "bar" );
```

OK
```java
new String("foo");
this.bar("bar");
```

### [TypecastParenPad](https://checkstyle.sourceforge.io/config_whitespace.html#TypecastParenPad) (spymemcached)

타입 변환 괄호 사이의 공백을 검사한다.

```xml
<module name="TypecastParenPad"/>
```

VIOLATION
```java
foo = ( String ) bar;
```

OK
```java
foo = (String) bar;
```

### [WhitespaceAfter](https://checkstyle.sourceforge.io/config_whitespace.html#WhitespaceAfter) (spymemcached)

comma(','), semi-colon(';') 뒤의 공백을 검사한다.

```xml
<module name="WhitespaceAfter">
    <property name="tokens" value="COMMA, SEMI"/>
</module>
```

VIOLATION
```java
void foo(int bar,int baz) {
}
```

OK
```java
void foo(int bar, int baz) {
}
```