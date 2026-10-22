# NAT2MADE COMP — JUCE source project

This is a **source project, not a compiled or tested VST3 plugin**. It is an initial prototype for the NAT2MADE COMP concept.

Included: five-band EQ, two serial compressor stages, an EFFECT control that increases second-stage compression/saturation, input/output gain, dry/wet mix, bypasses, state save/restore, and a dark amber-accented interface.

Not implemented yet: external sidechain, sidechain listen/HPF, oversampling selection, Mid/Side, Delta monitoring, A/B comparison, preset bank, gain-reduction meters, installers, and commercial QA. The tonal references are inspiration only.

## Windows build
Requirements: Windows 10/11, Visual Studio 2022 with **Desktop development with C++**, Git for Windows, CMake tools, and internet for JUCE download.

From a terminal opened in this folder:
```bat
cmake -S . -B build -G "Visual Studio 17 2022" -A x64
cmake --build build --config Release --target NAT2MADE_COMP_VST3 NAT2MADE_COMP_Standalone
```
Expected VST3 bundle is usually under `build\\NAT2MADE_COMP_artefacts\\Release\\VST3\\NAT2MADE COMP.vst3`. Copy the complete bundle to `C:\\Program Files\\Common Files\\VST3`, then rescan plugins in REAPER.

AU is macOS-only and is not part of this Windows target. Build/test on macOS separately before considering this cross-platform.
