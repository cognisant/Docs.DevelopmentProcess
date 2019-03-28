# C# Code Styles

For C# projects we will abide to the rules enforced by [StyleCop Analyzers](https://github.com/DotNetAnalyzers/StyleCopAnalyzers) to ensure consistent formatting, and ensure well documented code.

## Changes

A small number of tweaks have been decided on from the core rules as defined, these are to account for existing preferences that have been used.

- `SA1101` disabled, `SA1101X` enabled: Team preference is to not prefix local class variables with `this`.
- `SA1309` disabled, `SX1309` and `SX1390S` enabled: Team preferences is for `private` fields to be prefixed with an underscore(`_`).
- `SA1602` disabled: Team preference is to not document items within enumerations.

## Cognisant CodeStyle.CSharp NuGet Packages

Two [Nuget](https://www.nuget.org) packages have been created to automatically set up the StyleCop Analyzers packages according to the above discussed preferences, along with a `stylecop.json` file to set any required preferences.

[CR.CodeStyle.CSharp.Full](https://www.nuget.org/packages/CR.CodeStyle.CSharp.Full/) is used for new projects and includes the default StyleCop Analyzers set up, with the changes noted above.

[CR.CodeStyle.CSharp.CodeOnly](https://www.nuget.org/packages/CR.CodeStyle.CSharp.CodeOnly/) is used for existing projects where we want to ensure consistent formatting, but avoid the task of documenting a large existing code base. It differs from the full package by disabling all documentation related rules (mostly `SA16XX`), along with the other changes noted above.
