# GTestCpp

[![License](http://img.shields.io/:license-apache-orange.svg)](http://www.apache.org/licenses/LICENSE-2.0) 


## Quickstart

Simply include this pod in your `Podfile` for any OSX target:
```
pod 'GTestCpp', '~> 1.10.0'
```

Then, in any C++ *or Objective C++* executable where you want to run tests,
structure your `main()` like this:
```
#include <gtest/gtest.h>
#include "path/to/your/Module1Test.cpp"
#include "path/to/your/Module2Test.cpp"

int main(int argc, char * argv[]) {
  testing::InitGoogleTest(&argc, argv);
  return RUN_ALL_TESTS();
}
```

## Summary

This repo contains a [CocoaPod](https://cocoapods.org/) wrapper for the c++ 
[Google Test](https://github.com/google/googletest) project, which provides a
testing framework.  The Google Test project itself includes a `main()` to
make integration with traditonal C++ projects easy.  This Pod excludes that
`main()` for easier integration with OSX and XCode-based projects.

Note that the license used in this repo is independent of that used in
Google Test, which currently has a [BSD-like license](https://github.com/google/googletest/blob/master/LICENSE).

See also the GoogleTest pod 
[in Firebase](https://github.com/firebase/firebase-ios-sdk/blob/master/Firestore/Example/GoogleTest.podspec).

## Development

This repo contains a single Podspec file.  To modify, just edit the 
Podspect and use `pod repo push MyRepo GTestCpp.podspec.json --use-libraries`.

