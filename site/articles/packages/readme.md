---
title: "Packages"
---

# Packages

This section gives package-by-package coverage for every shippable library NuGet in the repository.

Packaged tools such as `Svg.Skia.Converter` and `svgc` stay documented under [Samples and Tools](../reference/samples-and-tools).

## Runtime packages

| Package | Start here when | Guide |
| --- | --- | --- |
| `Svg.Skia` | You want the main SkiaSharp runtime renderer, export helpers, hit testing, or Android VectorDrawable support. | [Svg.Skia](svg-skia) |
| `Svg.Model` | You need the intermediate drawable and picture model for inspection, mutation, or custom pipelines. | [Svg.Model](svg-model) |
| `Svg.Custom` | You want the underlying SVG DOM and parser that the renderer consumes. | [Svg.Custom](svg-custom) |
| `ShimSkiaSharp` | You need a cloneable command-model equivalent of key SkiaSharp drawing primitives. | [ShimSkiaSharp](shim-skiasharp) |

## Avalonia UI packages

| Package | Start here when | Guide |
| --- | --- | --- |
| `Svg.Controls.Skia.Avalonia` | You want the richest Avalonia SVG integration, backed by `Svg.Skia` and real `SkiaSharp.SKPicture` output. | [Svg.Controls.Skia.Avalonia](svg-controls-skia-avalonia) |
| `Svg.Controls.Avalonia` | You want the same high-level Avalonia SVG concepts but rendered through the Avalonia drawing stack. | [Svg.Controls.Avalonia](svg-controls-avalonia) |
| `Skia.Controls.Avalonia` | You want reusable Avalonia controls and `IImage` wrappers for raw SkiaSharp content, with or without SVG. | [Skia.Controls.Avalonia](skia-controls-avalonia) |

## Generated-code packages

| Package | Start here when | Guide |
| --- | --- | --- |
| `Svg.CodeGen.Skia` | You want to turn the intermediate picture model into checked-in or pipeline-generated C# code. | [Svg.CodeGen.Skia](svg-codegen-skia) |
| `Svg.SourceGenerator.Skia` | You want `.svg` assets turned into generated `Picture` classes during the build. | [Svg.SourceGenerator.Skia](svg-sourcegenerator-skia) |

## Choosing quickly

- Choose `Svg.Skia` for direct runtime rendering and export.
- Choose `Svg.Controls.Skia.Avalonia` for interactive Avalonia usage on the Skia-backed path.
- Choose `Svg.Controls.Avalonia` for Avalonia drawing-context integration without the `SKSvg` runtime surface.
- Choose `Svg.Model` and `ShimSkiaSharp` when the main task is inspection, transformation, or code generation rather than direct display.
- Choose `Svg.CodeGen.Skia` or `Svg.SourceGenerator.Skia` when startup cost should move from runtime to build time.
