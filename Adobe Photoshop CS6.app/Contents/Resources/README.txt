This is a Intrinsic Images library, developed towards inclusion in Photoshop CS6.

- Please keep all the important design decisions documented in this file.
- The directory names must be lower case, due to Perforce related limitations.
  Whereas the file names can be mixed case.
- Use cmake (2.8.4 current version) for building various library flavors until
  actual tech transfer.
- Use boost library judiciously. Photoshop world does not like some aspects of
  it. Libraries used by Intrinsics so far are - numerics
- I think we should (must) use gml. The issue is there is no "instance specific"
  way to enable/disable SSE optimization for classes. It is important that
  we can generate both SSE and non SSE code in a single library unit. Miklos?
- Use hpp file extension for c++ headers.
- Use "#pragma once" only, previous projects (strand) did not give any trouble.
  Miklos?



Todo:
- Check -mfpmath=sse -msse2 flags in CMakeLists.txt for all the compilers?
- Add version number logic and associated namespace to the library after
  consulting with Steve DiVerdi. cmake's configuration include file generation
  looks interesting.
- How to create a subdirectory under build for a target platform?
  Unfortunately, you can't set CMAKE_BINARY_DIR on the fly, it is implicitly
  defined.
