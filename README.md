# Swift QR Code Generator

[![Swift 6.1](https://img.shields.io/badge/Swift-6.1-orange.svg)](https://swift.org)
[![macOS](https://github.com/kicsipixel/swift-qrcode-generator/actions/workflows/darwin.yml/badge.svg)](https://github.com/kicsipixel/swift-qrcode-generator/actions/workflows/darwin.yml)
[![Linux](https://github.com/kicsipixel/swift-qrcode-generator/actions/workflows/linux.yml/badge.svg)](https://github.com/kicsipixel/swift-qrcode-generator/actions/workflows/linux.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A QR code generator written in pure Swift with no dependencies.

The project is mostly a direct translation of [Nayuki's](https://github.com/nayuki/) [QR code generator for Rust](https://github.com/nayuki/QR-Code-generator/tree/master/rust), with small changes applied to make the code more idiomatic in Swift.

## Usage

### Swift Package Manager
To use in your project, add the following dependency to your `Package.swift`:

```swift
.package(url: "https://github.com/kicsipixel/swift-qrcode-generator.git", from: "2.0.3")
```

## Example
```swift
import QRCodeGenerator

let url = "https://hummingbird.codes/"
let qr = try! QRCode.encode(text:url, ecl: .medium)
let svg = qr.toSVGString(border: 4)
```
