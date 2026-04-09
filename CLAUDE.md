# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

TideTimes is a native iOS app built with SwiftUI, targeting iOS 18.0+. It is in early development — currently a minimal template ready for feature implementation.

## Build & Test Commands

This is a pure Xcode project (no Package.swift). Build and test via `xcodebuild`:

```bash
xcodebuild build -project TideTimes.xcodeproj -scheme TideTimes -destination 'platform=iOS Simulator,name=iPhone 16'
xcodebuild test -project TideTimes.xcodeproj -scheme TideTimes -destination 'platform=iOS Simulator,name=iPhone 16'
```

For local development, open `TideTimes.xcodeproj` in Xcode and use Cmd+R to run or Cmd+U to test.

## Architecture

- **Entry point**: [TideTimes/TideTimesApp.swift](TideTimes/TideTimesApp.swift) — `@main` SwiftUI app using `WindowGroup`
- **Main view**: [TideTimes/ContentView.swift](TideTimes/ContentView.swift) — currently template placeholder
- **Unit tests**: [TideTimesTests/TideTimesTests.swift](TideTimesTests/TideTimesTests.swift) — uses Swift Testing framework (`import Testing`, `@Test` attribute)
- **UI tests**: [TideTimesUITests/](TideTimesUITests/) — uses XCTest

The app uses SwiftUI throughout with no third-party dependencies.

## CI/CD

GitHub Actions ([.github/workflows/swift.yml](.github/workflows/swift.yml)) runs on `macos-latest` and triggers on push/PR to `main`, executing `swift build -v` and `swift test -v`.
