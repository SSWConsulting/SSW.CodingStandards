---
date: 2019-03-26T08:47:11+01:00
draft: false
id: 'ssw88'
title: 'Avoid generic Exceptions'
ruleUrl: 'http://www.ssw.com.au/ssw/CodeAuditor/'
ruleType: Regex
fileFilter: '*.cs'
shouldExists: false
isError: false
searchIn: 'content'
regex: "catch\\s*\\(\\s*Exception\\s*"
---

## Rule Details

You should avoid catching generic exception, instead let it bubble up.

Examples of **incorrect** code for this rule:

```csharp
try {
    doSomething();
} catch(Exception ex) {
    // some logic
}
```

Examples of **correct** code for this rule:

```csharp
try {
    doSomething();
} catch(IOException ex) {
    // some logic
}
```
