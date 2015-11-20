# "Inventory of Epics" for the Roslyn Analyzer Ecosystem

Here is a current list of the major areas of work ("epics") for the Roslyn analyzer ecosystem. See the [README](https://github.com/dotnet/roslyn-analyzers-contrib/blob/master/README.md) for an explanation of what that means.

1. Replace FxCop

    Replace FxCop with a collection of Roslyn-based analyzers and fixers. We will take the opportunity to remove FxCop rules that are no longer relevant, and to add new rules around new language features.

2. Provide style analyers in VS

    Create a comprehensive, configurable set of Roslyn-based style analyzers and fixers. These will draw on the work of @sharwell and the team over at [DotNetAnalyzers/StyleCopAnalyzers](https://github.com/DotNetAnalyzers/StyleCopAnalyzers).

3. Implement a configuration mechanism for Roslyn analyzers and fixers

    This is especially important for style analyzers, because different projects have different "house styles".

4. Improve the analyzer project templates

5. Improve the test infrastructure

    Today, when you create a new analyzer project in Visual Studio, you get a test project that includes boilerplate code for setting up a test and verifying the result. We should consider whether to factor out this test infrastructure into its own project or repo, where we could then make it more configurable and capable. As matters stand, even if Microsoft were to improve the test infrastructure in the project template, existing analyzer projects would not benefit.

    Also in the test infrastructure category, we should consider creating a repo with a large set of code samples, both correct and incorrect, over which developers could run their analyzers.

6. Telemetry, feedback, ratings

    Can we provide a mechanism for analyzers to provide telemetry to their authors? What about a web site that used analyzer telemetry to provide user feedback and ratings, and offer suggestions for the most popular or highest quality analyzer packages, perhaps broken down by category (style, correctness, security, API design, etc.). 
