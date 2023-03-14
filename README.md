# Swift Test Report

Generates an MD file from Swift XCTests and show it in the workflow summary. Uses [`Testify `](https://github.com/BinaryBirds/Testify) library to generat MD file.

## Usage

Include the action in your workflow (make sure that a Swift 5.6+ toolchain is on your PATH, on macOS this should be given, but on Linux you may need to first install it e.g. using [`setup-swift`](https://github.com/fwal/setup-swift)):

```yaml
- uses: BinaryBirds/swift-test-report@0.0.1
```
Full example:

```yaml
on: [push]

jobs:
  generate_report:
    runs-on: macos-latest
    name: Generate MD report
    steps:
      - uses: actions/checkout@v3
      - uses: BinaryBirds/swift-test-report@0.0.1
```

