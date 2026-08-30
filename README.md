[![](https://img.shields.io/nuget/v/soenneker.lucide.enums.icons.svg?style=for-the-badge)](https://www.nuget.org/packages/soenneker.lucide.enums.icons/)
[![](https://img.shields.io/github/actions/workflow/status/soenneker/soenneker.lucide.enums.icons/build-and-test.yml?style=for-the-badge)](https://github.com/soenneker/soenneker.lucide.enums.icons/actions/workflows/build-and-test.yml)
[![](https://img.shields.io/github/actions/workflow/status/soenneker/soenneker.lucide.enums.icons/publish-package.yml?style=for-the-badge)](https://github.com/soenneker/soenneker.lucide.enums.icons/actions/workflows/publish-package.yml)
[![](https://img.shields.io/nuget/dt/soenneker.lucide.enums.icons.svg?style=for-the-badge)](https://www.nuget.org/packages/soenneker.lucide.enums.icons/)
[![](https://img.shields.io/github/actions/workflow/status/soenneker/soenneker.lucide.enums.icons/codeql.yml?label=CodeQL&style=for-the-badge)](https://github.com/soenneker/soenneker.lucide.enums.icons/actions/workflows/codeql.yml)

# Soenneker.Lucide.Enums.Icons

A generated `LucideIcon` enum for selecting Lucide icons without string literals.

## Install

```bash
dotnet add package Soenneker.Lucide.Enums.Icons
```

## Usage

```csharp
using Soenneker.Lucide.Enums.Icons;

LucideIcon icon = LucideIcon.CircleCheck;

string label = icon switch
{
    LucideIcon.CircleCheck => "Complete",
    LucideIcon.CircleX => "Failed",
    _ => "Unknown"
};
```

This package contains identifiers only; it does not include SVG markup or render icons. Use `Soenneker.Lucide.Icons` when the SVG data is also required.

The enum is regenerated as the upstream icon set changes. Persist enum names rather than their numeric values, because member ordering is not a storage contract. Consumers should also tolerate newly added names and the removal or renaming of upstream icons.
