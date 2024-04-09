# How do Programmers Bypass Compiler Bugs?
---

## Project summary
Compilers are essential in daily development, but their bugs can introduce hidden bugs to many software projects. As compiler bugs are important, researchers have conducted various empirical studies to understand their characteristics. Most of the prior studies analyze only the bug reports and patches of compilers. From such sources, they analyze the root causes, locations, and repairs of compiler bugs. Their findings are useful for understanding compiler bugs themselves, but to the best of our knowledge, the impact of compiler bugs is rarely explored. For example, before compiler bugs are fixed, programmers would bypass such bugs, but no prior study analyzes the workarounds for compiler bugs.

To complement the prior studies, in this paper, we analyze how the bugs of two mainstream compilers, gcc and llvm, affect real development. Besides the bug reports and patches of compilers, in this study, from 632 Github projects, we collect 806 commits whose messages mention compiler bugs. From the dataset, we analyzes how compiler bugs affect real projects. Furthermore, we manually analyze 219 commits whose messages explicitly mention compiler bugs. Our results lead to eight findings that are useful for programmers, compiler developers, and researchers. For example, we find that programmers often modify programs or build files to bypass compiler bugs. When they modify build files, they often introduce technical debts, and such workaround should be removed after compiler bugs are fixed.
---
## Dataset
We collect 2,989 bug reports from 1,355 Github projects, and manually inspected 219 commits whose messages explicitly mention the urls of compiler bug reports. For details, see [all_bugs.txt] for the whole set; [association.txt] for manully inspected result of selected bugs.
