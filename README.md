# TideTimes

A native iOS app for viewing tide times, built with SwiftUI.

## Requirements

- Xcode 16+
- iOS 18.0+

## Getting Started

1. Clone the repository
2. Open `TideTimes.xcodeproj` in Xcode
3. Select a simulator or connected device and press Cmd+R to run

## Building & Testing

```bash
# Build
xcodebuild build -project TideTimes.xcodeproj -scheme TideTimes -destination 'platform=iOS Simulator,name=iPhone 16'

# Test
xcodebuild test -project TideTimes.xcodeproj -scheme TideTimes -destination 'platform=iOS Simulator,name=iPhone 16'
```

## CI

GitHub Actions automatically builds and runs tests on every push and pull request to `main`.
