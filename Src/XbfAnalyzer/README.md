# XbfAnalyzer
XbfAnalyzer analyzes and displays information about XBF (XAML Binary Format) files.
It includes a node parser that works with the new XBF v2.1 format introduced with Windows 10.

This program is intended to be used for research purposes.
The XAML node structure it displays may not completely match the actual file content.

XbfAnalyzer cannot currently parse all XBF files as some features are not yet supported.
The node parser was derived entirely from analyzing generated XBF files, so there may be some mistakes, inaccuracies, etc.

## Using XbfAnalyzer
XbfAnalyzer is built as a simple WPF application.
To use it, drag and drop one or more XBF files into the main window.

## Notes
XbfAnalyzer will not display any node structure information for XBF v1 files since the included node parser only works with v2 files.
There are other projects that work with v1 files, including [XbfDump](https://github.com/WalkingCat/XbfDump) and [XbfDecompiler](https://github.com/TeamGnome/XbfDecompiler).

XBF v2 files have a completely different node stream format than v1 files.
Unlike v1, XBF v2 files do not include the names and properties of standard controls (e.g., Grid, Button, TextBlock, etc.) in the header.
Instead, these controls and their properties appear to have unique, hardcoded ID numbers.

Special thanks to [Christoph Hausner](https://github.com/chausner) for discovering the complete type, property, and enumeration mappings in GenXbf.dll from the Windows 10 Anniversary Update SDK.
