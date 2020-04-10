# Checkstyle

[Checkstyle](https://checkstyle.sourceforge.io/)에서 제공되는 모듈 내용을 정리한다.
- [Google Checkstyle 8.31](https://github.com/checkstyle/checkstyle/blob/checkstyle-8.31/src/main/resources/google_checks.xml)
- [Spymemcached Checkstyle 2.12.3](https://github.com/couchbase/spymemcached/blob/2.12.3/etc/checkstyle.xml)


Link
- [File Filters](javacheckstyle.md#File-Filters)
    - [BeforeExecutionExclusionFileFilter](javacheckstyle.md#BeforeExecutionExclusionFileFilter)
- [Annotations](javacheckstyle.md#Annotations)
    - [AnnotationLocation](javacheckstyle.md#AnnotationLocation)
    - [MissingOverride](javacheckstyle.md#MissingOverride)
- [Block Checks](javacheckstyle.md#Block-Checks)
    - [AvoidNestedBlocks](javacheckstyle.md#AvoidNestedBlocks)
    - [EmptyBlock](javacheckstyle.md#EmptyBlock)
    - [EmptyCatchBlock](javacheckstyle.md#EmptyCatchBlock)
    - [LeftCurly](javacheckstyle.md#LeftCurly)
    - [NeedBraces](javacheckstyle.md#NeedBraces)
    - [RightCurly](javacheckstyle.md#RightCurly)
- [Class Design](javacheckstyle.md#Class-Design)
    - [FinalClass](javacheckstyle.md#FinalClass)
    - [HideUtilityClassConstructor](javacheckstyle.md#HideUtilityClassConstructor)
    - [InterfaceIsType](javacheckstyle.md#InterfaceIsType)
    - [OneTopLevelClass](javacheckstyle.md#OneTopLevelClass)
    - [VisibilityModifier](javacheckstyle.md#VisibilityModifier)
- [Coding](javacheckstyle.md#Coding)
    - [DefaultComesLast](javacheckstyle.md#DefaultComesLast)
    - [EmptyStatement](javacheckstyle.md#EmptyStatement)
    - [EqualsHashCode](javacheckstyle.md#EqualsHashCode)
    - [FallThrough](javacheckstyle.md#FallThrough)
    - [IllegalTokenText](javacheckstyle.md#IllegalTokenText)
    - [MissingSwitchDefault](javacheckstyle.md#MissingSwitchDefault)
    - [MultipleVariableDeclarations](javacheckstyle.md#MultipleVariableDeclarations)
    - [NoFinalizer](javacheckstyle.md#NoFinalizer)
    - [OneStatementPerLine](javacheckstyle.md#OneStatementPerLine)
    - [OverloadMethodsDeclarationOrder](javacheckstyle.md#OverloadMethodsDeclarationOrder)
    - [SimplifyBooleanExpression](javacheckstyle.md#SimplifyBooleanExpression)
    - [SimplifyBooleanReturn](javacheckstyle.md#SimplifyBooleanReturn)
    - [StringLiteralEquality](javacheckstyle.md#StringLiteralEquality)
    - [SuperClone](javacheckstyle.md#SuperClone)
    - [VariableDeclarationUsageDistance](javacheckstyle.md#VariableDeclarationUsageDistance)
- [Imports](javacheckstyle.md#Imports)
    - [AvoidStarImport](javacheckstyle.md#AvoidStarImport)
    - [CustomImportOrder](javacheckstyle.md#CustomImportOrder)
    - [IllegalImport](javacheckstyle.md#IllegalImport)
    - [RedundantImport](javacheckstyle.md#RedundantImport)
    - [UnusedImports](javacheckstyle.md#UnusedImports)
- [Javadoc Comments](javacheckstyle.md#Javadoc-Comments)
    - [AtclauseOrder](javacheckstyle.md#AtclauseOrder)
    - [JavadocMethod](javacheckstyle.md#JavadocMethod)
    - [InvalidJavadocPosition](javacheckstyle.md#InvalidJavadocPosition)
    - [JavadocParagraph](javacheckstyle.md#JavadocParagraph)
    - [JavadocStyle](javacheckstyle.md#JavadocStyle)
    - [JavadocTagContinuationIndentation](javacheckstyle.md#JavadocTagContinuationIndentation)
    - [JavadocType](javacheckstyle.md#JavadocType)
    - [MissingJavadocMethod](javacheckstyle.md#MissingJavadocMethod)
    - [NonEmptyAtclauseDescription](javacheckstyle.md#NonEmptyAtclauseDescription)
    - [SingleLineJavadoc](javacheckstyle.md#SingleLineJavadoc)
    - [SummaryJavadoc](javacheckstyle.md#SummaryJavadoc)
- [Miscellaneous](javacheckstyle.md#Miscellaneous)
    - [ArrayTypeStyle](javacheckstyle.md#ArrayTypeStyle)
    - [AvoidEscapedUnicodeCharacters](javacheckstyle.md#AvoidEscapedUnicodeCharacters)
    - [CommentsIndentation](javacheckstyle.md#CommentsIndentation)
    - [Indentation](javacheckstyle.md#Indentation)
    - [NewlineAtEndOfFile](javacheckstyle.md#NewlineAtEndOfFile)
    - [OuterTypeFilename](javacheckstyle.md#OuterTypeFilename)
    - [UpperEll](javacheckstyle.md#UpperEll)
- [Modifier](javacheckstyle.md#Modifier)
    - [ModifierOrder](javacheckstyle.md#ModifierOrder)
    - [RedundantModifier](javacheckstyle.md#RedundantModifier)
- [Naming Conventions](javacheckstyle.md#Naming-Conventions)
    - [AbbreviationAsWordInName](javacheckstyle.md#AbbreviationAsWordInName)
    - [CatchParameterName](javacheckstyle.md#CatchParameterName)
    - [ClassTypeParameterName](javacheckstyle.md#ClassTypeParameterName)
    - [ConstantName](javacheckstyle.md#ConstantName)
    - [InterfaceTypeParameterName](javacheckstyle.md#InterfaceTypeParameterName)
    - [LambdaParameterName](javacheckstyle.md#LambdaParameterName)
    - [LocalFinalVariableName](javacheckstyle.md#LocalFinalVariableName)
    - [LocalVariableName](javacheckstyle.md#LocalVariableName)
    - [MemberName](javacheckstyle.md#MemberName)
    - [MethodName](javacheckstyle.md#MethodName)
    - [MethodTypeParameterName](javacheckstyle.md#MethodTypeParameterName)
    - [PackageName](javacheckstyle.md#PackageName)
    - [ParameterName](javacheckstyle.md#ParameterName)
    - [StaticVariableName](javacheckstyle.md#StaticVariableName)
    - [TypeName](javacheckstyle.md#TypeName)
- [Regexp](javacheckstyle.md#Regexp)
    - [Regexp](javacheckstyle.md#Regexp)
- [Size Violations](javacheckstyle.md#Size-Violations)
    - [FileLength](javacheckstyle.md#FileLength)
    - [LineLength](javacheckstyle.md#LineLength)
    - [MethodLength](javacheckstyle.md#MethodLength)
    - [ParameterNumber](javacheckstyle.md#ParameterNumber)
- [Whitespace](javacheckstyle.md#Whitespace)
    - [EmptyForIteratorPad](javacheckstyle.md#EmptyForIteratorPad)
    - [EmptyLineSeparator](javacheckstyle.md#EmptyLineSeparator)
    - [FileTabCharacter](javacheckstyle.md#FileTabCharacter)
    - [GenericWhiteSpace](javacheckstyle.md#GenericWhiteSpace)
    - [MethodParamPad](javacheckstyle.md#MethodParamPad)
    - [NoLineWrap](javacheckstyle.md#NoLineWrap)
    - [NoWhitespaceAfter](javacheckstyle.md#NoWhitespaceAfter)
    - [NoWhitespaceBefore](javacheckstyle.md#NoWhitespaceBefore)
    - [OperatorWrap](javacheckstyle.md#OperatorWrap)
    - [ParenPad](javacheckstyle.md#ParenPad)
    - [SeparatorWrap](javacheckstyle.md#SeparatorWrap)
    - [TypecastParenPad](javacheckstyle.md#TypecastParenPad)
    - [WhitespaceAfter](javacheckstyle.md#WhitespaceAfter)
    - [WhitespaceAround](javacheckstyle.md#WhitespaceAround)


## [File Filters](https://checkstyle.sourceforge.io/config_filefilters.html)

### [BeforeExecutionExclusionFileFilter](https://checkstyle.sourceforge.io/config_filefilters.html#BeforeExecutionExclusionFileFilter)

checkstyle 검사를 제외할 파일 패턴 설정.

```xml
<module name="BeforeExecutionExclusionFileFilter">
    <property name="fileNamePattern" value="module\-info\.java$"/>
</module>
```


## [Annotations](https://checkstyle.sourceforge.io/config_annotation.html)

### [AnnotationLocation](https://checkstyle.sourceforge.io/config_annotation.html#AnnotationLocation)

annotation의 위치를 검사.

```xml
<module name="AnnotationLocation">
    <property name="id" value="AnnotationLocationMostCases"/>
    <property name="tokens"
            value="CLASS_DEF, INTERFACE_DEF, ENUM_DEF, METHOD_DEF, CTOR_DEF"/>
</module>
<module name="AnnotationLocation">
    <property name="id" value="AnnotationLocationVariables"/>
    <property name="tokens" value="VARIABLE_DEF"/>
    <property name="allowSamelineMultipleAnnotations" value="true"/>
</module>
```

VIOLATION
```java
@Override @Nullable
public String foo() {
    return "bar";
}

@SuppressWarnings("deprecation") public String foo() {
    return "bar";
}
```

OK
```java
@Override
@Nullable
public String foo() {
    return "bar";
}

@SuppressWarnings("deprecation")
public String foo() {
    return "bar";
}

// allow one single parameterless annotation on the same line
@Override public String foo() {
    return "bar";
}

@SuppressWarnings("deprecation") @Mock DataLoader loader;
```

### [MissingOverride](https://checkstyle.sourceforge.io/config_annotation.html#MissingOverride)

@inheritDoc이 부여된 메소드가 override 됐는지를 검사.

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

### [AvoidNestedBlocks](https://checkstyle.sourceforge.io/config_blocks.html#AvoidNestedBlocks)

nested block이 존재하는지 검사.

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

### [EmptyBlock](https://checkstyle.sourceforge.io/config_blocks.html#EmptyBlock)

empty block이 존재하는지 검사.

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

### [EmptyCatchBlock](https://checkstyle.sourceforge.io/config_blocks.html#EmptyCatchBlock)

비어있는 catch block을 검사.

```xml
<module name="EmptyCatchBlock">
    <property name="exceptionVariableName" value="expected"/>
</module>
```

VIOLATION
```java
try {
    throw new RuntimeException();
} catch (RuntimeException e) {
}
```

OK
```java
try {
    throw new RuntimeException();
} catch (RuntimeException expected) {
}

try {
    throw new RuntimeException();
} catch (RuntimeException e) {
    e.printStackTrace();
}
```

### [LeftCurly](https://checkstyle.sourceforge.io/config_blocks.html#LeftCurly)

LeftCurly('{')의 줄바꿈을 검사.

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

### [NeedBraces](https://checkstyle.sourceforge.io/config_blocks.html#NeedBraces)

brace('{', '}')가 존재하는지 검사.

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

### [RightCurly](https://checkstyle.sourceforge.io/config_blocks.html#RightCurly)

RightCurly('}')의 줄바꿈을 검사.

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

### [FinalClass](https://checkstyle.sourceforge.io/config_design.html#FinalClass)

private 생성자를 가진 클래스의 modifier가 final인지를 검사.

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

### [HideUtilityClassConstructor](https://checkstyle.sourceforge.io/config_design.html#HideUtilityClassConstructor)

static 메소드만 가지는 util 클래스의 생성자가 private인지를 검사.

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

## [InterfaceIsType](https://checkstyle.sourceforge.io/config_design.html#InterfaceIsType)

interface가 type으로 쓰이는지를 검사.

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

### [OneTopLevelClass](https://checkstyle.sourceforge.io/config_design.html#OneTopLevelClass)

하나의 파일에 두개 이상의 클래스를 정의했는지를 검사.

```xml
<module name="OneTopLevelClass"/>
```

VIOLATION
```java
// Parent.java
class Parent {
}
class Child {
}
```

OK
```java
// Parent.java
class Parent {
}

// Child.java
class Child {
}
```

## [VisibilityModifier](https://checkstyle.sourceforge.io/config_design.html#VisibilityModifier)

클래스 멤버의 modifier가 private, protected 인지를 검사.

```xml
<module name="VisibilityModifier">
    <property name="protectedAllowed" value="true"/>
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

### [DefaultComesLast](https://checkstyle.sourceforge.io/config_coding.html#DefaultComesLast)

switch에서 default 뒤에 case가 존재하는지 검사.

```xml
<module name="DefaultComesLast"/>
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

### [EmptyStatement](https://checkstyle.sourceforge.io/config_coding.html#EmptyStatement)


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

### [EqualsHashCode](https://checkstyle.sourceforge.io/config_coding.html#EqualsHashCode)

equals 메소드를 override하면 hashcode 메소드도 override 했는지 검사.

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


### [FallThrough](https://checkstyle.sourceforge.io/config_coding.html#FallThrough)

switch-case에 fall through를 하는 곳에 `"falls?[ -]?thr(u|ough)"` 패턴의 주석이 존재하는지 검사.

```xml
<module name="FallThrough">
    <property name="reliefPattern" value="falls?[ -]?thr(u|ough)"/>
</module>
```

VIOLATION
```java
int i = 0;
switch (i) {
    case 0:
        i++;
    case 1:
        i++;
    case 2:
    case 3: {
        i++;
    }
    default:
    break;
}
```

OK
```java
int i = 0;
switch (i) {
    case 0:
        i++;
    // fall through
    case 1:
        i++;
    // fall through
    case 2:
    case 3: {
        i++;
    }
    // fall through
    default:
    break;
}
```


### [IllegalTokenText](https://checkstyle.sourceforge.io/config_coding.html#IllegalTokenText)

escape sequence를 8진수, 유니코드로 표현했는지를 검사.

```xml
<module name="IllegalTokenText">
    <property name="tokens" value="STRING_LITERAL, CHAR_LITERAL"/>
    <property name="format"
              value="\\u00(09|0(a|A)|0(c|C)|0(d|D)|22|27|5(C|c))|\\(0(10|11|12|14|15|42|47)| 134)"/>
    <property name="message"
              value="Consider using special escape sequence instead of octal value or Unicode  escaped value."/>
</module>
```

VIOLATION
```java
char tab = '\u0009';
char octalTab = '\011';
```

OK
```java
char escapedSequenceTab = '\t';
```


### [MissingSwitchDefault](https://checkstyle.sourceforge.io/config_coding.html#MissingSwitchDefault)

switch에서 default가 존재하는지 검사.

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

### [MultipleVariableDeclarations](https://checkstyle.sourceforge.io/config_coding.html#MultipleVariableDeclarations)

변수를 comma(',')를 사용하여 정의하였는지 검사.

```xml
<module name="MultipleVariableDeclarations"/>
```

VIOLATION
```java
int foo, bar, fooarray[];
```

OK
```java
int foo;
int bar;
int[] fooarray;
```

### [NoFinalizer](https://checkstyle.sourceforge.io/config_coding.html#NoFinalizer)

finalize 메소드를 override 했는지 검사.

```xml
<module name="NoFinalizer"/>
```

VIOLATION
```java
class Foo {

    @Override
    protected void finalize() throws Throwable {
        super.finalize();
    }

}
```

OK
```java
class Foo {
}
```

### [OneStatementPerLine](https://checkstyle.sourceforge.io/config_coding.html#OneStatementPerLine)

한 라인에 다수의 statement가 존재하는지 검사.

```xml
<module name="OneStatementPerLine"/>
```

VIOLATION
```java
int var = 1, var2 = 2;
foo++; bar++;
```

OK
```java
int var = 1
int var2 = 2;
var1++;
var2++;
```

### [OverloadMethodsDeclarationOrder](https://checkstyle.sourceforge.io/config_coding.html#OverloadMethodsDeclarationOrder)

오버로드 메소드의 순서를 검사.

```xml
<module name="OverloadMethodsDeclarationOrder"/>
```

VIOLATION
```java
public void foo(int i) { }

public void foo(String s) { }

public void bar() { }

public void foo(int i, String s) { }
```

OK
```java
public void foo(int i) { }

public void foo(String s) { }

public void foo(int i, String s) { }

public void bar() { }
```

### [SimplifyBooleanExpression](https://checkstyle.sourceforge.io/config_coding.html#SimplifyBooleanExpression)

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

### [SimplifyBooleanReturn](https://checkstyle.sourceforge.io/config_coding.html#SimplifyBooleanReturn)

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

### [StringLiteralEquality](https://checkstyle.sourceforge.io/config_coding.html#StringLiteralEquality)

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

### [SuperClone](https://checkstyle.sourceforge.io/config_coding.html#SuperClone)

부모의 clone() 호출을 검사.

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

### [VariableDeclarationUsageDistance](https://checkstyle.sourceforge.io/config_coding.html#VariableDeclarationUsageDistance)

변수 정의와 변수 사용 사이의 거리가 3을 초과하지 않았는지를 검사.

```xml
<module name="VariableDeclarationUsageDistance">
    <property name="allowedDistance" value="3"/>
</module>
```

VIOLATION
```java
int foo = 0;
int bar = 0;
int baz;
foo = foo + bar;  // foo distance is 3     : OK
bar = foo + foo;  // bar distance is 3     : OK
int qux;
baz = bar;        // baz distance is 4     : VIOLATION
```

OK
```java
int foo = 0;
int bar = 0;
int baz;
foo = foo + bar;  // foo distance is 3     : OK
bar = foo + foo;  // bar distance is 3     : OK
baz = bar;        // baz distance is 3     : OK
```

## [Imports](https://checkstyle.sourceforge.io/config_imports.html)

### [AvoidStarImport](https://checkstyle.sourceforge.io/config_imports.html#AvoidStarImport)

star('*') import가 존재하는지 검사.

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

### [CustomImportOrder](https://checkstyle.sourceforge.io/config_imports.html#CustomImportOrder)

import 순서를 검사.

```xml
<module name="CustomImportOrder">
    <property name="sortImportsInGroupAlphabetically" value="true"/>
    <property name="separateLineBetweenGroups" value="true"/>
    <property name="customImportOrderRules" value="STATIC###THIRD_PARTY_PACKAGE"/>
    <property name="tokens" value="IMPORT, STATIC_IMPORT, PACKAGE_DEF"/>
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

### [IllegalImport](https://checkstyle.sourceforge.io/config_imports.html#IllegalImport)

sun 패키지의 import가 존재하는지 검사.

```xml
<module name="IllegalImport"/>
```

VIOLATION
```java
import sun.management.counter.StringCounter;
```

### [RedundantImport](https://checkstyle.sourceforge.io/config_imports.html#RedundantImport)

java.lang, 중복, 현재 패키지의 import를 검사.

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

### [UnusedImports](https://checkstyle.sourceforge.io/config_imports.html#UnusedImports)

사용되지 않는 import를 검사.

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

### [AtclauseOrder](https://checkstyle.sourceforge.io/config_javadoc.html#AtclauseOrder)

tag 순서를 검사.

1. @param
2. @return
3. @throws
4. @deprecated

```xml
<module name="AtclauseOrder">
    <property name="tagOrder" value="@param, @return, @throws, @deprecated"/>
    <property name="target"
              value="CLASS_DEF, INTERFACE_DEF, ENUM_DEF, METHOD_DEF, CTOR_DEF, VARIABLE_DEF"/>
</module>
```

VIOLATION
```java
/**
 * @return bar string
 * @param foo foo integer
 * @param bar bar integer
 */
public String foo(int foo, int bar) {
    return "bar";
}
```

OK
```java
/**
 * @param foo foo integer
 * @param bar bar integer
 * @return bar string
 */
public String foo(int foo, int bar) {
    return "bar";
}
```

### [JavadocMethod](https://checkstyle.sourceforge.io/config_javadoc.html#JavadocMethod)

public 메소드에서 @param, @return tag 생략이 가능하도록 함.

```xml
<module name="JavadocMethod">
    <property name="scope" value="public"/>
    <property name="allowMissingParamTags" value="true"/>
    <property name="allowMissingReturnTag" value="true"/>
    <property name="allowedAnnotations" value="Override, Test"/>
    <property name="tokens" value="METHOD_DEF, CTOR_DEF, ANNOTATION_FIELD_DEF"/>
</module>
```

OK
```java
// allow missing @param, @return tag */
/**
 * This is foo method.
 */
public String foo(int foo, int bar) {
    return "bar";
}
```

### [InvalidJavadocPosition](https://checkstyle.sourceforge.io/config_javadoc.html#InvalidJavadocPosition)

부적절한 javadoc의 위치를 검사.

```xml
<module name="InvalidJavadocPosition"/>
```

VIOLATION
```java
@SuppressWarnings("foo")
/**
 * This comment looks like javadoc but it at an invalid location.
 * Therefore, the text will not get into Foo.html and the check will produce a violation.
 */
public class Foo {
}
```

OK
```java
/**
 * This comment looks like javadoc but it at an invalid location.
 * Therefore, the text will not get into Foo.html and the check will produce a violation.
 */
@SuppressWarnings("foo")
public class Foo {
}
```

### [JavadocParagraph](https://checkstyle.sourceforge.io/config_javadoc.html#JavadocParagraph)

paragraph(`<p>`) 태그를 검사.

```xml
<module name="JavadocParagraph"/>
```

VIOLATION
```java
/**
 * No tag
 *
 * <p>Tag immediately before the text.
 * <p>No blank line before the tag.
 *
 * <p>
 * New line after tag.
 *
 * <p> Whitespace after tag.
 */
public class TestClass {
}
```

OK
```java
/**
 * No tag
 *
 * <p>Tag immediately before the text.
 *
 * <p>No blank line before the tag.
 *
 * <p>New line after tag.
 *
 * <p>Whitespace after tag.
 */
```

### [JavadocStyle](https://checkstyle.sourceforge.io/config_javadoc.html#JavadocStyle)

적절하지 않거나 존재하지 않는 HTML 태그 사용 및 첫 문장에 마침표를 사용했는지 검사.

```xml
<module name="JavadocStyle"/>
```

VIOLATION
```java
/**
 * This is Foo class
 * <foo>This is Foo class</foo>
 */
class Foo {
}
```

OK
```java
/**
 * This is Foo class.
 * <h1>This is Foo class</h1>
 */
class Foo {
}
```

### [JavadocTagContinuationIndentation](https://checkstyle.sourceforge.io/config_javadoc.html#JavadocTagContinuationIndentation)

indentation (4 spaces) 검사.

```xml
<module name="JavadocTagContinuationIndentation"/>
```

VIOLATION
```java
/**
 * @param foo
 *   foo integer
 * @param bar
 *   bar integer
 * @return bar string
 */
public String foo(int foo, int bar) {
    return "bar";
}
```

OK
```java
/**
 * @param foo
 *     foo integer
 * @param bar
 *     bar integer
 * @return bar string
 */
```

### [JavadocType](https://checkstyle.sourceforge.io/config_javadoc.html#JavadocType)

public type(annotation/enum/class/interface)에서 @param 생략이 가능하도록 함

```xml
<module name="JavadocType">
    <property name="scope" value="public"/>
    <property name="allowMissingParamTags" value="true"/>
</module>
```

OK
```java
// allow missing @param tag */
/**
 * This is Foo class
 */
public class Foo<T> {
    ...
}
```

### [MissingJavadocMethod](https://checkstyle.sourceforge.io/config_javadoc.html#MissingJavadocMethod)

2라인을 넘어가는 메소드의 javadoc이 존재하는지 검사.

```xml
<module name="MissingJavadocMethod">
    <property name="scope" value="public"/>
    <property name="minLineCount" value="2"/>
    <property name="allowedAnnotations" value="Override, Test"/>
    <property name="tokens" value="METHOD_DEF, CTOR_DEF, ANNOTATION_FIELD_DEF"/>
</module>
```

VIOLATION
```java
public String foo(int foo, int bar) { // minLineCount is > 2
    System.out.println("foo");
    System.out.println("bar");
    return "bar";
}
```

OK
```java
/**
 * This is foo method.
 */
public String foo(int foo, int bar) {
    System.out.println("foo");
    System.out.println("bar");
    return "bar";
}

public String foo(int foo, int bar) { // minLineCount is <= 2
    System.out.println("foo");
    return "bar";
}

@Override
public String foo(int foo, int bar) { // @Override, @Test is allowed
    System.out.println("foo");
    System.out.println("bar");
    return "bar";
}
```

### [NonEmptyAtclauseDescription](https://checkstyle.sourceforge.io/config_javadoc.html#NonEmptyAtclauseDescription)

@param, @return, @throws, @deprecated의 설명이 존재하는지 검사.

```xml
<module name="NonEmptyAtclauseDescription"/>
```

VIOLATION
```java
/**
 * @param foo
 * @param bar
 * @return bar string
 */
public String foo(int foo, int bar) {
    return "bar";
}
```

OK
```java
/**
 * @param foo foo integer
 * @param bar bar integer
 * @return bar string
 */
public String foo(int foo, int bar) {
    return "bar";
}
```

### [SingleLineJavadoc](https://checkstyle.sourceforge.io/config_javadoc.html#SingleLineJavadoc)

단일 라인의 inline 태그가 존재하는지 검사.

```xml
<module name="SingleLineJavadoc">
    <property name="ignoreInlineTags" value="false"/>
</module>
```

VIOLATION
```java
/** Single line Javadoc that references {@link String}. */
public void foo() { // not allowed inline tag. only allowed multi-line 
}
```

OK
```java
/**
 * Single line Javadoc that references {@link String}.
 */
public void foo() {
}

/** Single line Javadoc. */
public void foo() {
}
```

### [SummaryJavadoc](https://checkstyle.sourceforge.io/config_javadoc.html#SummaryJavadoc)

summary 첫 문장이 마침표로 끝나는지 검사.

```xml
<module name="SummaryJavadoc">
    <property name="forbiddenSummaryFragments"
              value="^@return the *|^This method returns |^A [{]@code [a-zA-Z0-9]+[}]( is a )"/>
</module>
```

VIOLATION
```java
/**
 * This is foo method
 */
public String foo(int foo, int bar) {
    return "bar";
}

/**
 *
 */
public String baz() {
    return "qux";
}
```

OK
```java
/**
 * This is foo method.
 */
public String foo(int foo, int bar) {
    return "bar";
}
```

## [Miscellaneous](https://checkstyle.sourceforge.io/config_misc.html)

### [ArrayTypeStyle](https://checkstyle.sourceforge.io/config_misc.html#ArrayTypeStyle)
배열 타입 스타일을 검사.

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

### [AvoidEscapedUnicodeCharacters](https://checkstyle.sourceforge.io/config_misc.html#AvoidEscapedUnicodeCharacters)

유니코드를 사용했는지 검사.

```xml
<module name="AvoidEscapedUnicodeCharacters">
    <property name="allowEscapesForControlCharacters" value="true"/>
    <property name="allowByTailComment" value="true"/>
    <property name="allowNonPrintableEscapes" value="true"/>
</module>
```

VIOLATION
```java
String foo = "\u00B5"; // micro sign
```

OK
```java
String foo = "μs";     // micro sign

// allowEscapesForControlCharacters
String bar = "\u200E";
// allow by allowByTailComment
String baz = "\u03BCS"; // the reader has no idea what this is.
// allow by allowNonPrintableEscapes */
String qux = "\u0020";
```

### [CommentsIndentation](https://checkstyle.sourceforge.io/config_misc.html#CommentsIndentation)

주석의 indentation을 검사.

```xml
<module name="CommentsIndentation">
    <property name="tokens" value="SINGLE_LINE_COMMENT, BLOCK_COMMENT_BEGIN"/>
</module>
```

VIOLATION
```java
    /*
    foo is true
*/
boolean foo = true;

    // bar is true
boolean bar = true;
```

OK
```java
/*
    foo is true
*/
boolean foo = true;

// bar is true
boolean bar = true;
```

### [Indentation](https://checkstyle.sourceforge.io/config_misc.html#Indentation)

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

### [NewlineAtEndOfFile](https://checkstyle.sourceforge.io/config_misc.html#NewlineAtEndOfFile)

파일의 맨 끝에 newline('\n')이 존재하는지 검사.

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

### [OuterTypeFilename](https://checkstyle.sourceforge.io/config_misc.html#OuterTypeFilename)

파일 이름과 클래스명이 일치하는지 검사.

```xml
<module name="OuterTypeFilename"/>
```

VIOLATION
```java
// Foo.java
class Bar {
}
```

OK
```java
// Foo.java
class Foo {
}
```

### [UpperEll](https://checkstyle.sourceforge.io/config_misc.html#UpperEll)

long을 'l'이 아닌 'L'로 표현하는지를 검사.

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

### [ModifierOrder](https://checkstyle.sourceforge.io/config_modifier.html#ModifierOrder)

modifier 순서를 검사.

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

### [RedundantModifier](https://checkstyle.sourceforge.io/config_modifier.html#RedundantModifier)

불필요한 modifier를 검사.

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

### [AbbreviationAsWordInName](https://checkstyle.sourceforge.io/config_naming.html#AbbreviationAsWordInName)

약어를 대문자로 표현했는지 검사.

```xml
<module name="AbbreviationAsWordInName">
    <property name="ignoreFinal" value="false"/>
    <property name="allowedAbbreviationLength" value="1"/>
    <property name="tokens"
              value="CLASS_DEF, INTERFACE_DEF, ENUM_DEF, ANNOTATION_DEF, ANNOTATION_FIELD_DEF,
                     PARAMETER_DEF, VARIABLE_DEF, METHOD_DEF"/>
</module>
```

VIOLATION
```java
int firstFOO;
int secondFOo;
```

OK
```java
int firstFoo;
int secondFoo;
String firstXML;    // abbreviation is allowed
String firstURL;    // abbreviation is allowed
```

### [CatchParameterName](https://checkstyle.sourceforge.io/config_naming.html#CatchParameterName)

catch 파라미터의 이름을 검사. `"^[a-z]([a-z0-9][a-zA-Z0-9]*)?$"` 패턴과 일치해야 한다.

```xml
<module name="CatchParameterName">
    <property name="format" value="^[a-z]([a-z0-9][a-zA-Z0-9]*)?$"/>
    <message key="name.invalidPattern"
             value="Catch parameter name ''{0}'' must match pattern ''{1}''."/>
</module>
```

VIOLATION
```java
try {
} catch (ArithmeticException Foo) {
} catch (ArrayIndexOutOfBoundsException BAR2) {
}
```

OK
```java
try {
} catch (ArithmeticException foo) {
} catch (ArrayIndexOutOfBoundsException bar2) {
}
```


### [ClassTypeParameterName](https://checkstyle.sourceforge.io/config_naming.html#ClassTypeParameterName)

클래스 제네릭 타입을 검사. `"(^[A-Z][0-9]?)$|([A-Z][a-zA-Z0-9]*[T]$)"` 패턴과 일치해야한다.

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

### [ConstantName](https://checkstyle.sourceforge.io/config_naming.html#ConstantName)

static final 변수 이름을 검사. `"^[A-Z][A-Z0-9]*(_[A-Z0-9]+)*$"` 패턴과 일치해야 한다.

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

### [InterfaceTypeParameterName](https://checkstyle.sourceforge.io/config_naming.html#InterfaceTypeParameterName)

interface 타입 이름을 검사. `"(^[A-Z][0-9]?)$|([A-Z][a-zA-Z0-9]*[T]$)"` 패턴과 일치해야 한다.

```xml
<module name="InterfaceTypeParameterName">
    <property name="format" value="(^[A-Z][0-9]?)$|([A-Z][a-zA-Z0-9]*[T]$)"/>
    <message key="name.invalidPattern"
             value="Interface type name ''{0}'' must match pattern ''{1}''."/>
</module>
```

VIOLATION
```java
interface Foo<t> { }
```

OK
```java
interface Foo<T> { }
```

### [LambdaParameterName](https://checkstyle.sourceforge.io/config_naming.html#LambdaParameterName)

람다의 파라미터 이름을 검사. `"^[a-z]([a-z0-9][a-zA-Z0-9]*)?$"` 패턴과 일치해야 한다.

```xml
<module name="LambdaParameterName">
    <property name="format" value="^[a-z]([a-z0-9][a-zA-Z0-9]*)?$"/>
    <message key="name.invalidPattern"
             value="Lambda parameter name ''{0}'' must match pattern ''{1}''."/>
</module>
```

VIOLATION
```java
Function<String, String> foo = Bar -> Bar.toLowerCase();
```

OK
```java
Function<String, String> foo = bar -> bar.toLowerCase();
```

### [LocalFinalVariableName](https://checkstyle.sourceforge.io/config_naming.html#LocalFinalVariableName)

지역 final 변수 이름을 검사. `"^[a-z][a-zA-Z0-9]*$"` 패턴과 일치해야한다.

```xml
<module name="LocalFinalVariableName">
    <property name="format" value="^[a-z]([a-z0-9][a-zA-Z0-9]*)?$"/>
        <message key="name.invalidPattern"
                 value="Local final variable name ''{0}'' must match pattern ''{1}''."/>
    </property>
</module>
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

### [LocalVariableName](https://checkstyle.sourceforge.io/config_naming.html#LocalVariableName)

지역 변수 이름을 검사. `"^[a-z]([a-z0-9][a-zA-Z0-9]*)?$"` 패턴과 일치해야한다.

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

### [MemberName](https://checkstyle.sourceforge.io/config_naming.html#MemberName)

클래스 멤버 이름을 검사. `"^[a-z][a-z0-9][a-zA-Z0-9]*$"` 패턴과 일치해야한다.

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

### [MethodName](https://checkstyle.sourceforge.io/config_naming.html#MethodName)

메소드 이름을 검사. `"^[a-z][a-z0-9][a-zA-Z0-9_]*$"` 패턴과 일치해야한다.

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

### [MethodTypeParameterName](https://checkstyle.sourceforge.io/config_naming.html#MethodTypeParameterName)

메소드 제네릭 타입 이름을 검사. `"(^[A-Z][0-9]?)$|([A-Z][a-zA-Z0-9]*[T]$)"` 패턴과 일치해야한다.

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

### [PackageName](https://checkstyle.sourceforge.io/config_naming.html#PackageName)

패키지 이름을 검사. `"^[a-z]+(\.[a-z][a-z0-9]*)*$"` 패턴과 일치해야한다.

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

### [ParameterName](https://checkstyle.sourceforge.io/config_naming.html#ParameterName)

파라미터 이름을 검사. `"^[a-z]([a-z0-9][a-zA-Z0-9]*)?$"` 패턴과 일치해야한다.

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

### [StaticVariableName](https://checkstyle.sourceforge.io/config_naming.html#StaticVariableName)

static 변수 이름을 검사. `"^[a-z][a-zA-Z0-9]*$"` 패턴과 일치해야한다.

```xml
<module name="StaticVariableName">
    <property name="format" value="^[a-z][a-z0-9][a-zA-Z0-9]*$"/>
    <message key="name.invalidPattern"
             value="Static variable name ''{0}'' must match pattern ''{1}''."/>
</module>
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

### [TypeName](https://checkstyle.sourceforge.io/config_naming.html#TypeName)

타입(class, interface, enum, annotation) 이름을 검사. `"^[A-Z][a-zA-Z0-9]*$"` 패턴과 일치해야한다.

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

### [Regexp](https://checkstyle.sourceforge.io/config_regexp.html#Regexp)

라인 뒤에 공백(' ') 혹은 탭('\t') 문자가 존재하는지 검사.

```xml
<module name="Regexp">
    <property name="format" value="[ \t]+$"/>
    <property name="illegalPattern" value="true"/>
    <property name="message" value="Trailing whitespace"/>
</module>
```


## [Size Violations](https://checkstyle.sourceforge.io/config_sizes.html)

### [FileLength](https://checkstyle.sourceforge.io/config_sizes.html#FileLength)

한 파일이 2500 라인을 초과했는지 검사.

```xml
<module name="FileLength">
    <property name="max" value="2500"/>
</module>
```

### [LineLength](https://checkstyle.sourceforge.io/config_sizes.html#LineLength)

한 라인에 100 캐릭터를 초과했는지 검사.

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

### [MethodLength](https://checkstyle.sourceforge.io/config_sizes.html#MethodLength)

메소드가 10000 라인을 초과했는지 검사.

```xml
<module name="MethodLength">
    <property name="max" value="10000"/>
</module>
```

### [ParameterNumber](https://checkstyle.sourceforge.io/config_sizes.html#ParameterNumber)

파라미터 개수가 10개를 초과했는지 검사.

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

### [EmptyForIteratorPad](https://checkstyle.sourceforge.io/config_whitespace.html#EmptyForIteratorPad)

for loop의 공백을 검사.

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

### [EmptyLineSeparator](https://checkstyle.sourceforge.io/config_whitespace.html#EmptyLineSeparator)

packge, import 등의 줄 바꿈을 검사.

```xml
<module name="EmptyLineSeparator">
    <property name="tokens"
              value="PACKAGE_DEF, IMPORT, STATIC_IMPORT, CLASS_DEF, INTERFACE_DEF, ENUM_DEF,
                     STATIC_INIT, INSTANCE_INIT, METHOD_DEF, CTOR_DEF, VARIABLE_DEF"/>
    <property name="allowNoEmptyLineBetweenFields" value="true"/>
</module>
```

VIOLATION
```java
package foo.bar.baz;
import foo.bar.baz.Qux;

public class Foo {
    public static void main(String[] args) {
    }
    public static void bar() {
    }
}
```

OK
```java
package foo.bar.baz;

import foo.bar.baz.Qux;

public class Foo {
    public static void main(String[] args) {
    }

    public static void bar() {
    }
}
```

### [FileTabCharacter](https://checkstyle.sourceforge.io/config_whitespace.html#FileTabCharacter)

탭('\t') 문자가 존재하는지 검사.

```xml
<module name="FileTabCharacter">
    <property name="eachLine" value="true"/>
</module>
```

### [GenericWhiteSpace](https://checkstyle.sourceforge.io/config_whitespace.html#GenericWhitespace)

제네릭의 공백 규칙을 검사.

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

### [MethodParamPad](https://checkstyle.sourceforge.io/config_whitespace.html#MethodParamPad)

메소드와 파라미터 사이의 공백을 검사.

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

### [NoLineWrap](https://checkstyle.sourceforge.io/config_whitespace.html#NoLineWrap)

import의 줄바꿈을 검사.

```xml
<module name="NoLineWrap">
    <property name="tokens" value="PACKAGE_DEF, IMPORT, STATIC_IMPORT"/>
</module>
```

VIOLATION
```java
package foo.bar.
        baz.qux;
import foo.bar.
        baz.Qux;
import static foo.bar.
        Baz.QUX;
```

OK
```java
package foo.bar.baz.qux;
import foo.bar.baz.Qux;
import static foo.bar.Baz.QUX;
```


### [NoWhitespaceAfter](https://checkstyle.sourceforge.io/config_whitespace.html#NoWhitespaceAfter)

토큰 뒤의 공백을 검사.

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

### [NoWhitespaceBefore](https://checkstyle.sourceforge.io/config_whitespace.html#NoWhitespaceBefore)

토큰 앞의 공백을 검사.

```xml
<module name="NoWhitespaceBefore"/>
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

### [OperatorWrap](https://checkstyle.sourceforge.io/config_whitespace.html#OperatorWrap)

연산자의 줄바꿈을 검사.

```xml
<module name="OperatorWrap">
    <property name="option" value="NL"/>
    <property name="tokens"
              value="BAND, BOR, BSR, BXOR, DIV, EQUAL, GE, GT, LAND, LE, LITERAL_INSTANCEOF,   
                     LOR, LT, MINUS, MOD, NOT_EQUAL, PLUS, QUESTION, SL, SR, STAR, METHOD_REF"/>
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
        
### [ParenPad](https://checkstyle.sourceforge.io/config_whitespace.html#ParenPad)

괄호 사이의 공백을 검사.

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

### [SeparatorWrap](https://checkstyle.sourceforge.io/config_whitespace.html#SeparatorWrap)

dot('.')이 개행문자 뒤에 존재하는지 검사.

```xml
<module name="SeparatorWrap">
    <property name="id" value="SeparatorWrapDot"/>
    <property name="tokens" value="DOT"/>
    <property name="option" value="nl"/>
</module>
```

VIOLATION
```java
new Foo().
    bar(null).
    baz();
```

OK
```java
new Foo()
    .bar(null)
    .baz();
```

comma가 개행문자 앞에 존재하는지 검사.

```xml
<module name="SeparatorWrap">
    <property name="id" value="SeparatorWrapComma"/>
    <property name="tokens" value="COMMA"/>
    <property name="option" value="EOL"/>
</module>
```

VIOLATION
```java
System.out.printf(
    "%d %d %d"
    ,1
    ,2
    ,3
);
```

OK
```java
System.out.printf(
    "%d %d %d",
    1,
    2,
    3
);
```

ellipsis('...')가 개행문자 앞에 존재하는지 검사.

```xml
<module name="SeparatorWrap">
    <property name="id" value="SeparatorWrapEllipsis"/>
    <property name="tokens" value="ELLIPSIS"/>
    <property name="option" value="EOL"/>
</module>
```

VIOLATION
```java
public static void printf(
    String
        arg1,
    Object
        ...arg2) { }
```

OK
```java
public static void printf(
    String
        arg1,
    Object...
        arg2) { }
```

배열 선언 문자('[', ']')가 개행문자 앞에 존재하는지 검사.

```xml
<module name="SeparatorWrap">
    <property name="id" value="SeparatorWrapArrayDeclarator"/>
    <property name="tokens" value="ARRAY_DECLARATOR"/>
    <property name="option" value="EOL"/>
</module>
```

VIOLATION
```java
int
    []array;
```

OK
```java
int[]
    array;
```

메소드 참조('::') 문자가 개행문자 뒤에 존재하는지 검사.

```xml
<module name="SeparatorWrap">
    <property name="id" value="SeparatorWrapMethodRef"/>
    <property name="tokens" value="METHOD_REF"/>
    <property name="option" value="nl"/>
</module>
```

VIOLATION
```java
Arrays.sort(stringArray, String::
    compareToIgnoreCase);
```

OK
```java
Arrays.sort(stringArray, String
    ::compareToIgnoreCase);
```

### [TypecastParenPad](https://checkstyle.sourceforge.io/config_whitespace.html#TypecastParenPad)

타입 변환 괄호 사이의 공백을 검사.

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

### [WhitespaceAfter](https://checkstyle.sourceforge.io/config_whitespace.html#WhitespaceAfter)

comma(','), semi-colon(';') 뒤의 공백을 검사.

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

### [WhitespaceAround](https://checkstyle.sourceforge.io/config_whitespace.html#WhitespaceAround)

token 사이에 공백이 존재하는지 검사.

```xml
<module name="WhitespaceAround">
    <property name="allowEmptyConstructors" value="true"/>
    <property name="allowEmptyLambdas" value="true"/>
    <property name="allowEmptyMethods" value="false"/>
    <property name="allowEmptyTypes" value="true"/>
    <property name="allowEmptyLoops" value="true"/>
    <property name="tokens"
              value="ASSIGN, BAND, BAND_ASSIGN, BOR, BOR_ASSIGN, BSR, BSR_ASSIGN, 
                     BXOR, BXOR_ASSIGN, COLON, DIV, DIV_ASSIGN, DO_WHILE, EQUAL, 
                     GE, GT, LAMBDA, LAND,LCURLY, LE, LITERAL_CATCH, LITERAL_DO, 
                     LITERAL_ELSE, LITERAL_FINALLY,LITERAL_FOR, LITERAL_IF, 
                     LITERAL_RETURN, LITERAL_SWITCH, LITERAL_SYNCHRONIZED,
                     LITERAL_TRY, LITERAL_WHILE, LOR, LT, MINUS, MINUS_ASSIGN, 
                     MOD, MOD_ASSIGN, NOT_EQUAL, PLUS, PLUS_ASSIGN, QUESTION, 
                     RCURLY, SL, SLIST, SL_ASSIGN, SR, SR_ASSIGN, STAR, 
                     STAR_ASSIGN, LITERAL_ASSERT, TYPE_EXTENSION_AND"/>
    <message key="ws.notFollowed"
             value="WhitespaceAround: ''{0}'' is not followed by whitespace. Empty blocks may only be represented as '{}' when not part of a multi-block statement (4.1.3)"/>
    <message key="ws.notPreceded"
             value="WhitespaceAround: ''{0}'' is not preceded with whitespace."/>
</module>
```

VIOLATION
```java
boolean result = foo==bar;     // '==' must preceded and followed whitespace

while(true) {}                // 'while' must followed by whitespace

if(foo == bar) { }            // 'if' is not followed by whitespace

System.out.println(foo+bar);  // '+' must preceded and followed whitespace

synchronized(this) {}         // 'synchronized' must followed by whitespace
```

OK
```java
boolean result = foo == bar;

while (true) {}

if (foo == bar) { }

System.out.println(foo + bar);

synchronized (this) {}
```
