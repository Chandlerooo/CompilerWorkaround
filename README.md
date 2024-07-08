# How do Programmers Bypass Compiler Bugs?
## Project summary
Compilers are essential in daily development, but their bugs can introduce hidden bugs to many software projects. As compiler bugs are important, researchers have conducted various empirical studies to understand their characteristics. Most of the prior studies analyze only bug reports and patches of compilers. From such sources, they analyze the root causes, locations, and repairs of compiler bugs. Their findings are useful for understanding compiler bugs themselves, but to the best of our knowledge, the impact of compiler bugs is rarely explored. For example, before compiler bugs are fixed, programmers would bypass such bugs, but no prior study analyzes the workarounds for compiler bugs.

To complement the prior studies, we analyze how the bugs of two mainstream compilers, gcc and llvm, affect real development. Besides the bug reports and patches of compilers, in this study, from 632 Github projects, we collect 806 commits whose messages mention compiler bugs. From the dataset, we analyze how compiler bugs affect real projects. Furthermore, we manually analyze 219 commits whose messages explicitly mention compiler bugs. Our results lead to eight findings that are useful for programmers, compiler developers, and researchers. For example, we find that programmers often modify programs or build files to bypass compiler bugs. When they modify build files, they often introduce technical debts, and such workaround should be removed after compiler bugs are fixed.
## Dataset
We collect 806 bug reports from 603 Github projects and manually inspected 219 commits whose messages explicitly mention the urls of compiler bug reports. For details, see [all_bugs.xlsx](https://github.com/Chandlerooo/CompilerWorkaround/blob/main/all_bugs.xlsx) for the whole set; [association.xlsx](https://github.com/Chandlerooo/CompilerWorkaround/blob/main/association.xlsx) for manually inspected result of selected bugs.
## Example
We provide a list of commits and bug reports used as examples in our paper for easy access.
<!-- Anchor for Table -->
| Project | Symptom | Workaround | Commit URL | Bugreport URL |
|---------|---------|------------|------------|---------------|
| Oblas   | rejects-valid | implementing methods | [d87584](https://github.com/sleepybishop/oblas/commit/d8758407869a6b0a2051c60509734220707a9ae6) | [Gcc91341](https://gcc.gnu.org/bugzilla/show_bug.cgi?id=91341) |
