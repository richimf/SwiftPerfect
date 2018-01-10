# hello-perfect

### PROJECT CREATION AND BASIC CONFIGURATION ###
This project has been created with this command line:
> swift package init --type executable

Generate xcode project command line:
> swift package generate-xcodeproj

Open project via terminal:
> open ./hello-perfect.xcodeproj/

Select Target: hello-perfect and Build & Run.
<br></br>
Add the following dependency inside Package.swift:
> .package(url:"https://github.com/PerfectlySoft/Perfect-HTTPServer.git", from: "3.0.0")

Code should look like this:
```Swift
import PackageDescription

let package = Package(
    name: "hello-perfect",
    dependencies: [
        // Dependencies declare other packages that this package depends on.
        .package(url:"https://github.com/PerfectlySoft/Perfect-HTTPServer.git", from: "3.0.0")
    ],
    targets: [
        // Targets are the basic building blocks of a package. A target can define a module or a test suite.
        // Targets can depend on other targets in this package, and on products in packages which this package depends on.
        .target(
            name: "hello-perfect",
            dependencies: []),
    ]
)
```

Update the Package, type in terminal window:
> swift package update

Regenerate Xcode Project:
> swift package generate-xcodeproj

Import libraries inside *Main.swift* (Verify Target is selected in hello-perfectPackageDescription), finally Build and Run:
```Swift
import PerfectLib
import PerfectHTTP
import PerfectHTTPServer
```

### PROJECT CREATION AND BASIC CONFIGURATION ###






























