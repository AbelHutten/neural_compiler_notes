# Neural Compiler Notes
WIP. PRs welcome

## Resources
[Neural Compilation and Decompilation with
Conditional Language Models (PhD Thesis)](https://era.ed.ac.uk/server/api/core/bitstreams/fef7e74d-32ef-4f4c-85d8-1b370baf92b3/content) 

\
[Learning C to x86 Translation: An Experiment in
Neural Compilation](https://arxiv.org/pdf/2108.07639)
\
https://github.com/jordiae/neural-compilers
\
[SLaDe: A Portable Small Language Model
Decompiler for Optimized Assembly](https://arxiv.org/pdf/2305.12520)
\
https://zenodo.org/records/10205121
\
[Forklift: An Extensible Neural Lifter](https://arxiv.org/abs/2404.16041)
\
https://github.com/jordiae/forklift

\
[LEGO: A Layout Expression Language for Code
Generation of Hierarchical Mapping](https://users.cs.utah.edu/~tavak/assets/pdf/LEGO-CGO26.pdf)
\
https://github.com/tavakkoliamirmohammad/LEGO

\
[LEGO-Compiler: Enhancing Neural Compilation
Through Translation Composability](https://arxiv.org/pdf/2505.20356)

### Learning algorithms that execute exactly

- [Discrete Neural Algorithmic Reasoning — ICML 2025](https://proceedings.mlr.press/v267/rodionov25a.html) · [Code](https://github.com/yandex-research/dnar)
- [Synthesis and Verification of Transformer Programs — IJCAI 2026](https://ijcai.org/proceedings/2026/434)
- [Learning to Add, Multiply, and Execute Algorithmic Instructions Exactly with Neural Networks — NeurIPS 2025](https://proceedings.nips.cc/paper_files/paper/2025/hash/71553eb7d97b9c332d9c520c5de724d9-Abstract-Conference.html)
- [Looped Transformers for Length Generalization — ICLR 2025](https://arxiv.org/abs/2409.15647) · [Code](https://github.com/UW-Madison-Lee-Lab/looped-tf)
- [Universal Length Generalization with Turing Programs — ICML 2025](https://proceedings.mlr.press/v267/hou25a.html)

### Compilation and compiler components

- [LLM-VeriOpt — CGO 2026](https://samainsworth.github.io/LLM-VeriOpt-CGO2026.pdf)
- [Synthesizing Instruction Selection Back-Ends from ISA Specifications Made Practical — CGO 2026](https://aengelke.net/pubs/2602-cgo2.pdf)
- [QiMeng-Xpiler — OSDI 2025](https://www.usenix.org/conference/osdi25/presentation/dong) · [Code](https://github.com/QiMeng-IPRC/QiMeng-Xpiler)
- [LEGO-Compiler — 2025 preprint, April 2026 journal publication](https://link.springer.com/article/10.1007/s42514-025-00272-9)
- [QiMeng-NeuComBack — NeurIPS 2025](https://arxiv.org/abs/2511.01183)
- [SuperCoder — revised August 2026](https://arxiv.org/abs/2505.11480v4) · [Code](https://github.com/Anjiang-Wei/SuperCoder)

## Notes
Everything that ignores the [Bitter Lesson](http://www.incompleteideas.net/IncIdeas/BitterLesson.html) will eventually be the bottleneck. Manually writing compilers does not scale with data or compute. The ability to compile tensor programs to arbitrary architectures is of fundamental importance. Compilers need to generate machine code that is correct and efficient. An ML approach to compilation needs to produce correct machine code, be able to produce more efficient code when given more data and or compute, and be capable of targeting arbitrary architectures.

Maybe a code world model can learn fundamental underlying properties of hardware that allow it to understand unseen architectures.

Using LLMs seems possibly not optimal. Maybe JEPA style SSL is better?

Would it be possible to have an invertible architecture so that a copiler gives a free decompiler? Probably not

Ultimate goal would be a model that can convert any program in any programming language, including machine language, to any other language on any architecture. We must start with a much smaller scope. We should map a course where each step brings us closer to the goal while delivering useful intermediaries.

We will start by learning compilers between languages for which correct compilers already exist. In order to overcome hand-crafted compilers, the neural compiler must eventually be capable of compiling machine code for architectures that do not have any compiler support.

CSmith can generate random C programs.

https://github.com/facebookresearch/compilergym

Public Git archive: a big code dataset for all

## Datasets
[ExeBench](https://huggingface.co/datasets/jordiae/exebench)

## Benchmarks
