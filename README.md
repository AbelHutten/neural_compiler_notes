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
[LEGO: A Layout Expression Language for Code
Generation of Hierarchical Mapping](https://users.cs.utah.edu/~tavak/assets/pdf/LEGO-CGO26.pdf)
\
https://github.com/tavakkoliamirmohammad/LEGO

\
[LEGO-Compiler: Enhancing Neural Compilation
Through Translation Composability](https://arxiv.org/pdf/2505.20356)

## Notes
Everything that ignores the [Bitter Lesson](http://www.incompleteideas.net/IncIdeas/BitterLesson.html) will eventually be the bottleneck. Manually writing compilers does not scale with data or compute. The ability to compile tensor programs to arbitrary architectures is of fundamental importance. Compilers need to generate machine code that is correct and efficient. An ML approach to compilation needs to produce correct machine code, be able to produce more efficient code when given more data and or compute, and be capable of targeting arbitrary architectures.

Maybe a code world model can learn fundamental underlying properties of hardware that allow it to understand unseen architectures.

Using LLMs seems possibly not optimal. Maybe JEPA style SSL is better?

Would it be possible to have an invertible architecture so that a copiler gives a free decompiler? Probably not

Ultimate goal would be a model that can convert any program in any programming language, including machine language, to any other language on any architecture. We must start with a much smaller scope. We should map a course where each step brings us closer to the goal while delivering useful intermediaries.

We will start by learning compilers between languages for which correct compilers already exist. In order to overcome hand-crafted compilers, the neural compiler must eventually be capable of compiling machine code for architectures that do not have any compiler support.

## Datasets
[ExeBench](https://huggingface.co/datasets/jordiae/exebench)

## Benchmarks

