---
title: "KSeExpr 4.0.0 Released!"
date: "2020-11-16"
categories: 
  - "news"
  - "officialrelease"
---

[![Pattern generated by KSeExpr](../images/kseexpr-1024x1024.jpg)](https://krita.org/wp-content/uploads/2020/11/kseexpr.jpg)

Today, we're happy to announce the release of KSeExpr 4.0.0!

KSeExpr is the fork of Disney Animation's [SeExpr](https://wdas.github.io/seexpr/) expression language library that we ship with Krita. It powers the SeExpr Fill Layer that was done in Amyspark's Google Summer of Code 2020 project.

## The main changes

This is a ginormous release, but these are the most important bits:

- **We've rebranded the fork.** This allows us to both ship the library without conflict with upstream.
    - The library as a whole is now `namespace`d (both in CMake and in C++) as `KSeExpr`.
    - The base library is now `KSeExpr`, whereas the UI is now `KSeExprUI`. The include folders have been flattened accordingly, to e.g. `<KSeExpr/Expression.h>` and `<KSeExprUI/ExprControlCollection.h>`.
- **We've changed the license to GPL v3.** The original code was (and is still released) under a tainted form of Apache 2.0, which has brought us many headaches. We've followed LibreOffice's lead and our changes are now released under this license.
- All code has been **reformatted and upgraded with C++14 features**.
- **We've dropped the Python bindings, as well as pthread.** If you just need the library (like us), all you need now is Qt and a C++14 compiler.
- The existing optional LLVM evaluator has reached feature parity with the interpreter. We've patched missing functionality, such as automatic casting from 1D vectors to 3D and string operators.
- Our fork fully supports static LLVM and Android. No more linking or API level issues.
- Arc trigonometric functions and `rand()`, previously documented but non-existing in the runtime, have been added.

## Download

Source code: [kseexpr-4.0.1.0.tar.gz](https://download.kde.org/stable/kseexpr/4.0.1/kseexpr-4.0.1.0.tar.gz)

Release hashes:

- md5sum: `f3242a4969cda9833c2f685786310b76 kseexpr-4.0.1.0.tar.gz`
- sha256: `13b8455883001668f5d79c5734821c1ad2a0fbc91d019af085bb7e31cf6ce926 kseexpr-4.0.1.0.tar.gz`

GPG signature: [kseexpr-4.0.1.0.tar.gz.asc](https://download.kde.org/stable/kseexpr/4.0.1/kseexpr-4.0.1.0.tar.gz.asc).

The tarball is now signed by Amyspark's Github GPG key (`FC00108CFD9DBF1E`). You can get the key [at their Github's profile](https://github.com/amyspark.gpg).

## The full changelog for v4.0.0.0 (November 12, 2020)

### Added

- Add implementation of rand() function (`a84fe56`)
- Enable ECM's automatic ASAN support (`16f58e9`)
- Enable and fix skipped imaging and string tests (`e8b8072`)
- Standardize all comment parsing (`c12bdb4`)
- Add README for the fork (`abc4f35`)
- Rebrand our fork into KSeExpr (`97694c4`)
- Automagically deploy pregenerated parser files (`0ae6a43`)
- Use SPDX license statements (`83614e6`)
- Enable version detection (`e79c35b`)
- Use STL-provided mutex and drop pthread dependency (`1782a65`)
- Reimplement Timer (`20a25bd`)
- Complete the relicensing process (`b19fd13`)
- Enable arc functions (`08af2ef`)
- Add abandoned test for nested expressions (`2af1db3`)
- Add abandoned type check tests (`65064ad`)
- Implement equality between ColorSwatchEditables (`8d864ce`)
- Add the abandoned typePrinter executable (`2171588`)
- Add BSD-3 release scripts (`fe11265`)
- Automatically deploy version changes (`1ebb54b`)

### Fixed

- Fix printf format validation (`a77cbfd`)
- Fix LLVM's support for string variables (`13c1dcd`)
- Detect and link against shared libLLVM (`b57c323`)
- Fix compilation on Android (`3969081`)
- Only build KSeExprUI if Qt5 is enabled (`63a0e3f`)
- Sort out pregenerated parser files (`ee47a75`)
- Fix translation lookup (`e37d5f0`)
- Fix path substitution with pregenerated files (`46acc2e`)
- Restore compatibility with MSVC on Windows (`9a8fa7c`)
- Properly trim range comments (`6320439`)
- Fix Vec1d promotion with LLVM evaluator (`cd9651d`)
- Fix interpreter state dump in MinGW (`ee2ca3e`)
- Fix pointless negative check on demos (`7328466`)
- Fix SpecExaminer and add abandoned pattern matcher tool (`366e733`)

### Removed

- Clean up various strings (`8218ab3`)
- Remove Disney internal widgets (part 1) (`a30cfe5`)
- Remove Disney internal widgets (part 2) (`14b2610`)
- Remove Disney internal widgets (part 3) (`d3b9d34`)
- Remove Disney internal widgets (part 4) (`bc65b77`)
- Remove Disney-internal libraries (`da04f96`)
- Remove Qt 4 compatibility (`bdef3e2`)
- Drop unused demos (`884a977`)
- Assorted cleanup (`6c5134f`)
- Assorted linkage cleanup (`18af7e6`)
- Clean up KSeExpr header install logic (`98b4c50`)
- Assorted cleanup in KSeExpr (`735958f`)
- Remove more unused documentation (`8a2ac53`)
- Remove KSeExprUIPy (`68baed1`)
- Remove Platform header (`6d6db30`)
- Cleanup and remove the plugin system (`b3c4d48`)
- Remove unused files in KSeExprUI (`6229b88`)
- Remove last remnants of sscanf/old number parse logic (`5717cd6`)
- Remove leftovers of Disney's Python tests (`df24cc4`)
- General cleanup of the package lookup system (`d332d35`)
- Clean up last remaining warnings (`36ea2d5`)
- Remove unused variable in the parser (`813d1a0`)
- Remove redundant inclusion (`fb55833`)

### Changed

- Set Krita build (library and UI only) as default (`2deb17a`)
- Update pregenerated files (`2c8481c`)
- Update and clean Doxygen docs (`7df9011`)
- Make performance monitoring an option (`6253bcd`)
- clang-tidy: Curve (`5584b30`)
- clang-tidy: Vec (`b02a8b0`)
- clang-tidy: Utils (`f9b89ae`)
- Update README (`05212cb`)
- clang-tidy: ExprType (`e07d9d1`)
- clang-tidy: ExprPatterns (`03010ff`)
- clang-tidy: ExprEnv (`a22d3a3`)
- Modernize imageSynth demo to C++14 (`474e268`)
- Modernize imageEditor demo to C++14 (`a9c7538`)
- Modernize asciiGraph demo to C++14 (`ec103be`)
- Modernize asciiCalculator demo to C++14 (`8939da6`)
- Modernize imageSynthForPaint3d demo to C++14 (`7658d75`)
- clang-tidy in KSeExprUI (`85860c0`)
- clang-tidy: Context (`574b711`)
- clang-tidy: ErrorCode (`74860fb`)
- constexpr-ize noise tables (`7335fc7`)
- clang-tidy: VarBlock (`935da03`)
- clang-tidy: Interpreter (`83ed077`)
- Split tests by category and use GTest main() (`933f0cc`)
- clang-tidy: ExprColorCurve (`675f160`)
- clang-tidy: ExprBrowser (`84e2782`)
- clang-tidy: ExprWalker (`5d24b2b`)
- clang-tidy: ExprColorSwatch (`c667d97`)
- clang-tidy: ExprControl (`9313acf`)
- clang-tidy: ExprControlCollection (`fd0693d`)
- clang-tidy: ExprCurve (`efeff98`)
- clang-tidy: ExprEditor (`338dc3c`)
- clang-tidy: Evaluator (LLVM disabled) (`3927858`)
- clang-tidy: ExprBuiltins (part 1) (`8e8fe4f`)
- clang-tidy: ExprBuiltins (part 2) (`05c7e70`)
- clang-tidy unused variables (`58aef1d`)
- Make Examiner::post pure virtual at last (`e5cc038`)
- clang-tidy: ExprNode (`7da56ba`)
- clang-tidy: ExprLLVM (LLVM disabled) (`aa34f51`)
- clang-tidy: ExprFuncX (`6715180`)
- Modernize tests to C++14 (`455c3b6`)
- clang-tidy Utils (`ec8c1f0`)
- clang-tidy: Evaluator (LLVM enabled) (`9e82340`)
- clang-tidy: ExprLLVMCodeGeneration (`f23aca9`)
- :gem: v4.0.0.0 (`5f02791`)