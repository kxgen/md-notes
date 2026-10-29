Common traits of high-quality code include:

- **Readability:** Can another team member easily understand your code? Can another programmer, working years from now, accurately interpret your code without you being around to provide context?

- **Maintainability:** Is it robust enough to add new features without breaking core functionality, or is it too brittle to adjust without requiring major refactoring? Prioritizing maintainable code might entail additional upfront hassle, but saves significant time and energy moving forward.

- **Efficiency:** Well-written code can reduce a system’s latency and resource consumption. For instance, carefully chosen data structures can minimize the number of [CPU operations](https://www.ibm.com/think/topics/central-processing-unit) required for a given function. Thoughtful [data caching strategies](https://www.ibm.com/think/topics/database-optimization) cut down on costly input/out (I/O) operations by eliminating redundant database queries and network requests, while promptly releasing unused memory avoids unnecessary RAM bloat.

Writing in _Harvard Data Science Review_ in 2023, researchers from Calvin University, Amherst College and Columbia proposed a prescriptive framework for good code:

**“The Four C’s.”**

- **Correctness:** The code does what it’s supposed to do. The authors emphasized two corollaries of this obvious inclusion: “First, correctness is a necessary but insufficient metric for good code. Second, the other goals support and promote correctness.”

- **Clarity:** Anyone reading and writing the code can tell what it’s intended to do and intuitively make modifications as necessary.

- **Containment:** Avoid sprawl, redundancy and unnecessary dependencies. Proper containment entails, among other things, “using functions to contain reusable code, and keeping code used across files or projects in a module or package.”

- **Consistency:** A codebase should maintain internal consistency of style, naming conventions, commentary, indentation and other practices.

##### Choosing Good Names

- _Use capitalization consistently_. It’s also wise to avoid instances in which two names are differentiated solely by their capitalization.

- _Keep a digest of abbreviations_. Short or even single-character variable names can help declutter code, but they can also become inscrutable to people less familiar with the project. Maintaining a “glossary” of sorts mitigates that trade-off.

### Select a coherent and minimal (but adequate) toolkit

Leveraging toolkits and libraries is a natural boon for code reusability and efficiency, helping to standardize workflows and outputs across different teams and broadly accelerate code creation. They’re particularly useful when code must mediate interactions with complex third-party systems or handle repetitive, “solved” problems.

But over-reliance on toolkits can add unnecessary bloat and introduce external dependencies, reducing code’s robustness and maintainability. They also have a tendency to abstract away the code’s underlying logic, decreasing its readability. The _HDSR_ authors articulate the ideal balance in simple terms: “We want our toolkit to be as simple as possible, but no simpler.”


Fowler and Beck’s list of code smells to be wary of includes examples such as:

- **Long function (long method):** A method containing too many lines of code.

- **Large class:** A class trying to do too much and containing too many variables, lacking cohesion.

- **Primitive obsession:** Using primitive data types instead of specialized small objects.

- **Mysterious name:** Functions or variables named poorly, hiding their actual intent.

- **Data clumps:** Groups of variables that frequently appear together everywhere.

- **Lazy elements:** Classes or functions that do too little to exist.

- **Long parameter list:** Functions requiring too many arguments to operate correctly.

- **Shotgun surgery:** One change requires modifying many scattered modules simultaneously (which is essentially the opposite of large class).

- **Duplicated code:** Identical or very similar code structures in multiple places.