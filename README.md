# Commit-Messaging System

A symbolic-shorthand to detail the changes in a version-control commit.

The CMS defines 'indications' for symbols, with a commit-message begining with one or more of these symbols. The enumeration of the symbol defines the domain of its indication:

Enumeration | Domain 
-|-
1st | Content
2nd | Functionality

The pair of symbols is expected to be sufficiently expressive, such that the message only needs to specify the object of the symbols' indication. 

```
 ____ Content symbol
v
== Message...
 ^___ Functionality symbol (optional)
```

## Symbols

Symbol | Indication
-|-
=| Static (no change) (this is the fallback indication)
*| Modification
+| Addition
~| Removal
]| Formatting
!| Breaking
^| Fix
v| Revert
%| Split
@| Rename
$| Optimisation

Obviously the Modification indication is the least specific and other indications provide better specification.

### Special CMS pairs

CMS Symbol | indication
---|-
#^ | Submodule update
\><| Merge commit

## Common CMS pairs

These are not strict definitions for CMS Symbols, nor is it an exhaustive list. Rather these are exemplary indications/interpretations.

CMS Symbol | Indication
---|-
]  | Reformatted code
*] | Modified UI presentation/layout
^  | Fixed typo
^^ | Fixed critical typo
@^ | Renamed something to fix functionality
*^ | Fixed functionality
%  | Split function/code/file
~% | Split functionality (into a separate repository/project)
*% | Split functionality (into a different mode/page/condition)
@  | Renamed something (class/function/variable/file...)
\+ | Added content (typically comments)
++ | Added functionality
~+ | Added functionality (by removing a restrictive condition perhaps)
*+ | Added functionality (by modifying a restrictive condition perhaps)
+! | Added content, breaking functionality (Work In Progress)
~! | Removed content, breaking functionality
v^ | Reverted content, fixing functionality
